---
title: Async data in components
description: Async data in components?
---

# Async data in components?

It is not possible because it's not linked to a route, Nuxt.js supercharges the component data() associated to a route to allow async data.

Faor sub components, there are 2 ways of achieving it:
1. Make the API call in the mounted() hook and setting the data afterwards. *Downside: no server rendering.*
2. Make the API call in the asyncData() method of the page component and giving the data as a prop to the subComponent. Server rendering will work fine. *Downside: the asyncData() of the page might be less readable because it's loading the async data of the sub components*

It all depends if you want the sub components to be server-rendered or not.

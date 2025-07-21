---
title: Netlify - Pricing Component
pubDate: Nov 8 2023
---

## Pricing component

When I started working at Netlify, we had pricing messages in our docs that told users if the feature they were reading about was offered on their current Netlify plan. The messages also mentioned the feature’s release stage, if applicable. However, these messages did not have consistent language and were scattered across numerous pages. If someone wanted to update the pricing message for a feature, they would have to search across multiple pages and update each message individually.

To solve this problem, I created a Vue.js component in our docs that contained all of our pricing messages. They were organized alphabetically by feature to make them easier to find. I made all of the messaging consistent and created a template for our team to use. Now, updating the pricing message is as easy as adding the small component code to the page and ensuring that the message is correct in the single Vue.js file.

Below is a screenshot example of the pricing component:

<img src="/portfolio/assets/img/pricingcomponent.png" alt="Pricing component">
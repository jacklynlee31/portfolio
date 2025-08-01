---
title: Netlify - Pricing Component
pubDate: Nov 8 2023
description: "Built a new Vue.js component for consistent pricing messages"
---

## Pricing component

When I started working at Netlify, we had pricing messages in our docs that told users if the feature they were reading about was offered on their current Netlify plan. The messages also mentioned the feature’s release stage, if applicable. However, these messages did not have consistent language and were scattered across numerous pages. If someone wanted to update the pricing message for a feature, they would have to search across multiple pages and update each message individually.

To solve this problem, I decided to use Vue.js.

First, I created a `messages.json` file to hold all of the features and pricing messages:

``` json
// messages.json
{
  "messages": {
    "directorySync": "Directory Sync is available on {elink}.",
    "organizations": "Organization management is available on {elink}.",
    "sso": "Single Sign-On (SSO) is available on {plink}."
  }
}
```

I made the list in alphabetical order to make it easy for the docs team to find and add feature names, when applicable. Each message followed a consistent format.

The message templates were pulled into a Vue component that handled formatting and rendering:

``` vue
<!-- PricingMessage.vue -->
<template>
  <div class="pricing">
    <p v-html="selectedMessage"></p>
  </div>
</template>

<script>
import messagesData from '../messages.json'

const enterpriseLink = '<a href="https://www.netlify.com/pricing/">Enterprise</a> plans'
const proLink = '<a href="https://www.netlify.com/pricing/">Pro</a> plans'

export default {
  props: { message: { type: String, required: true } },
  computed: {
    selectedMessage() {
      let raw = messagesData.messages[this.message] || 'Message not found.'
      raw = raw.replace('{elink}', enterpriseLink)
      raw = raw.replace('{plink}', proLink)
      return raw
    }
  }
}
</script>
```

The Vue component automatically replaced placeholders like `{elink}` and `{plink}` with HTML links to the correct pricing plan.

Once that was done, writers only had to include a brief line of code in the docs to pull in the correct message:

```vue
<PricingMessage message="directorySync" />
```

This component made pricing plan updates much faster and reduced inconsistencies.
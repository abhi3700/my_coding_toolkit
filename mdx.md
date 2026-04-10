# MDX

Learn everything about MDX syntax.

> Useful in mintlify, ... docs.

## Syntax

- Start of page:

```mdx
---
title: "Welcome"
description: "Everything you need to send/receive payments using stablecoins."
icon: "robot"
---
```

> Here, icon has to be checked if supported as per **FontAwesome**.

- Cards in grid:

```mdx
<Columns cols={2}>
  <Card title="Web App" icon="globe" href="/webapp/overview">
    Explore the UniFi dashboard and payment flows.
  </Card>

  <Card title="Falcon Agent" icon="robot" href="/falcon/overview">
    Automate payments, scheduling, and workflows using your AI-powered payment agent.
  </Card>

  <Card title="Payment Gateway" icon="credit-card" href="/payment-gateway/overview">
    Accept payments globally with UniFi — built for merchants and platforms.
  </Card>

  <Card title="CLI" icon="terminal" href="/cli/overview">
    Automate payments and manage workflows via CLI.
  </Card>

  <Card title="API Reference" icon="code" href="/api-reference/introduction">
    Integrate UniFi into your product or backend.
  </Card>
</Columns>
```

- Gray color card/callout

```mdx
<Callout>
Built for real-world payments — from freelancers to enterprises.
</Callout>
```

- Blue color card/callout

```mdx
<Note>
Built for real-world payments — from freelancers to enterprises.
</Note>
```

- Green color card/callout

```mdx
<Tip>
Built for real-world payments — from freelancers to enterprises.
</Tip>
```

- Yellow color card/callout

```mdx
<Warning>
Built for real-world payments — from freelancers to enterprises.
</Warning>
```

- Divider (same as markdown)

```mdx
---
```

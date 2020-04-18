# html-embed Attributes

You can pass custom attributes to the `<widgetbot>` element, to change the options when initializing it, for example:

```html
<widgetbot
  server="299881420891881473"
  shard="https://e.widgetbot.io"
></widgetbot>
```

## Available options

::: tip Definitions

```ts
type url = string

interface Attributes {
  // Server + channel IDs
  server: string
  channel?: string

  // The height and width. You can specify a number to
  // use pixels or use CSS units eg. 100%
  width?: number | string
  height?: number | string

  // Connect to a custom WidgetBot server (Only set this if you are explicitly told to)
  shard?: url
}

export default Attributes
```
:::
# Crate Options

You can customize Crate when initializing it. In the example below `location: ['top', 'left']` was added:

```ts
new Crate({ server: '299881420891881473', location: ['top', 'left'] })
```

This will change Crate's default location from bottom right on the page to top left. To find out more, about location options, see the relevant section in [Definitions](##Definitions). 

> [!IMPORTANT]
> You must include a comma `,` after each complete option except the last one, and remove the question mark `?` when customizing.

Below are some options that Crate supports with more in-depth explanations further below. 

## Definitions

::: tip TypeScript definitions

```ts
type url = string
type size = string

export type vertical = 'top' | 'bottom' | number
export type horizontal = 'left' | 'right' | number

interface Options {
  // Server + channel IDs
  server: string
  channel?: string

  // Thread ID
  thread?: string

  // Dynamic username
  username?: string
  // Dynamic avatar
  avatar?: string

  // Accessibility settings
  accessibility?: string[]
  // The settings group to use
  settingsGroup?: string

  // JWT login
  token?: string

  // Where the button should appear on-screen
  location?: [vertical, horizontal]

  // The color of the button
  color?: string
  // The glyph to display on the button
  glyph?: [url, size]
  // Custom CSS to be injected into the Shadow root
  css?: string

  // Crate message notifications
  notifications?: boolean
  // Crate unread message indicator
  indicator?: boolean
  // Crate notification timeout
  timeout?: number

  // Enables notifications to be triggered for all channels, in crate and embed
  allChannelNotifications?: boolean
  // Embed notification timeout
  embedNotificationTimeout?: number

  // Only load the widget once the user opens it
  defer?: boolean
  // Connect to a custom WidgetBot server
  shard?: url
}

export default Options
```
## Explanations
### Server + channel IDs
This option displays the default channel when opening the Widgetbot Crate. Crate's server string has to be the server ID of the channel you want displayed. To learn how to find server and channel IDs, check out the [html-embed tutorial](https://docs.widgetbot.io/embed/html-embed/tutorial#html-embed-tutorial). 

### Thread ID
To make a specific thread be the default, add `thread: 'ID String'` to Crate option. Finding the thread ID will be the same steps as finding the server and channel IDs. 

### Color
By default, Crate will use Discord's official colors. Add `color: 'string'` and replace `string` with either a RGBA or Hex color code. 

Transparency is supported.

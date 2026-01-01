# Snippets

reminder that some may not work.

## in use

- [Chat Related Toasts At Top v2](https://nspc911.github.io/themes/vencord/ChatRelatedToastsAtTopv2.theme.css)

  Improves the original Chat Related Alerts at Top snippet by reducing the `:has` selector usage as much as possible

- [Members Hide Unless Hover](https://nspc911.github.io/themes/vencord/MembersHideUnlessHover.theme.css)

  hide the members list until you hover on it

- [Bordered Embeds](https://nspc911.github.io/themes/vencord/BorderedEmbeds.theme.css)

  Adds borders to embeded contents, like webhooks and previews. Need I say more?

  `Variables`

  ```css
  :root {
    /* Border width for the embeds */
    --wh-border-width: 4px;
    /* Background opacity. The higher it is, the more of the border color seeps through */
    --wh-background-opacity: 0%;
    /* Default background color. Relative color is used for those who use transparent themes */
    --wh-default-background: hsl(from var(--background-surface-high) h s l / 100%);
    /* Whether to keep the Suppress Embed button shown, or hide when not hovered on */
    --wh-always-show-suppress-embed-button: 0
  }
  ```

  [<kbd>Jump to message</kbd>](https://discord.com/channels/1015060230222131221/1028106818368589824/1402181676007821324)

- HSL x Better Folders

  Fixes Horizontal Server List breaking the extra sidebar of Better Folders

  Use my [HSL Version](https://nspc911.github.io/themes/vencord/HorizontalServerList.theme.css) instead

- [Image Zoom Spyglass Lens](https://nspc911.github.io/themes/vencord/vc-spyglass-image-zoom-lens.css)

  Turns the Image Zoom plugin from Vencord into a spyglass, with an optional zoom animation

`Variables`

  Turns the Image Zoom plugin from Vencord into a spyglass, with an optional zoom animation

  `Variables`

  ```css
  /* set to 0 to disable animation */
  :root {
    --vcizl-animate-duration: 1s
  }
  ```

  [<kbd>Jump to message</kbd>](https://discord.com/channels/1015060230222131221/1028106818368589824/1430160181357969449)

## not used

- [Refreshed Seamless Chat Bar](https://nspc911.github.io/themes/vencord/RefreshedSeamlessChatBar.theme.css) 📦

  Moves `Someone is typing`, `Cooldown is active`, `You are viewing older messages` and `Replying to someone` such that they are seamless with the message bar

  [<kbd>Jump to message</kbd>](https://discord.com/channels/1015060230222131221/1028106818368589824/1354738654148427786)

  `Variables`

  ```css
  :root {
    /* change padding of the bar */
    --rscb-chat-box-padding: 8px; /* default is 8px for alignment */
    /* Whether you want the chat to clip typing status *\
    \*   thorough the bar when someone starts typing   */
    --rscb-clip-chat-through-typing-bar: 0;
    /* use a fixed upload button if your *\
    \*      find it not aligned          */
    --rscb-use-fixed-attach-button: 0;
  }
  ```

- [midnight island chat status](https://nspc911.github.io/themes/vencord/MidnightIslandChatStatus.theme.css) 📦

  turns the `x is typing` and `slowmode is enabled` into their separate pills that hover over the chat bat. May not work with non-midnight themes.

- [Chat Related Alerts at Top](https://nspc911.github.io/themes/vencord/ChatRelatedAlertsAtTop.theme.css) 📦

  Moves the `x number of new messages` and `You are viewing old messages` to the top and make them seamless with each other (down to the button style)

  `Variables`

  ```css
  :root {
    /* Set to 1 if you want them to float  *\
    |*      Recommended while using        *|
    \*      Midnight/Rounded Themes        */
    --craat-popout: 0; /* Default = 0 */
    /* Change the border radius *\
    \*      for the alerts      */
    --craat-border-radius: 16px; /* default: 16px */
  }
  ```

  [<kbd>Jump to message</kbd>](https://discord.com/channels/1015060230222131221/1028106818368589824/1354756324285743216)

- [Blurry Backdrop](https://nspc911.github.io/themes/vencord/BlurryBackdrop.theme.css) 📦

  Make backdrops formed from full screen elements be blurry

  `Variables`

  ```css
  :root {
    /* The blur radius, can be *\
    \*   any types of length   */
    --blrbg-blur-by: 2px;
    /* how dim you want the bg *\
    \*   aside from the blur   */
    --blrbg-dimmness: 25;
  }
  ```

  [<kbd>Jump to message</kbd>](https://discord.com/channels/1015060230222131221/1028106818368589824/1362083384829935920)

- [Blurry Settings Modal](https://nspc911.github.io/themes/vencord/BlurrySettingsModal.theme.css) 📦

  Makes `the.rabbit.disabler`'s '[Make Settings a window](https://discord.com/channels/1015060230222131221/1028106818368589824/1353097168214425693)' snippet have the settings and options background be transparent (i mean literally every element except toggles and buttons :3)

  `Variables`

  ```css
  :root {
    /* The blur radius, can be *\
    \*   any types of length   */
    --blrsm-blur-by: 5px;
    /* how dim you want the bg *\
    \*   aside from the blur   */
    --blrsm-dimmness: 25;
  }
  ```

  [<kbd>Jump to message</kbd>](https://discord.com/channels/1015060230222131221/1028106818368589824/1362419625945464852)

- Blurry Quick Switcher 📦

  Makes Quick Switcher have a blurry background. What more did you expect.

  [<kbd>Jump to message</kbd>](https://discord.com/channels/1015060230222131221/1028106818368589824/1362656483770372219)

- [Client Theme for Visual Refresh](https://nspc911.github.io/themes/vencord/VisualRefreshClientTheme.theme.css) 📦

  Adds the compatibility for Client Theme to work on Visual Refresh (may change if Discord fixes the variables)

  [<kbd>Jump to message</kbd>](https://discord.com/channels/1015060230222131221/1028106818368589824/1331976527545368646)

  This snippet will be archived after the fix has been merged.

<sub>
Footnotes:
1. If a snippet doesn't have a url, refer to the message.
2. If a snippet has <kbd>📦</kbd>, it means that I no longer use the snippet.
<sub>

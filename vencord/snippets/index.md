# Snippets

- [Seamless Chat Bar](https://nspc911.github.io/themes/vencord/SeamlessChatBar.theme.css) 🗝

  Moves `Someone is typing`, `Cooldown is active`, `You are viewing older messages` and `Replying to someone` such that they are seamless with the message bar

  [<kbd>Jump to message</kbd>](https://discord.com/channels/1015060230222131221/1028106818368589824/1322496323202715689)

  `Variables`

	```css
	:root {
	  /* Use if your theme overwrites the color like Nocturnal
	  --channeltextarea-background: var(--backgroundColor01);*/
	  /* set to 0px if no applauncher */
	  --scb-applauncher-padding: -52px; /* default = -52px */
	  /* border radius of bar */
	  --scb-border-radius: 8px; /* default = 8px */
		}
	```

- [Refreshed Seamless Chat Bar](https://nspc911.github.io/themes/vencord/RefreshedSeamlessChatBar.theme.css) 🔃

  ^ but for Visual Refresh

  [<kbd>Jump to message</kbd>](https://discord.com/channels/1015060230222131221/1028106818368589824/1354738654148427786)

  `Variables`

    ```css
	:root {
	  /* change padding of the bar */
	  --rscb-chat-box-padding: 8px; /* default is 8px for alignment */
	}
	```

- [Chat Related Alerts at Top](https://nspc911.github.io/themes/vencord/ChatRelatedAlertsAtTop.theme.css) 🔃

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

  [<kbd>Jump to message</kbd>]()

- HSL x Better Folders 🔃

  Fixes Horizontal Server List breaking the extra sidebar of Better Folders

  Use my [HSL Version](https://nspc911.github.io/themes/vencord/HorizontalServerList.theme.css) instead

- Pin a server 🗝

  Allows you to pin any server of your choice to replace the pinned Discovery icon. **The server must not be in a folder**

  [<kbd>Jump to message</kbd>](https://discord.com/channels/1015060230222131221/1028106818368589824/1327967783778254868)

- [Client Theme for Visual Refresh](https://nspc911.github.io/themes/vencord/VisualRefreshClientTheme.theme.css) 🔃

  Adds the compatibility for Client Theme to work on Visual Refresh (may change if Discord fixes the variables)

  [<kbd>Jump to message</kbd>](https://discord.com/channels/1015060230222131221/1028106818368589824/1331976527545368646)

  This snippet will be archived after the fix has been merged.

- No Favourite Channel Icon 🗝

  Removes the channel icons from channels while using Favorites v2

  [<kbd>Jump to message</kbd>](https://discord.com/channels/1015060230222131221/1028106818368589824/1337032719602946079)

<sub>
Footnotes:
1. If a snippet doesn't have a url, refer to the message.
2. If a snippet has <kbd>🔃</kbd>, it means it works for Visual Refresh
3. If a snippet has <kbd>🗝️</kbd>, it means it works on pre-refresh
<sub>

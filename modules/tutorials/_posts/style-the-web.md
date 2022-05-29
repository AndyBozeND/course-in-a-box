---
title: Custom styling a website
---

## Getting the Stylus add-on for your browser
We'll use Firefox in this tutorial, but you can do the same thing in the Chrome and Edge browsers.
1. Select **Add-ons and themes** from the browser menu or just press **Ctrl+Shift+A**.
2. Search for the add-on **stylus** and install it.
3. 3. Make sure that the Stylus extension is enabled. You should see that a Stylus button has been added to the browser toolbar.

<img src="/img/stylus_button.png" alt="Screenshot of the Stylus add-on button"/>

## Using developer tools
Firefox's Web Developer Tools lets you inspect web pages. You can see the HTML and any CSS. Press **Ctrl+Shift+I** when you are viewing a web page to inspect the page. 

<img src="/img/dev_tools.png" alt="Screenshot of the developer tools window"/>

## Adding custom CSS to style a web page
As an example, perhaps you work in the Primo Back Office, sometimes in test and sometimes in production. You might want to easily distinguish between the two environments so that you don't accidentally change something in production when you meant to make the change in test. Any easy way to distinguish between the two would be to colorize test. In this example, we've colorized test to be pink.

<img src="/img/bo_login.png" alt="Screenshot of the colorized logon page"/>

First, visit the Primo staging logon page, then click the Stylus button and click on **Write style for this URL**.

<img src="/img/staging_styles.png" alt="Screenshot of the Stylus create style"/>

Paste the following CSS into the editor.

```
  body {
      mix-blend-mode: multiply;
      isolation: auto;
  }
  body::after {
      position: fixed;
      content: " ";
      top: 0;
      left: 0;
      height: 100vh;
      background-color: rgba(255, 100, 50, .2);
      width: 100vw;
      z-index: 1000;
      pointer-events: none;
  }
```
Be sure to select **URLs on the domain** at the bottom of the editor so that the CSS will affect all page in Back Office. Fill in a name for the style, such as **Primo staging** in the box in the top left corner, then click the **Save** button below the box.

Go back to the Primo staging tab and you should see it with a pink tint. If it doesn't, click on the Stylys button, and be sure that the **Turn all styles off** box is unchecked.

You can return to the Stylus editor to add more CSS to **Primo staging** if you want to make further customizations.

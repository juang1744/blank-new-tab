<h1 align="center" width="100%">
  <a href="https://github.com/juangutierrez01/chrome-custom-new-tab"><img src="./extension_icon.svg" alt="Chrome extension logo" width="36rem"></a>
  chrome-custom-new-tab
</h1>

<p align="center">
  <a href="/"><img src="https://img.shields.io/badge/Chrome-4285F4?logo=google-chrome&logoColor=white" alt="Google Chrome badge"></a>
  <a href="/"><img src="https://img.shields.io/badge/Size-<1MB-limegreen" alt="Size <1MB badge"></a>
  <a href="/"><img src="https://img.shields.io/badge/HTML-E34F26?logo=html5&logoColor=white" alt="HTML badge"></a>
  <a href="/"><img src="https://img.shields.io/badge/🌙Dark_Mode-dimgrey" alt="Dark Mode badge"></a>
  <a href="/"><img src="https://img.shields.io/badge/☀️Light_Mode-white?logo=sun&logoColor=white" alt="Light Mode badge"></a>
</p>

Replace Google's default new tab page ...

<details>
  <summary><code>chrome://new-tab-page/</code></summary>
  
```html
<!doctype html>
<html dir="ltr" lang="en"
    chrome-refresh-2023>
  <head>
    <meta charset="utf-8">
    <title>New Tab</title>
    <style>
      body {
        background: #3C3C3C;
        margin: 0;
      }

      #backgroundImage {
        border: none;
        height: 100%;
        pointer-events: none;
        position: fixed;
        top: 0;
        visibility: hidden;
        width: 100%;
      }

      [show-background-image] #backgroundImage {
        visibility: visible;
      }
    </style>
  </head>
  <body>
    <iframe id="backgroundImage" src=""></iframe>
    <ntp-app></ntp-app>
    <script type="module" src="new_tab_page.js"></script>
    <link rel="stylesheet" href="chrome://resources/css/text_defaults_md.css">
    <link rel="stylesheet" href="chrome://theme/colors.css?sets=ui,chrome">
    <link rel="stylesheet" href="shared_vars.css">
  </body>
</html>
```

</details>

...with a far simpler custom new tab:

```html
<title>New Tab</title>
<link rel="icon" href="images/extension_icon.svg" type="image/svg+xml">
<style>@media(prefers-color-scheme:dark){body{background:#3c3c3c}}</style>
```

|Before|After|
|---|---|
|![Default Light Mode](./before_light.png#gh-light-mode-only)![Default Dark Mode](./before_dark.png#gh-dark-mode-only)|![Custom Light Mode](./after_light.png#gh-light-mode-only)![Custom Dark Mode](./after_dark.png#gh-dark-mode-only)|

## Installation

1. Download this repository:

    ```bash
    git clone https://github.com/juangutierrez01/chrome-custom-new-tab/
    ```

2. On Google Chrome, head to `chrome://extensions`
3. Turn on `Developer mode`
4. Click `Load Unpacked`
5. Select the folder `chrome-custom-new-tab` that was downloaded in step 1.
6. Success! Your new tab page should now be a custom, blank page.

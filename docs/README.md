# Welcome to Docs Page
This page serves as a file archive and provides fast access to them.

Without leaving the page, you can navigate through all kinds of files, such as http pages, jupyter notebooks, and pdf files, etc...

## Guide
My function need to access some attributes of external website, and it is often restricted due to [**Same-origin policy**](https://stackoverflow.com/questions/25098021/securityerror-blocked-a-frame-with-origin-from-accessing-a-cross-origin-frame).

#### To have `auto-window-size` function works properly, there are two solutions:
1. Click the switch on the navigation bar above to enable `<iframe>` window scrolling.
2. For the best performance, disable the same-origin policy in your browser:*
   1. [Google Chrome](https://stackoverflow.com/questions/3102819/disable-same-origin-policy-in-chrome)
   2. [Mozilla Firefox](https://stackoverflow.com/questions/17088609/disable-firefox-same-origin-policy)
   3. [Apple Safari](https://stackoverflow.com/questions/4556429/disabling-same-origin-policy-in-safari)

***Warning: Disabling the same-origin policy this is very unsafe and should NEVER being done if you do not know exactly what you are doing.**

### IMPLEMENTATION
Page rendering is achieved by using `<iframe>` window in html. I implement an automatic iframe height adjuster using Javascript for full screen display as following,

```Javascript
function resizeIframe(iframe) {
    iframe.style.height = iframe.contentWindow.document.documentElement.scrollHeight + 'px';
}
```






















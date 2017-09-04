# Slack Themes

How to turn slack app into the Dark :)

---

## How to
- Go to
```sh
cd /Applications/Slack.app/Contents/
cd ./Resources/app.asar.unpacked/src/static
vi ssb-interop.js
```
- Edit `ssb-interop.js` to add the following lines:


```js
document.addEventListener('DOMContentLoaded', function() {
 $.ajax({
   url: 'https://raw.githubusercontent.com/mdellerie/slack-themes/master/black.css',
   success: function(css) {
     $("<style></style>").appendTo('head').html(css);
   }
 });
});
```

---

## Preview

![Screenshot](screenshot.png)

+++
Don't hesitate to fork the CSS to customize the darkness :)

---
Thanks for watching :)
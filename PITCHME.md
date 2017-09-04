# slack-themes

just append the following to app.asar.unpacked/src/static/ssb-interop.js:

```
document.addEventListener('DOMContentLoaded', function() {
 $.ajax({
   url: 'https://raw.githubusercontent.com/mdellerie/slack-themes/master/black.css',
   success: function(css) {
     $("<style></style>").appendTo('head').html(css);
   }
 });
});
```
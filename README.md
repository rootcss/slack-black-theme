# slack-black-theme


On Mac, open the file at this path:

`/Applications/Slack.app/Contents/Resources/app.asar.unpacked/src/static/ssb-interop.js`

and paste the following snippet at the end of it.


```javascript
document.addEventListener('DOMContentLoaded', function() {
    $.ajax({
        url: 'https://raw.githubusercontent.com/laCour/slack-night-mode/master/css/raw/black.css',
        success: function(css) {
            $("<style></style>").appendTo('head').html(css);
        }
    });
});
```

Reference: https://github.com/laCour/slack-night-mode/issues/73#issuecomment-287467332


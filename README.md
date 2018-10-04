# slack-black-theme


On Mac, open the file at this path:

`/Applications/Slack.app/Contents/Resources/app.asar.unpacked/src/static/ssb-interop.js`

and paste the following snippet at the end of it.


```javascript
document.addEventListener('DOMContentLoaded', function() {
    $.ajax({
        url: 'https://gist.githubusercontent.com/rootcss/b9f3c596932f638a3ff770819245c553/raw/cbfd99c3d6a3ace953af91a0b1a8f9d6fbaf97c1/black.css',
        success: function(css) {
            $("<style></style>").appendTo('head').html(css);
        }
    });
});
```

Note: I recommend to create your own gist and use that as your source in above snippet. This will prevent you from XSS and few others attacks. PS: Don't use a remote snippet which is controlled by someone else :)


Reference: https://github.com/laCour/slack-night-mode/issues/73#issuecomment-287467332


# js-sdk

## Add Widget

To add the widget, simply paste the embedding code to the page.

### Example of the embedding code

```html
<script>
(function(i,s,o,g,r,a,m){i['FluxWidgetObject']=r;i[r]=i[r]||function(){
(i[r].q=i[r].q||[]).push(arguments);};a=s.createElement(o);m=s.getElementsByTagName(o)[0];
a.async=1;a.src=g;a.id='FluxWidgetScript';m.parentNode.insertBefore(a,m);
})(window,document,'script','https://my.allychat.ru/widget/dist/widget.js','fab');

fab('init', {});

</script>
```

URL to widget `https://my.allychat.ru/widget/dist/widget.js` is specified just for example. For each instance, URL will be different.
 
Settings is specified when initializing the widget `fab('init', {})`
Available settings:
* alias - unique client ID (by default will generate an anonymous random alias)
* appId - application ID (need for splitting by multiple application)
* bubbleColor - color for the widget button and the message bubbles (common widget color)
* lightTheme - light mode of widget theme (need if light bubble color is specified)

Examples:
```javascript
fab('init', {alias: 'ABC123', appId: 'mobile', bubbleColor: 'white', lightTheme: true});

fab('init', {alias: 'FOOBAR', bubbleColor: '#33aa8f'});
```

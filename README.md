# js-sdk

## Подключение виджета

Для подключения виджета нужно вставить небольшой кусок кода на страницу.

### Пример кода для вставки виджета

```html
<script>
(function(i,s,o,g,r,a,m){i['FluxWidgetObject']=r;i[r]=i[r]||function(){
(i[r].q=i[r].q||[]).push(arguments);};a=s.createElement(o);m=s.getElementsByTagName(o)[0];
a.async=1;a.src=g;a.id='FluxWidgetScript';m.parentNode.insertBefore(a,m);
})(window,document,'script','https://my.allychat.ru/widget/dist/widget.js','fab');

fab('init', {});

</script>
```

Путь к виджету `https://my.allychat.ru/widget/dist/widget.js` указан в качестве примера. Для каждого клиента он будет свой.
 
При инициализации виджета `fab('init', {})` передаются настройки виджета.
Список настроек:
* alias - уникальный идентификатор пользователя. По-умолчанию генерируется автоматически.
* appId - идентификатор приложения. Нужен только для разделения по разным каналам.

Пример
```javascript
fab('init', {alias: 'ABC123', appId: 'mobile'});
```

# jQuery Video Popup Plugin (Vimeo and YouTube)

### Utilizando

Depois de incluir o jQuery e os arquivos do plugin na sua página HTML, basta criar a div que irá receber a ação do popup.

```html
<a id="video" video-url="https://www.youtube.com/watch?v=0wCC3aLXdOw">
    Open Popup
</a>
```


```javascript
$("#video").videoPopup({
    autoplay: 1,
    controlsColor: 'white',
    showVideoInformations: 0,
    width: 1000,
});
```

---

### Options

É possível definir diversas opções na chamada do popup:
```javascript
$("#video").videoPopup({
    autoplay: false,
    showControls: true,
    controlsColor: null,
    loopVideo: false,
    showVideoInformations: true,
    width: null
});
```

### Custom Options
Cada plataforma possui atributos diferentes, então, caso precise, você pode defini-los utilizando o ```customOptions```
YouTube -> https://developers.google.com/youtube/player_parameters?hl=pt-br#Parameters
Vimeo -> https://developer.vimeo.com/apis/oembed#arguments
```javascript
$("#video").videoPopup({
    autoplay: 1,
    controlsColor: 'white',
    showVideoInformations: 0,
    width: 1000,
    customOptions: {
        rel: 0,
        end: 60
    }
});
```
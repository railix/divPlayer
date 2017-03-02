# divPlayer

**divPlayer** is a HTML5 video player written in JavaScript, CSS and HTML. The player's HTML content is generated in 1 or more `div` containers of you choice. Multiple player instances are supported (see [How to use](https://github.com/railix/divPlayer#how-to-use)).

## Content
* [Screenshots](https://github.com/railix/divPlayer#screenshots)
* [Features](https://github.com/railix/divPlayer#features)
* [Browser support](https://github.com/railix/divPlayer#browser-support)
* [How to use](https://github.com/railix/divPlayer#how-to-use)
* [Player settings](https://github.com/railix/divPlayer#player-settings)
* [Contact](https://github.com/railix/divPlayer#contact)
* [License](https://github.com/railix/divPlayer#license)

## Screenshots
<img src="https://cloud.githubusercontent.com/assets/25888776/23147596/832b089c-f7e0-11e6-9228-7e829b52fc42.png" width="480" height="290" />
<img src="https://cloud.githubusercontent.com/assets/25888776/23147598/86ecb110-f7e0-11e6-8ebd-de4c7588b6e8.png" width="480" height="290" />
## Features
**divPlayer** version **0.1** supports:
- Basic functionalities like: **play/pause**, **full screen**, **seek**, **change/mute/unmute volume**.
- Multiple players on same page.
- Specify different player settings like `width`, `height`, `autoplay` etc. for each player (see [Player settings](https://github.com/railix/divPlayer#player-settings)).
- Keyboard pause/resume (`space`) and mute/unmute (`m`).
- Seeking through the video by clicking on the progress bar and by dragging it.
- Limited CPU footprint while seeking through video.

### Browser support
Tested and supported on the following browsers:

#### Desktop
| browser        | version     |
| ---------------|:------------|
| Firefox        | >= 49       |
| Chrome         | >= 55       |
| IE             | >= 11       |
| Edge           | >= 20.10240 |
| Opera          | >= 43       |
**May work on other/lower versions of browsers.**
**Safari: not tested, but if you have tested it, please provide feedback.**

#### Mobile
| browser                      | version          | OS                |
| -----------------------------|:-----------------|:------------------|
| Firefox                      | >= 50.1          | >= Android 5.0    |
| Chrome                       | >= 55            | >= Android 5.0    |
| Internet (Samsung browser)   | >= 3.2.38        | >= Android 5.0    |

## How to use
Download the content of the **src** folder above (**divplayer.css**, **divplayer.js** and **fonts** folder) and see examples below.

### 1 player on webpage
```HTML
<head>
  <link rel="stylesheet" href="divplayer.css"/>
</head>
<body>

  <div id="myVideo"></div>
  
  <script type="text/javascript" src="divplayer.js"></script>
  <script>
    divPlayer.start([
    {
      id: "myVideo",
      src: "http://link/to/video/file.mp4"
    }]);
  </script>
</body>
```
### 2 players in webpage
```HTML
<head>
  <link rel="stylesheet" href="divplayer.css"/>
</head>
<body>

  <div id="myVideo"></div>
  <div id="myVideo2"></div>
  
  <script type="text/javascript" src="divplayer.js"></script>
  <script>
    divPlayer.start([
    {
      id: "myVideo",
      src: "http://link/to/video/file.mp4"
    },
    {
      id: "myVideo2",
      src: "http://link/to/video/file2.mp4"
    }]);
  </script>
</body>
```
  
### Player settings
| property        | value examples                   | required | type   | info                              |
| --------------- |:---------------------------------|:--------:| ------:|:----------------------------------|
| id              |         -                        | yes      | string | id of `div` element               |
| src             |         -                        | yes      | string | URL of video file                 |
| width           | "854"                            | no       | string | width of player (default: "854")  |
| height          | "480"                            | no       | string | height of player (default: "480") |
| img             | "http://link/to/img.png"         | no       | string | URL of poster image for player to display when web page loads|
| autoplay        |  "true" / "false"                | no       | string | start playing automatically after page load (default: "false")|
| preload         |  "none" / "metadata" / "auto"    | no       | string | `"none"` = do not load video data when page loads (default), `"metadata"` = load only video duration, `"auto"` = start buffering video when page is loaded|
| mobileui        |  "0" / "1" / "2"                 | no       | string | use mobile UI for mobile devices (bigger controlbar). `"0"` = use mobile UI if mobile device is auto-detected (default), `"1"` = always use mobile UI, `"2"` = always use non-mobile UI |

## Contact
If you have any general remarks/questions/ideas about improvement/requests/technical issues, do not hesitate to contact me through GitHub or open a thread in the **Issues** section.

## License
MIT License

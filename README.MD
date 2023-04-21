# Instagram-stories - Stories like on instagram. 📸

<br>

<p align="center">
  <a href="#-about-the-project">About the project</a> •
  <a href="#-technologies">Technologies</a> •
  <a href="#-getting-started">Getting started</a> •
  <a href="#-license">License</a>
</p>

<p align="center">
<img alt="project preview" src="./.github/stories.jpg" width="75%"   >
</p>

## 👩‍💻 About the project

This project is a slider like the instagram stories. Developed using vanilla JS and Typescript languages. Fully responsive and designed with focus on accessibility.

Among the main functionalities of this slider, we can highlight: the support for images and videos, the slider is able to automatically slide between stories, the possibility to pause the exhibition of the stories and the feature to return to the last viewed story after refreshing the page.

With all these functionalities, this slider is a great option for those who want to create an interactive and attractive experience for their users.  

[click here, see closer](https://instagram-stories-cs.netlify.app/) 😉

## Usage

 The ``Slide`` class implements the story carousel, it expects to receive 4 parameters:

- **container**: an HTML element that will contain the slides. 
- **slides**: an array of HTML elements that represent each slide to be displayed.
- **controls**: an HTML element that contains the controls for navigating through the slides (previous and next buttons).
- **time**: a numeric value that represents the duration time of each slide in milliseconds (optional, the default value is 5000).

```javascript
const container = document.getElementById("slide");
const elements = document.getElementById("slide-elements");
const controls = document.getElementById("slide-controls");

if (container && elements && controls && elements.children.length) {
  const slide = new Slide(
    container, 
    Array.from(elements.children),
    controls,
    3000
  );
}
```

## Methods

The slide class has some public methods that can be useful for many different projects.

| Method               | Description           |                                                                                                                       
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------| - 
| `show(index: number)`|   Displays the slide corresponding to the index passed as parameter and updates the state of the control.    
| `prev()`|    Shows the slide preceding the current slide.     
| `next()`|    shows the next slide after the current slide.
| `pause()`|   pauses the automatic slideshow. This is triggered by a "pointerdown" event (such as a click or tap) in the slideshow controls.
| `continue()`| continues the automatic presentation of the slides after the pause. This is triggered by a "pointerup" or "touchend" event outside the slideshow controls
| `autoVideo(video: HTMLVideoElement)`|   Adds a new video to the slide and sets the transition time equal to the duration of the video. This function can be useful if you want to add a video dynamically to the slide after startup, or if you want to modify the transition time of the slide to match the duration of the video.

example:

```javascript
 ...
const slide = new Slide(
  container, 
  Array.from(elements.children),
  controls,
  3000
);

// Display the second slide
slide.show(1);

// Move to the previous slide
slide.prev();

// Move to the next slide
slide.next();

// Pause the slideshow
slide.pause();

// Resume the slideshow
slide.continue();

// Add a new video and set the transition time to match its duration
const video = document.getElementById("video2");
slide.autoVideo(video as HTMLVideoElement);
...

```

## 🚀 Technologies

- Javascript
- [Typescript](https://www.typescriptlang.org/)
- [Vite](https://vitejs.dev/)


## 💻 Getting started

### Requirements

- [Node.js](https://nodejs.org/en/)
- [Yarn](https://classic.yarnpkg.com/) or [NPM](https://www.npmjs.com/) _(examples are with NPM)_ 

**Clone the project and access the folder**

```bash
$ git clone https://github.com/leandrorodrigues00/instagram-stories && cd instagram-stories

```

**Follow the steps below**

```bash
# Install the dependencies
$ npm i


# Start the app
$ npm run dev
```

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<p align="center">
  Made with 💜&nbsp; by  Leandro Rodrigues
</p>

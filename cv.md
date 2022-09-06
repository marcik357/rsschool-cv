# Anton Mykhailichenko
## My contacts:

__Phone:__ +38 (098) 850 77 93

__Telegram__: [@marcik357](https://t.me/marcik357)

__e-mail:__ [marcik357@gmail.com](mailto:marcik357@gmail.com)

## About Me
I am a prepress engineer with ten years of experience. Lost a job due to the war and now I'm studying Front-end.

## Skills:
* HTML
* CSS
* JS (basic level)

## Code examples:
Create 100 dragble objects:
[codepen.io](https://codepen.io/marcik357/pen/WNJvJQa)
```javascript
let generateButton = document.querySelector("#generateButton");
let interactivePanel = document.querySelector("#interactivePanel");

let currentDiv;
let move = false;
let offsetX, offsetY;

generateButton.addEventListener("click", function () {
  interactivePanel.innerHTML = "";
  for (let i = 0; i < 100; i++) {
    interactivePanel.append(generateElement());
  }
});

interactivePanel.addEventListener("mousedown", function (e) {
  if (e.target.parentElement == interactivePanel) {
    move = true;
    offsetX = e.offsetX;
    offsetY = e.offsetY;
    currentDiv = e.target;
  }
});

interactivePanel.addEventListener("mousemove", function (e) {
  if (move) {
    currentDiv.style.top =
      e.clientY - offsetY - generateButton.offsetHeight + "px";
    currentDiv.style.left = e.clientX - offsetX + "px";
  }
});

interactivePanel.addEventListener("mouseup", function (e) {
  move = false;
});

function generateElement() {
  let div = document.createElement("div");
  div.classList.add("interactiveElement");
  let maxLeft = window.innerWidth - 50;
  let maxTop = window.innerHeight - 150;
  div.style.top = getRandomValue(maxTop) + "px";
  div.style.left = getRandomValue(maxLeft) + "px";
  div.style.backgroundColor = getRandomColor();
  return div;
}

function getRandomColor() {
  var letters = "0123456789ABCDEF";
  var color = "#";
  for (var i = 0; i < 6; i++) {
    color += letters[getRandomValue(16)];
  }
  return color;
}

function getRandomValue(max) {
  return Math.floor(Math.random() * max);
}

```

## Education:
**National Aerospace University «Kharkiv Aviation Institute».**
 Metrology
 
## Languages:
 * **Ukrainian**
 * **English B1**
 * **Russian**

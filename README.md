# UI Events
![Wireflow](https://github.com/M4TThys123/SPRINT-7-UI-Events/blob/main/assets/ui-states.JPG)

## Beschrijving
Gedurende deze opdracht heb ik geleerd hoe je verschillende eventListeners kan gebruiken voor UI interacties met de gebruiker.

## JavaScript code:
```javascript

// Define Elements
const buttons = document.querySelectorAll('a');
let mousedownTimer;

// Loop trough all buttons
buttons.forEach(button => {

    // Add single click event listener
    button.addEventListener('click', function() {
        button.classList.add('color-green');  
    });

    // Add double click event listener
    button.addEventListener('dblclick', function() { 
        button.classList.add('color-purple');
    });

    // Add keydown event listener
    button.addEventListener('keydown', function(e) {
        if (e.code == 'KeyZ') {
            button.classList.add('color-lightpurple');
        }
     });

    // Add mousedown event listener
     button.addEventListener('mousedown', function() {
         mousedownTimer = setTimeout(() => {
            button.classList.add('color-green')
     }, 1500);
    });
})
```




![GNU GPL V3](https://www.gnu.org/graphics/gplv3-127x51.png)

This work is licensed under [GNU GPLv3](./LICENSE).

# CPNT-262-achievement-7
## By: Edgar Caballero
<br>

### Attributions:
- [Build a Product Card Parallax using VueJS by: Tyler Potts](https://www.youtube.com/watch?v=xrqI4rXW3dM&t=468s)
- [Codepen for the Card design and animations by: Curtis Lee](https://codepen.io/that_boy_curt/pen/mdbvxoW?editors=0110)
- [Word-Spacing property for the card animation by: W3schools](https://www.w3schools.com/cssref/pr_text_word-spacing.asp)
- [Jessica's "vue-component-activity](https://github.com/Enyorose/vue-component-activity)

### Reflections:
- Moved the “assets” folder inside the components folder. I felt that it looked better inside the “components” since everything “App.vue”  imported(referenced?)  is in that folder. 
- I wanted to just use one component for my card and cram as much as I could into each component. From "App.vue" I used v-binds to change the template syntax of my components.
    - Probably shouldve just used v-for isntead of inserting each "Card" slot individually into "App.vue"

### Troubleshooting:
 - I had trouble targeting the components when i was styling them in “App.vue” especially the footer. It would overlap the content when the screen size got smaller. 
  - Usually I would set these parameters:

```
body {
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: column;
  min-height: 100%;
}
html {
  height: 100%;
}

.footer {
  margin-top: auto;
}
```

 - Since the bodyof the html was a flexbox the footer would usually stick to the bottom of the page
 - In the end I had to use these parameters for my footer component, "ChildFooter.vue" to make it stick to the bottom:
 ```
  position: absolute;
  bottom: 0;
 ```
 - Although, it still overlaps the content in a smaller screen
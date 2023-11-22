# Frontend Mentor - Intro component with sign up form solution

This is a solution to the [Intro component with sign up form challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/intro-component-with-signup-form-5cf91bd49edda32581d28fd1). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page
- Receive an error message when the `form` is submitted if:
  - Any `input` field is empty. The message for this error should say _"[Field Name] cannot be empty"_
  - The email address is not formatted correctly (i.e. a correct email address should have this structure: `name@host.tld`). The message for this error should say _"Looks like this is not an email"_

### Screenshot

![](./screenshot.jpg)

Add a screenshot of your solution. The easiest way to do this is to use Firefox to view your project, right-click the page and select "Take a Screenshot". You can choose either a full-height screenshot or a cropped one based on how long the page is. If it's very long, it might be best to crop it.

Alternatively, you can use a tool like [FireShot](https://getfireshot.com/) to take the screenshot. FireShot has a free option, so you don't need to purchase it.

Then crop/optimize/edit your image however you like, add it to your project, and update the file path in the image above.

**Note: Delete this note and the paragraphs above when you add your screenshot. If you prefer not to add a screenshot, feel free to remove this entire section.**

### Links

- Solution URL: https://github.com/vernonroque/intro-signup-form.git
- Live Site URL: https://introduction-signup-form.netlify.app/

## My process

1. I first created the outline and structure in html.
   -I made sure to create the structure first. I then started doing the
   css styling to organize
2. Next, I started doing the CSS styling
   - I used flexbox to position the containers. I also used flexbox to organize
     the form header and the actual form
   - I designed the layout with a desktop screen in mind
3. I added functionality with javascript
   - I made sure the form would produce the errors if a user didn't fill in one of the
     inputs.
4. I styled the design in CSS for a mobile responsive design

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Javascript
- Flexbox
- Desktop-first workflow

### What I learned

1. I learned its best not to use '100vh' when defining the height of a container.
   -The reason: It causes overflow problems. When the height is fixed, and the content
   needs to act responsively, the content sometimes spills out of the container and
   causes unexpected overflow problems. I think the only time ill define a height is
   for landing page images and the header at the top of a webpage

DONT DO:

```css
body {
  height: 100vh;
}
.main {
  height: 100vh;
}
```

2. I learned a lot about how to submit the form. There's two ways.
   - You can add a 'submit' event listener to the form, and then handle the data
     your liking
   - You can add a 'click' event listener to the button inside the form, and then
     handle the data to your liking

```js
form.addEventListener('submit',(e)=> {
  ...
}
or

submitButton.addEventListener('click', (e)=>{
  ...
})
```

3. I learned how to access the class attribute of a tag

- I need to access the class attribute from each input. I needed to do this
  for validating each field

```js
inputFields.forEach((input) => {
  const className = input.className;
});
```

4. I learned how to access any attribute of a tag element
   -I had to access the "name" attribute for each input field to display the
   error messages appropriately

```js
inputFields.forEach((input) => {
  const inputNameAttribute = input.getAttribute("name");
});
```

If you want more help with writing markdown, we'd recommend checking out [The Markdown Guide](https://www.markdownguide.org/) to learn more.

**Note: Delete this note and the content within this section and replace with your own learnings.**

### Continued development

Use this section to outline areas that you want to continue focusing on in future projects. These could be concepts you're still not completely comfortable with or techniques you found useful that you want to refine and perfect.

**Note: Delete this note and the content within this section and replace with your own plans for continued development.**

### Useful resources

- [Example resource 1](https://www.example.com) - This helped me for XYZ reason. I really liked this pattern and will use it going forward.
- [Example resource 2](https://www.example.com) - This is an amazing article which helped me finally understand XYZ. I'd recommend it to anyone still learning this concept.

**Note: Delete this note and replace the list above with resources that helped you during the challenge. These could come in handy for anyone viewing your solution or for yourself when you look back on this project in the future.**

## Author

- Website - [Add your name here](https://www.your-site.com)
- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/yourusername)
- Twitter - [@yourusername](https://www.twitter.com/yourusername)

**Note: Delete this note and add/remove/edit lines above based on what links you'd like to share.**

## Acknowledgments

This is where you can give a hat tip to anyone who helped you out on this project. Perhaps you worked in a team or got some inspiration from someone else's solution. This is the perfect place to give them some credit.

**Note: Delete this note and edit this section's content as necessary. If you completed this challenge by yourself, feel free to delete this section entirely.**

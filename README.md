```
/* Normalize Css  */
/*
Used for cross browser consistencey for default or previously made set up. To set up this css, if we are using npm, we can just install normalize css. If We are using the react.js then we need to just import normalize css in our index.js or app.js. As we are working on html and css only, so we have to download it. To download, go to the following web adress,

      https://necolas.github.io/normalize.css/

We Can use the normalize css in two ways. One is to create new file for this particular css. Another one is we should have paste the entire css code in our main css. But we have to keep in mind that, we must have paste the normalize css code first than the other styles. That means, all the styles must be later of the normalize css codes.

Now we are going to create a new normalize css file in our case. Here, one more thing we have to keep in our mind that, we have to use the normalize css link above the main css file of our project.  */


/* normalize css dont do anything with the box sizing. That's why we have to assign the value of it manually. We will do that for all the element including pseudo after and before element. */

*, ::after, ::before{
  box-sizing: border-box;
  /* This will help us while we are going to add padding, then the width is not going to be bigger.  */
}

/* Font's */
/* To select font's we have two alternative at this moment. Those are,
1. fontpair.co
2. https://www.pagecloud.com/blog/best-google-fonts-pairings

Now go to below font's and typography section to know more about fonts.
 */
@import url('https://fonts.googleapis.com/css?family=Lexend:400');

html {font-size: 100%;} /*16px*/

:root{
  /* primary */
  /* Collect those shade of the colors use the following site,
  1. https://noeldelgado.github.io/shadowlord/#73fdad
  */
  --primary_100: #e7cdd8;
  --primary_200: #d09bb1;
  --primary_300: #b8688b;
  --primary_400: #a13664;
  --primary_500: #89043d;
  --primary_600: #6e0331;
  --primary_700: #520225;
  --primary_800: #370218;
  --primary_900: #1b010c;

  /* grey */
  /* To have the grey colors shade we have can go for the privious primary color finding way. Or simply we can go to bootstrap or tailwindcss. These two platform do have a great resources for doing such color related tasks. Here, we have three options.
  1. https://getbootstrap.com/docs/5.0/customize/color/#color-sass-maps
  2. https://tailwindcss.com/docs/customizing-colors#color-palette-reference  */
  --grey_50:  #fafafa;
  --grey_100: #f4f4f5;
  --grey_200: #e4e4e7;
  --grey_300: #d4d4d8;
  --grey_400: #a1a1aa;
  --grey_500: #71717a;
  --grey_600: #52525b;
  --grey_700: #3f3f46;
  --grey_800: #27272a;
  --grey_900: #18181b;

  /* Other color variables */
  /* These variables can be anything you want. But it is recommended to have those for better view. To chose these colors manually we can use the following website. Hope it will work fine,
  1. https://www.happyhues.co/
  */
  --black: #222;
  --white: #fff;
  --red_light: #f8d7da;
  --red_dark: #842029;
  --green_light: #d1e7dd;
  --green_dark: #0f5132;

  /* Fonts or Typography */
  /* After Choosing a font, than go to the following site for styling font size on body and heading and grab the css and post it here in main css file.
  1. type-scale.com

  Here the code line 26 (@import) to line 143 (small, text_small selectors end) is from the type-scale.com site. Not all of them but all the font and typography part are from this site.

  After that all the other variables, properties and values are found from the other resources. Resources are mentioned beside to the particular property value or variables. */
  --headerFont: 'Lexend', sans-serif;
  --BodyFont: 'Lexend', sans-serif;
  --smallFont: 0.7em;

  /* Other variables */
  /* These other variables are for better access to our doc and editing or coding ability. Those will increase our productivity and will save huge time. */
  --backroundColor: var(--grey_50);
  --textColor: var(--grey_900);
  --borderRadius: 0.25rem;
  --letterSpacing: 1px;
  --transition: 0.3s ease-in-out all;
  --maxWidth: 1120px;
  --fixedWidth: 600px;

  /* Box Shadow */
  /* This box shadow code can be found from the following tailwindcss website,
  1. https://tailwindcss.com/docs/box-shadow */

  /* As small shadow either we use first or second.  */
  --boxShadow_1: 0 1px 3px 0 rgb(0 0 0 / 0.1), 0 1px 2px -1px rgb(0 0 0 / 0.1);
  --boxShadow_2: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);

  /* As for hovering over use either third or fourth. */
  --boxShadow_3: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
  --boxShadow_4: 0 20px 25px -5px rgb(0 0 0 / 0.1), 0 8px 10px -6px rgb(0 0 0 / 0.1);

}

body {
  /* Using the primary and grey color in the the specific element is one type of use. It has some problem, we have to change it manually every time whenever we need. There is another way to do so, it is having the specific element and the color variable in the root element which will be applied for all the element in the entire project.  */
  background: var(--grey_50);
  font-family: var(--BodyFont)
  font-weight: 400;
  line-height: 1.75;
  color: var(--grey_900);
}

p {
  margin-bottom: 1.5rem;
  max-width: 40em;
}

h1, h2, h3, h4, h5 {
  margin: 0;
  margin-bottom: 1.38rem;
  font-family: var(--headerFont);
  font-weight: 400;
  line-height: 1.3;
  text-transform: capitalize;
}

h1 {
  margin-top: 0;
  font-size: 3.052rem;
}

h2 {font-size: 2.441rem;}

h3 {font-size: 1.953rem;}

h4 {font-size: 1.563rem;}

h5 {font-size: 1.25rem;}

small, .text_small{
  var(--smallFont)
}

/* Link */
a{
  text-decoration: none;
}

/* Unordered list */
ul{
  list-style-type: none;
  padding: 0;
}

/* Image default styling and sizing */
.imageContainer{
  width: 40vh;
  border: 5px solid var(--primary_500);
  border-radius: var(--borderRadius);
  max-width: var(--maxWidth);
}

.image{
  width: 100%;
  /* Once again, if we want have height in the previous imageContainer we must have assign the value for the image class with height of 100%. Otherwise there will be some empty or white space in the image. Which is so ugly. */
  display: block;
  object-fit: cover;
  /* This object fit property is to adjust the aspect ratio of the image. Otherwise, some of image part may be remain missing.  */
}

/* Buttons */
.btn{
  cursor: pointer;
  color: var(--white);
  background-color: var(--primary_500);
  border: transparent;
  border-radius: var(--borderRadius);
  letter-spacing: var(--letterSpacing);
  padding: 0.375rem 0.75rem;
  box-shadow: var(--boxShadow_1);
  transition: var(--transition);
  text-transform: capitalize;
  display: inline-block;

  /*
  This property will be used while needed
  display: block;
  width: 200px;
  margin: 0 auto; */
}

.btn:hover{
  background: var(--primary_700);
  box-shadow: var(--boxShadow_3);
}

.hipster_btn{
  color: var(--primary_500);
  background: var(--primary_200);
}

.hipster_btn:hover{
  color: var(--primary_200);
  background: var(--primary_700);
}

.btn_block{
  width: 100%;
}

/* Alert's */
.alert{
  padding: 0.375rem 0.75rem;
  margin: 1rem;
}

.alert_danger{
  color: var(--red_dark);
  background: var(--red_light);
}

.alert_success{
  color: var(--green_dark);
  background: var(--green_light);
}

/* Forms */
.form{
  width: 90vw;
  background: var(--white);
  max-width: var(--fixedWidth);
  border-radius: var(--borderRadius);
  box-shadow: var(--boxShadow_2);
  padding: 2rem 2.5rem;
  margin: 3rem auto;
}

.form_label{
  display: block;
  font-size: var(--smallFont);
  margin-bottom: 0.5rem;
  text-transform: capitalize;
  letter-spacing: var(--letterSpacing);
}

.form_input, .form_textarea{
  width: 100%;
  padding: 0.375rem 0.75rem;
  border-radius: var(--borderRadius);
  background: var(--backroundColor);
  border: 1px solid var(--grey_200)
}

.form_row{
  margin-bottom: 1rem;
}

.form_textarea{
  height: 7rem;
}

::placeholder{
  font-family: inherit;
  color: var(--grey_400);
}

/* Form alert */
.form_alert{
  color: var(--red_dark);
  letter-spacing: var(--letterSpacing);
  text-transform: capitalize;
}

/* Loading sign */
@keyframes spinner{
  to{
    transform: rotate(360deg);
  }
}
.loading{
  width: 6rem;
  height: 6rem;
  border: 5px solid var(--primary_100);
  border-radius: 50%;
  border-top-color: var(--primary_500);
  animation: spinner 0.5s linear infinite;
  margin: 0 auto;
}

/* Section Title */
.title{
  text-align: center;
}

/* If we don't need such a title or margin we can easily remove it by calling the element. */
.title h2{
  /* margin: 0; */
  /* Again, we can change it, anything we want. Or we can have a property and value in the title_underline to remove the margin. The code is,

  margin-top: -1rem;

  There is no difference between margin: 0; here and margin-top: -1rem there. That's all.
   */
}
.title_underline{
  background: var(--primary_500);
  width: 7rem;
  height: 0.25rem;
  margin: 0 auto;
  margin-top: -1rem;
}

```

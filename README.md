# fylo-dark-challenge

![Desktop HD](https://user-images.githubusercontent.com/16800201/155210669-51739b80-e6a3-45a8-84ed-099d6cffbb18.png)


# Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Why I like SASS](#why-i-like-sass)
* [Setup](#setup)

# General info
As the name suggests, I did this as a [Frontend Mentor](https://www.frontendmentor.io/challenges) challenge. I personally believe the best way to practice your web development skills is to practice with projects and challenges. This design has some nice layout challenges in it. A perfect training ground to practice your Flexbox and Grid skills. Since this is a fully responsive development challenge, I also made use of media queries. I added breakpoints at the phone, tablet (additionally added -- not part of the challenge) and desktop sizes.

This gave me the opportunity to replicate designs just from a picture. It is a great way to work independently, in case we don't work with exact specifications or designs.

# Technologies
Project is built with:
- HTML5 
- SASS (CSS pre-processor)
- Flexbox
- CSS Grid
- Mobile-first workflow (Media Queries)

# Why I like SASS
I like to use SASS as it makes writing css super convenient. It provides many additional features on Vanilla CSS (used in the project), like:

### Nesting
I use nesting almost throughout the whole document as it saves time and prevents errors.

```scss
nav{
        display: flex;
        justify-content: space-between;
        align-items: center;
        color: $font-color;
        font-family: $font-stack-primary;
        padding-bottom: 2.5em;
        a{
            font-size: .9rem;
            color: $font-color;
            text-decoration: none;
        }
      }
 ``` 
 The same thing in CSS translates to:
 ```css
 .wrapper nav {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: justify;
      -ms-flex-pack: justify;
          justify-content: space-between;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
  color: white;
  font-family: Raleway;
  padding-bottom: 2.5em;
}

.wrapper nav a {
  font-size: .9rem;
  color: white;
  text-decoration: none;
}
```
### Variables
I use a separate variables file (```_variables.scss```) to have my variables in one place. I usually make variables out of components/styles that are referenced often. This also allows me to make global changes (eg: editing the colour/style scheme) extremely efficiently.

```scss
//Fonts
$font-stack-primary: Raleway;
$font-stack-secondary: Open Sans;

//Background colours
$bg-email: hsl(217, 28%, 15%);
$bg-main: hsl(218, 28%, 13%);
```
### Modules
Just like JS modules, we don't need to write all code in one scss file. I use a separate file for variables which I then import in:
```scss
@import '_variables';
```

Another important feature is Mixins (not used here) which lets us make groups of CSS declarations that we want to reuse throughout your site.


# Setup
If you use Node.js, you can also install Sass using npm by running:

```
$ npm install -g sass
```

If you use the [Homebrew](https://brew.sh/) package manager for Mac OS X or Linux, you can install Dart Sass by running:

```
$ brew install sass/sass/sass
```
Once you are done, you can download the [Live SASS Compiler](https://marketplace.visualstudio.com/items?itemName=ritwickdey.live-sass) extension in VSCode to watch your SCSS files (converting them to CSS).

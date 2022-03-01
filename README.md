# CloseCuts


## Introduction

This is a non-transactional website for a Salon Academy. On this website the user can find out more about the Academy and book an appointment with the Salon. The website is responsive so users can view the site and book appointments on mobile and tablet devices, while on the go. 

![image](/docs/images/i-am-responsive-screenshot.png)

------

## Accessibility

I’ve added ARIA attributes to all links on the page with text information. This is to help disabled users understand what the links are and their purpose. 

I’ve used Symantic HTML markup which helps browsers to understand the context of the content, and also helps with the accessibility for users with impairments.

I’ve used `role` and `alt` Attributes on all the background images to explain what the images are.

------

## Accessibility Score: Google Lighthouse Test

The site ran through Google Lighthouse for Desktop and Mobile:

### Desktop Scores:

![image](/docs/images/google-lighthouse-test-desktop.png)

### Mobile Scores:

![image](/docs/images/google-lighthouse-test-mobile.png)

------

## SEO (Search Engine Optimisation)

I've added `meta data` and a `title` to the .html pages. This helps Search engines like Google when looking for matches based on what the user searches for. 

I added a `description`, `keywords` and `author`. Search Engines will display the title and description information in their search results.

------

## Features List

### 1. Booking Form Call to Action Buttons

The user has the option to book an appointment from the navigation when they are at the top of the page, or at the middle when they start scrolling down to browse.
![image](/docs/images/feature-booking-form-cta-buttons.png)


### 2. Intuitive Booking Form

On the Booking Form Page, there is an intuative booking form for the user to fill out when they want to book an appointment.

The form includes a `date selector` and `time selector` so the user can specify when they want to come in for the hair cut.

The form is also `responsive` so yu user can book an appointment while out and about on mobile and tablet devices.

![image](/docs/images/feature-booking-form.png)

### 3. Contact Us Anchor Button

The Contact Us details are below the browser fold. I've used an `anchor element` on the button so the user is automatically scolled down to the contact us section on the homepage, should the user want to get in touch with the salon.

![image](/docs/images/feature-contact-us-anchor-button.png)


### 4. Hover State on Buttons

All the button on the site have a `uniformed hover state` interaction so it's clear for the user that the buttons are clickable.

![image](/docs/images/feature-hover-state-buttons.png)

------

## Testing

### Responsive Testing

I have tested that the site is responsive by applying specific styles for different `CSS breakpoints`

#### Breakpoints used for mobile devices:

1. `max-width: 350px` 
2. `max-width: 320px`
3. `max-width: 450px`

#### Breakpoints used for tablet devices:

1. `max-width: 914px`
2. `max-width: 916px`

I used the Chrome inspect element to check the different CSS breakpoints.


### Booking From Data Submission

I've tested the booking form and user data is submitted succesfully.
![image](/docs/images/testing-booking-form-data-submission.png)

### Form Validation

I've tested the validation on the booking form so the user cannot submit the form unless all fields have been filled out. The prevents missing information that is needed to make the booking.
![image](/docs/images/testing-form-validation.png)

### Accessibility

I used the `Chrome Screen Reader Extention` to test that the site is accessibility friendly.

![image](/docs/images/testing-screen-reader.png)

### Bugs encountered during testing

1. The transparent background for the form was not showing.
I checked the code and saw that there was a space between `rgba` and the `values`.

Incorrect: `background: rgba (0, 0, 0, 0.5);`

Correct: `background: rgba(0, 0, 0, 0.5);`

![image](/docs/images/bug-1.png)

2. The date and time selector icons were not using the applied CSS styles. I have to override the styles and apply directly. The icons seem to be gererated by the browser. They were not from a third-party library.

![image](/docs/images/bug-2.png)

Using the syntax below allowed me to override the styles for the default icons:
```
input[type="date"]::-webkit-calendar-picker-indicator{
   background-color:white;
}
 
input[type="time"]::-webkit-calendar-picker-indicator{
   background-color:white;
}
```

3. Mobile  - Navigation buttons were not aligned and not in order.
	This took a lot of back and forth in changing styles for the `header`, `navigation` and the `li` elements.

![image](/docs/images/bug-3.png)

4. The ‘Book an Appointment’ button on the homepage was partially hidden on mobile view.
First I increased the height on `#homepage-block-one` and then updated the padding on `#homepage-block-one p`

![image](/docs/images/bug-4.png)


## HTML and CSS Code Validation

Both the W3C Markup HTML Validator and W3C CSS Validator were used to to confirm there are no errors in the codebase.

![W3C Markup Validator Report](https://validator.w3.org/nu/?doc=https%3A%2F%2Fkslg.github.io%2Fpp1-closecuts%2Findex.html)

![image](/docs/images/w3c-markup-validation.png)


![W3C CSS Validator Report](https://jigsaw.w3.org/css-validator/validator?uri=https%3A%2F%2Fkslg.github.io%2Fpp1-closecuts%2Findex.html&profile=css3svg&usermedium=all&warning=1&vextwarning=&lang=en#css)

![image](/docs/images/w3c-css-validation.png)



------

## Release History

We continually tweak and adjust this template to help give you the best experience. Here is the version history:

**September 1 2021:** Remove `PGHOSTADDR` environment variable.

**July 19 2021:** Remove `font_fix` script now that the terminal font issue is fixed.

**July 2 2021:** Remove extensions that are not available in Open VSX.

**June 30 2021:** Combined the P4 and P5 templates into one file, added the uptime script. See the FAQ at the end of this file.

**June 10 2021:** Added: `font_fix` script and alias to fix the Terminal font issue

**May 10 2021:** Added `heroku_config` script to allow Heroku API key to be stored as an environment variable.

**April 7 2021:** Upgraded the template for VS Code instead of Theia.

**October 21 2020:** Versions of the HTMLHint, Prettier, Bootstrap4 CDN and Auto Close extensions updated. The Python extension needs to stay the same version for now.

**October 08 2020:** Additional large Gitpod files (`core.mongo*` and `core.python*`) are now hidden in the Explorer, and have been added to the `.gitignore` by default.

**September 22 2020:** Gitpod occasionally creates large `core.Microsoft` files. These are now hidden in the Explorer. A `.gitignore` file has been created to make sure these files will not be committed, along with other common files.

**April 16 2020:** The template now automatically installs MySQL instead of relying on the Gitpod MySQL image. The message about a Python linter not being installed has been dealt with, and the set-up files are now hidden in the Gitpod file explorer.

**April 13 2020:** Added the _Prettier_ code beautifier extension instead of the code formatter built-in to Gitpod.

**February 2020:** The initialisation files now _do not_ auto-delete. They will remain in your project. You can safely ignore them. They just make sure that your workspace is configured correctly each time you open it. It will also prevent the Gitpod configuration popup from appearing.

**December 2019:** Added Eventyret's Bootstrap 4 extension. Type `!bscdn` in a HTML file to add the Bootstrap boilerplate. Check out the <a href="https://github.com/Eventyret/vscode-bcdn" target="_blank">README.md file at the official repo</a> for more options.

------

## FAQ about the uptime script

**Why have you added this script?**

It will help us to calculate how many running workspaces there are at any one time, which greatly helps us with cost and capacity planning. It will help us decide on the future direction of our cloud-based IDE strategy.

**How will this affect me?**

For everyday usage of Gitpod, it doesn’t have any effect at all. The script only captures the following data:

- An ID that is randomly generated each time the workspace is started.
- The current date and time
- The workspace status of “started” or “running”, which is sent every 5 minutes.

It is not possible for us or anyone else to trace the random ID back to an individual, and no personal data is being captured. It will not slow down the workspace or affect your work.

**So….?**

We want to tell you this so that we are being completely transparent about the data we collect and what we do with it.

**Can I opt out?**

Yes, you can. Since no personally identifiable information is being captured, we'd appreciate it if you let the script run; however if you are unhappy with the idea, simply run the following commands from the terminal window after creating the workspace, and this will remove the uptime script:

```
pkill uptime.sh
rm .vscode/uptime.sh
```

**Anything more?**

Yes! We'd strongly encourage you to look at the source code of the `uptime.sh` file so that you know what it's doing. As future software developers, it will be great practice to see how these shell scripts work.

---

Happy coding!

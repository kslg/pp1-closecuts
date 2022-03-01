<h1 align="center">CloseCuts</h1>


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

<a href="https://validator.w3.org/nu/?doc=https%3A%2F%2Fkslg.github.io%2Fpp1-closecuts%2Findex.html" target="_blank">W3C Markup Validator Report</a>

![image](/docs/images/w3c-markup-validation.png)

<a href="https://jigsaw.w3.org/css-validator/validator?uri=https%3A%2F%2Fkslg.github.io%2Fpp1-closecuts%2Findex.html&profile=css3svg&usermedium=all&warning=1&vextwarning=&lang=en#css" target="_blank">W3C CSS Validator Report</a>

![image](/docs/images/w3c-css-validation.png)

------

## Deployment

The site was published via Github Pages. You can see the site live 
<a href="https://kslg.github.io/pp1-closecuts/index.html" target="_blank">here</a>.

------

## UX Planning

I used the 5 Planes of UX to provide a conceptual framework. 

### The Strategy Plane

#### Mission Objectives / The What:

- Low Cost, Affordable service for members of the public.
- Stylish establishment.
- Not compromising on quality.
- Book Appointments online.

#### The Why:
- Where students gain the experience to be qualified hairdressers.
- Students earn and learn.
- Engage with the community.
- Provide a public service.

### Ideas & Inspiration Mind Map
![image](/docs/images/mind-map-image.png)

### Demographic
- Target Audience between: 16 years - 35 years
- O.A.Ps Welcome
- All genders Welcome.

### Colour Palette Ideas
- High colour contrast for better accessibility and clear communication.
![image](/docs/images/colour-palette-ideas.png)

### Content Strategy
- Information on the mission: Why we are doing this
- Book an appointment
- Store Location
- Opening Times

### Typography
Fonts selected are `Asap` and `Asap Condensed` from Google Fonts which are clear and easy to read. https://fonts.google.com/

![image](/docs/images/typography-screenshot.png)

---

## The Scope Plane

### Functional Requirements

1. Problem: Customers need to book an appointment using an easy online form.

   Solution: To build an Online Booking Form that can be accessed and filled out on desktop and responsive devices. 

2. Problem: 
- So the customer does not think the site is frozen, not working.
- To make the banner content more attractive.

   Solution: Zoom behaviour on the Hero Image

3. Problem: The users have to scroll all the way to the top to use the navigation to through the site.

   Solution: Make the Navigation ‘sticky’ so it’s position is always fixed at the top.

4. Problem: Making Customers understand the culture and what the CloseCuts is about.
	
   Solution: Present and image gallery showing customer experiences.

### Content Requirements

- This is a static content site with no regular updates required. 
- Content is easy to maintain via HTML/CSS and upscaled if needed. 
- Content on the site will be a mix of copy/text, images and forms.
- Video content can als0 be added.

### Interaction Design

All Links and CTA (Call to Action) buttons will change colour to let the customers know that the buttons and links are clickable. 

So that copy text does not take up too much real estate on the site, content can be partially hidden and a `Read More` button can be clicked to reveal more content. 

### Scope of MVP

Using the `MoSCoW prioritisation method` which is used in Agile project delivery to outline the importance of each requirement and what needs to be delivered in the MVP.

#### MoSCoW Definition:
![image](/docs/images/moscow-requirements-screenshot.png)

---
## The Structure Plane

### Site Architecture
- Easy Navigation allows the user to get to their destination in less than three clicks.
- Sticky Navigation allows easy access to other main pages.

---

## The Skeleton Plan

### Header
- Grey background.
- Black Text in a yellow/gold box.
- Hover States: White text.

 Example:

 ![image](/docs/images/header-cta-states-wireframe.png)

### Footer

- Grey background.
- White Text.
- Yellow/Gold Icons.

Example:

![image](/docs/images/footer-wireframe.png)

## CTA Buttons
Non-clicked State: 
- Yellow text box
- Black text

Hover State:
- Yellow text box
- White text

![image](/docs/images/hover-state-buttons-wireframe.png)

## Colour Palette:

![image](/docs/images/colour-palette-wireframe.png)

## Iconography:
All icons to be in Dark Yellow:

![image](/docs/images/social-icons-wireframe.png)

--- 

## The Surface Plane / Final Concept

### Homepage

### Con



------

### Credits / Borrowed Resources / Tools

Balsamic

W3C


------

### Descoped Requirements / Future Enhancements
- Some requirements had to be descoped from the project due to time contraints. 
- Descoping is a process which is part or Agile Project Management, and can be requirements that are brought back into a sprint or project at a later date.

1. Sticky Navigation.
2. Read More funtionality.
3. Content Layout as seen in the Final Concept designs.
4. Image Gallery Page.
5. Contact Us Page.


------

### Unfixed Bugs

------

<p align="center">End of document.</p>
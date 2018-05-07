# htrml300 Assignment 4

## Design1-Header.png
In Desgn1, the most important aspect is the curved division between header image and content below. 

![First design image](https://james1992.github.io/html300-assignment4/images/Design1-Header.png)

### Will it take a little, lot, or absurd amount of work to build this feature/design?

To implement a curved design that mimics the above design header one would need to spend a moderate amount of time working with scalar vector graphics (svg).  With an SVG file it is possible to replicate the curved design by using styling similar to that on CSS tricks (https://css-tricks.com/creating-non-rectangular-headers/).  The coding required to implement their examples is relatively minor and easy to reproduce but if you have not worked with svg before there will be initial learning curve that you need to overcome.  The same as there is for any other element of web design.

In addition, it would take time to produce the desired output since the curves go each way (meaning that on one half there is mostly header and on the other mostly white space).  But it is very doable with a moderate amount of effort.


### Are there other options for similar result with less work?

Another option to replicate the above output header is to format the image in a photo editing software first (e.g. PhotoShop or GIMP) with the curved design.  That formatted image could then be loaded into the website to replace the rectangular image that was used previously.  Depending on your experience with photo editing this might be a much faster approach to implement the design.  If you have not used GIMP or PhotoShop extensively then the svg approach would likely be easier.

### Is it a good development choice? Do you have any concerns with it?

I think it is a good design choice, it does not hinder the users ability to navigate the site and it is a catchy design which gives it visual appeal.  The only issue I could see with the design is that it adds a lot of unused white space to the page but that seems to a minor issue.

### What would be the first dev step you would try when building? Ex: “Add border radius to curve the edges” or “Something with SVGs”. This doesn't have to be terribly specific, just do your best. 

1. Setup an svg tag in html to hold the header image.
2. add the picture as the background image to the svg portion of the page.
3. add the inverse of a white circle to the left side of the page and a white circle to the right to block out the desired portions of the header.
4. refine the svg graphics until you are happy with the look of the header.

## Design2-Signup01
In Design2, the "Indoors" and "Outdoors" buttons will submit the form.

![Second design image](https://james1992.github.io/html300-assignment4/images/Design2-Signup01.png)

### Will it take a little, lot, or absurd amount of work to build this feature/design?

Designing the page above so that both indoors and outdoors buttons submit the form should require very little work to implement*.  At the most basic level it would involve copying the onclick call from one button to the other so that they both would operate in the same manner.  Likely this is not the desired effect because the two buttons confer two very different choices.  It is likely they have the same form handler but that each button would pass in a variable to indicate which one was pressed and that would influence the behavior of the form handler.

* This assumes that the JavaScript form handler is already implemented.  If that is not yet implemented then this would likely take a lot of work depending on the complexity of the script.

### Are there other options for similar result with less work?

I do not see any easier way to implement this design because all the developer needs to do is copy and paste an onclick event from one button to the other.  That should require less than a minutes worth of effort.

### Is it a good development choice? Do you have any concerns with it?

I do not think that this is a good design choice because it is not obvious to the user that clicking on either button will launch the form handler on their inputs.  It is possible that the user of the form does not fill out the information from the top down and clicks on either of the "submit" buttons first before filling out their name or email.

A better way to implement this element is to add a "Submit" to the page that way there should be no confusion over when the form will be submitted.

### What would be the first dev step you would try when building? Ex: “Add border radius to curve the edges” or “Something with SVGs”. This doesn't have to be terribly specific, just do your best. 

1. Add an onclick event to one of the two buttons.
2. Set the event to launch the form handler code in JS.
3. Add any parameters to the function call that need to be passed into the form handler. 
4. Copy and paste the onclick event to the other button and update the parameters if needed.

## Design3-Signup02
Don't miss the note from designer in Design3.

![Third design image](https://james1992.github.io/html300-assignment4/images/Design3-Signup02.png)

### Will it take a little, lot, or absurd amount of work to build this feature/design?

This is something that would take a lot of work to implement and requires the use of JavaScript, see the second answer on Stack Overflow (https://stackoverflow.com/questions/12381563/how-to-stop-browser-back-button-using-javascript) a working example of which can be found here: (http://output.jsbin.com/yaqaho#!).  However this is attempting to override the default behavior of the browser and as a result may not work in future releases of web browsers or it may work in some but not others.  From testing the live output the implementation works as requested.  The user is unable to go back with the back button and the contents of the page are not lost when they click back.

The above implementation should allow the user to navigate forward and back with the form buttons as the code should not impact that part of the page.

### Are there other options for similar result with less work?

The other option that is much easier to implement is the first answer in the above stack overflow page.  The implementation is to instead prompt the user with a warning when they click the back button to firm that is what they want to do because doing so will cause them to lose their progress and data.

### Is it a good development choice? Do you have any concerns with it?

No disabling the back button is poor choice because the page is attempting to circumvent the browser design and implement a page design that is foreign to the user. The user expects the back button to work as intended and if it does not they will be come frustrated and confused.  Confusion is the last thing you want when someone is filling out your web form.  

For that reason the better approach is to instead of disabling the back button is to add a warning message that informs the user of what will happen if they click back.  This is the approach used by webpages that do not want users clicking the back arrow.

### What would be the first dev step you would try when building? Ex: “Add border radius to curve the edges” or “Something with SVGs”. This doesn't have to be terribly specific, just do your best. 

1. Add a JavaScript file to hold the code required to override the back button
2. Ensure that the webpage hash does not change when the user clicks the back button
3. Use the function to deny the normal use of the back button
4. Copy whatever is left on the above example.
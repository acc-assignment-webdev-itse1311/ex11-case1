# NP HTML5, CSS3, and JavaScript 6e Tutorial 11, Case Problem 1

## Description
1.  Use your editor to open the bw_review_txt.html and bw_review_txt.js files from the html11 > case1 folder. Enter your name and the date in the comment section of each file, and save them as bw_review.html and bw_review.js respectively.
2.  Return to the bw_review.html file in your editor. Go to the document head and add a script element for the bw_review.js file. Load the file asynchronously.
3.  Take some time to study the contents of the file, paying close attention to the form elements and their IDs. Save your changes to the file.
4.  Return to the bw_review.js file in your editor. Directly after the initial comment section, insert an event handler that runs the init() function when the page is loaded by the browser.
5.  Create the init() function. The purpose of the function is to define the event listeners used in the page. Add the following commands to the function:
    a.  Declare the stars variable that stores an object collection of the reviewing stars, referenced by the span#stars img selector.
    b.  Loop through the star collection and for each star image in the collection change the cursor style to pointer and add an event listener to run the lightStars() function in response to the mouseenter event occurring over each star image.
    c.  After the for loop, add an event listener to the comment text area box that runs the update- Count() function in response to the keyup event. 
6.  Create the lightstars() function. The purpose of this function is to color a star when the user moves the mouse pointer over a star image in order to reflect the user's rating of the book. Add the following commands to the function:
    a.  Daniel has stored the rating value of each star image in the img element's alt attribute. Store the value of the alt attribute of the target of the event object in the starNumber variable.
    b.  Declare the stars variable containing the object collection referenced by the selector span#stars img.
    c.  Loop through the stars collection with an index ranging from 0 up to less than the value of the starNumber variable. Light every star in the collection by changing the src attribute of the star image to the bw_star2.png image file.
    d.  After the for loop, create another loop that loops through the stars collection with the index ranging from the value of the starNumber variable to less than 5. Unlight every star in this col- lection by changing the src attribute of the star image to the bw_star.png image file.
    e.  Change the value of the input box with the id attribute "rating" to starNumber stars, where starNumber is the value of the starNumber variable.
    f.  When the mouse pointer moves off a star image, the lit stars should be unlit. Add an event listener to the target of the event object that runs the turnOffStars() function in response to the mouseleave event.
    g.  If the user clicks the star image, the selected rating should be set, which means moving the mouse pointer off the star should not remove the rating. Add an event listener for the target of the event object that runs an anonymous function removing the turnOffStars() function from the mouseleave event.	
7.  Create the turnOffStars() function. The purpose of this function is to unlight the stars when the user moves the mouse pointer off the star images. Add the following commands to the function: 
    a.  Declare the stars variable containing the object collection referenced by the selector span#stars img.
    b.  Loop through all images in the stars collection and change the src attribute of each image to the bw_star.png file.
    c.  Change the value of the rating input box to an empty text string.
   8.  Create the updateCount() function that keeps a running total of the number of characters that the user has typed into the comment text area box. Add the following commands to the function:
   a.  Declare the commenfText variable that references the value stored in the comment text area box.
   b.  Use the countCharacters() function with commentText as the parameter value to calculate the number of characters in commentText. Store the value in the charCount variable.
   c.  Declare the wordCountBox that references the wordCount input box.
   d.  Change the value stored in the wordCount input box to the text string charCount/1000 where charCount is the value of the charCount variable.
   e.  If charCount is greater than 1000, change the style of the wordCount input box to a white font on a red background, otherwise set the style to a black font on a white background.	
9.  Document your work with descriptive comments throughout the file and save the script file.
10. Open bw_review.html in your browser. Verify that as you move your mouse pointer over the stars below the book description, the rating value automatically matches your selection. Also verify that moving the mouse pointer off the star images removes the rating unless you have clicked one of the stars. Finally, verify that as you type characters into the text area box, a running count of the character total is shown below the box and, if the number of characters exceeds 1000, the total is displayed in a white font on a red background.

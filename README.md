In this lab, we're going to start building a web based Tic Tac Toe game! The first step is to build the actual game board, and later you'll learn JavaScript, which will add the interactivity. So let's take a breath and focus on just styling some content. :)

Project Setup
Create a new a project folder for this lab and open it in VS Code.
Create an index.html and styles.css file.
Stub out the HTML file and add a <link> to the CSS file.
Building the Game Board (HTML)
So, we know that a Tic Tac Toe game has 9 possible squares that a player can place either an X or an O in. Think about how you might lay this out and give it a shot on your own before you continue.

Let's really think about the board in terms of borders. You probably already guessed that we're going to need 9 different elements to represent each move, but you might not think about the best way to lay those out in order to maximize our ability to use CSS efficiently to get the board looking right.

Create a <div> with an id of "board". This will be the container for our game board.
Add an <h1> into the #board div, and add the text content "Tic Tac Toe".
Nested within the #board div, add 3 <div>'s with a class of "row".
Within each .row <div>, add 3 more <div>'s.
The 3 <div>'s within each row (for 9 total) will be our squares where the player can place an X or O!
Now, you need a way to identify each square. Logically, it makes sense that we have left squares, right squares, top squares, middle squares, and bottom squares. So, let's add classes to identify each square.
For the first <div> in the first row, add a class for "top" and "left". Your <div> should look like this <div class="top left"></div>.
Now, we have a way to identify the top left square!
Also, stacking multiple class names on an element is a very common practice. You will use it a lot later with Bootstrap.
We need to add identifiers for all the other squares as well, so let's continue:
Add the classes "top" and "middle" for the next <div> in the first row, and hopefully, you see where this is going now.
For the third <div> in the first row, add "top" and "right" classes.
For the center row child <div>'s, use the class "center". You'll likely need a way to identify it differently than the outside <div>'s when we add interactivity with JavaScript.
Add the rest of the classes to the <div>'s in the middle and bottom rows.
Styling the Game Board (CSS)
Ok, so you've got your HTML, but it doesn't look like anything when you run it, right? Your screen should be completely blank because we've only put <div>'s on the screen so far. There is no content or borders, so nothing shows up.

We need to layout and style the game board. Let's get started.

Add 3rem worth of padding to the top of the #board div and center align the text.
Float left all of the <div>'s nested inside the rows (which represent the 9 cells of the game). Also, add a height and width of 100px.
Hint: you can do this with one selector that selects all of the child <div>'s nested within any element with the class .row.
Add a "clear fix" for all of the .row's.
When floating <div>'s, you need to let the browser know when floating should end. You do this with the clear CSS property.
Example property for the "clear fix": clear: both;.
Center and set the width of the .row's.
Hint: margin can be used to horizontally center use 0 and auto.
Set the width of each row to 302px. The extra 2px is for the 2 vertical borders on each .row that are 1px each, which we are about to add!
Create a class selector in your CSS for top, bottom, left, and right. Add the appropriate border side for each class.
.top example: border-bottom: 1px black solid
Think about the borders that certain cells share in common. In the example above, we added a bottom border to the .top cells because all of the top cells have a bottom border. Create the borders for the others.
We don't need styling for the .middle class, but we're going to leave it in our HTML. You'll understand why when we get to the JavaScript section of the game.
Hint: Change the black border color to a different color on each class selector to see exactly where your border is being placed.
Add a style to change the cursor to a pointer whenever a cell has a mouse hover over it.
That's it! You should see a nicely laid out Tic Tac Toe board whenever you open your page.

Now it's time to learn a little JavaScript so that you can bring your game to life!

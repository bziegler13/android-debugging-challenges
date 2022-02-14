# android-debugging-challenges
This lab consisted of 4 debugging challenges. 

The first challenge had an incorrect method call that made the application crash. An Integer was being passed to a method that required a string so we edited the code to use the appropriate method.

The second challenge had errors in its layout file. The onclick method was incorrectly named (and thus a non-existant method was being called on click) and the background layer was rendered as clickable which presented as a bug preventing the button from being clicked. Edits to the layout file fixed this.

The third challenge had errors in its layout and source files. There was a mismatch in the imported resources and the layout for the activity prevented the text from being seen.

The fourth challenge had the most to fix.
In the main activity java file we moved the logic for instatiating some of the objects into the onCreate method. Because the movies object was never instantiated in the first place it caused a bug with null object reference.
A layout manager was also never set for the recycler view so that also needed to be added.
Lastly, the fetchmovies() method never called the notifyDataSetchanged method, so we passed the adapter object into the fetchmovies method to be able to call that.
In the adapter code the getItemCount method was non-functional so we fixed that as well to return the size of the movies ArrayList.
Lastly there was a typo in the model for the movie object which caused the title to not be extracted properly.


GIF HERE

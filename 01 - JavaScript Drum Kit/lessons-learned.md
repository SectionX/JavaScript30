1) The DOM API returns a nodelist. Afaik there isn't any particular benefit to 
   working with nodelists and it's mostly done so the API can remain language
   agnostic. Unless there is information to the opposite, it's a good practice
   to create an array out of a nodelist, and to do this in JS, use the Array's
   method: .from which copies and transforms any iterable to an array.

   Array.from(nodelist) 

2) Up till know I was familiar with click Event. Today I've learned about keydown
   and transition Events. In particular, 
   
   I applied keydown to the window element of the DOM, so whenever anyone presses
   a button anytime while on the website, JS will listen and respond.

   I also applied a transitionend event listener to the div elements. One way to animate an element is to add a class with different CSS style. The act of adding 
   the class is a transition, so once it finishes, the listener will remove the class
   and return the element to it's default style.

3) Audio tags have a method called .play() which plays the source media file. Audio
   elements have a property "currentTime" which is essentially the sound's duration.
   Repeated attempts to play the sound before the file has ended playing will result
   in failure unless I "rewind" the file, by setting currentTime = 0;

4) The data- attribute is the standard way to add data attributes. These attributes can
   be anything really and by using the data- notation it's possible to directly manipulate them through the DOM.
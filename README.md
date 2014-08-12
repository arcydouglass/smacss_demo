#CMYK - A SMACSS/ SASS Project
===========
CMYK is a project that brings together some of the things that I was learning about Scalable Modular And Modular Architecture of CSS (SMACSS):

https://smacss.com/

And Syntactically Awesome Style Sheets (SASS):

http://sass-lang.com/


####Structure

The combination of SMACSS/ SASS makes CSS much more like a like a programming language. SMACSS has the advantage of breaking the CSS into smaller to understand pieces.  This is based on five main categories of base, layout, module, state and theme.  All of these files are imported into a master file.

In order to take advantage of the power of SASS, I also added another category called mixins.Mixins are small small snippets of code that can be repeated every time the mixin is called. SASS also brings the power of variables and mixins which is the ability to reuse chunks of doce.

By splitting the CSS into its core pieces, I found that the CSS was easier to read and easier to edit.

 
####Mixins and Modules

The power of SMACSS and SASS suggested new patterns for organizing objects in CSS. I found this to be useful in splitting object declarations and any actions that might use the object like an animation. In this project, each module was used a combination of object declarations and a type of animation.

Defining the object in my case it was a box. The box declaration was a mixin with standard height and width properties. The mixin could then be imported into the module.  The mixin would be used as many times as the module was referenced by the the HTML. If I wanted to change the declaration of the box, I only changed it one place.

Each animation was a mixin that was defined independent of a specific object. This meant that if I needed to use a different animation, I could just change the animation that is imported in the module. I could also change a box to a circle I could just change the shape declaration that I wanted to import. 

This provided an efficient way to include media queries which would provide directions on how the module would change in response to changes in screen sizes. SASS's mixin was very useful to import specific code of the animation.

Since the code for each module was very small, I ended up combining related modules together in one file.  This also allowed me add definitions for pseudo classes.

####HTML ID/ Classes

I found that my HTML classes were more descriptive to represent the added specificity of the SMACSS modules. One of the surprising things was that every time I wanted to have an object of a different color, I had to have a new class.  In a programming language, the color  might have been stored in an array which would have allowed a simple ways to create a series of classes that are the same except for a change in color. Even CSS like @extend would still require an individual class for each color.

Still this was a huge improvement over standard CSS.






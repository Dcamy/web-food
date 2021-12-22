# web-food
Creating a responsive "web food" website as part of @academind's #100DaysOfCode course

Only adding to GH to practice using it for version control etc.

This is not open sourced code https://github.com/academind/100-days-of-web-development/blob/08-responsive-web-design/LICENSE.MD

More here https://academind.com/courses

/* 3 keyboard short cuts you should be constantly using are; 
1. alt+shift+f to clean up your code (must install Prettier) and
2. ctrl+s to save your changes. By making this your default after every change
you save yourself a shit ton of headache trying to sort out why an edit didn't
do anything  
3. ctrl+/ for adding comments and/or commenting out settings*/

/* Build from the top to the bottom, less specific to greater specificiy */

/* 

Diving into Units (specifically for font size)

PX are easy to understand and translate but they limit the users control.

% is relative to the parent element size and hard to manage due to cascading nature
i.e. 100% on my browser is 16px. and 200% is. DEPENDANT ON THE PARENT

EM Size is relarive to the font size, and hard to manage due to cascading nature
If no font size is set to a parent then the default becomes the browser defaults font size. Is equal to the % 1em is 100% and yet sometime differnt. DEPENDANT ON THE PARENT

REM Size is relative to the root element font size, i.e. the HTML root font, if no font size is declared in the CSS such as 

HTML {
    font-size: 16px;
}. 

Then it will default to the the browser defaults, the parents be damned here. This returns control to the user and is the preferred choice IF APPLICABLE. 

The specific application can depend on the individual preferences as a dev and also on project requirments. For our WebFood site we will be stylilng with "rem"

*/

/* 

Deep dive em vs rem vs % NOT working with Text elements

% Always referes to parent elements 

em & rem always refer to the default fontsize set my the browser unless overwritten in the CSS root HTML which should never be done.

We will use rem, % and px for other elements, and mostly if not entirely rem for font sizing

*/

DESKTOP FIRST VS MOBILE FIRST
Responsive design is about more then just units, 

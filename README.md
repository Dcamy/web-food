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

Desktop First - 
Traditional Approach
Office Based Audiance 
Feature-rich websites

Mobile First -
Functional appraoch - less space to work with
Lifestyle/news focused audiance IG is mobile first 
"Content First" -

Your adiance and thier device is the driving factor if you should build mobile first or desktop first
This we have a huge impact in what you build and how you build it.

Think of the MVP, do you build it for the desktop user and then adjust it for the mobile user or build smaller mobile and adjust for desktop. Both approaches are both valid, but today we generally build mobile first.

As the course is made for office based users it follows the feature rich desktop first design flow


GETTING STARTED WITH MEDIA QUERIES

Is CSS

@media (min width or max-width: 1200px) {
                    p {
            font-size: 2rem;
                    }
            }

This tells the browser we need need to know about the users device, if it meets critiria use x

Desktop First - we say if the screen is only 1200px start scaling down the contect and provide these NEW rules 2rem, and if again the px drop to say 768px we want to drop again and apply THESE NEW rules i.e. 1.5rem 

Mobile First - we apply the revers logic, we build smaller say 1.5rem and if the screen is larger then apply 2rem, if it is a desktop apply 3rem. 

This is not just rem, font size, color etc, the entire CSS code should be reapplied for the given screen size

< 768px and < 1200px or > 768px and > 1200px either way you go these are called break points

Only that which is defined by the media queries change, this could be only the font size. We do not write each line for each break point, we simply say We are building Desktop first, if you have a small 1200px then do this, if 768 do this for x, y, and z and sometime m, p, j, d and so on

Common break point - (not the only ones)

Portrait devices - 
smart phone 480px 
table 768px

Landscape devices - 
Notebook 1024px 
Desktop 1200px 
TV >1200px
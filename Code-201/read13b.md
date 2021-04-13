**Transforms**

Transform property can be control size, position, and change elements. There are two different settings for transform property, two dimensional and three dimensional.

*Transform Syntax:*
The actual syntax for the transform property include the transform property followed by the value. The value specifies the transform type followed by a specific amount inside parentheses.

*2D Transforms:*
Two-dimensional transforms work on the x and y axes.

* 2D Rotate:
The rotate value provides the ability to rotate an element from 0 to 360 degrees. 

* 2D Scale:
Using the scale value within the transform property allows you to change the appeared size of an element. The default scale value is 1.

* 2D Translate:
The translate value works a bit like that of relative positioning, pushing and pulling an element in different directions without interrupting the normal flow of the document.

* 2D Skew:
Skew is used to distort elements on the horizontal axis, vertical axis, or both.


*3D Transforms:*
Using three-dimensional transforms we can change elements on the z axis, giving us control of depth as well as length and width.

* 3D Rotate:
With three-dimensional transforms we can rotate an element around any axes,  we use three new transform values, including rotateX, rotateY, and rotateZ.

* 3D Scale:
By using the scaleZ three-dimensional transform elements may be scaled on the z axis.

* 3D Translate:
Elements may also be translated on the z axis using the translateZ value.

* 3D Skew:
Elements may be skewed on the x and y axis, then transformed three-dimensionally as wished, but they cannot be skewed on the z axis.


**Transitions & Animations**

With CSS3 transitions you have the potential to alter the appearance and behavior of an element whenever a state change occurs, such as when it is hovered over, focused on, active, or targeted. Animations within CSS3 allow the appearance and behavior of an element to be altered in multiple keyframes. 

*Transitions:*

For a transition to take place, an element must have a change in state, and different styles must be identified for each state. There are four transition related properties in total, including transition-property, transition-duration, transition-timing-function, and transition-delay. 

*Animations:*

* Animations Keyframes:
To set multiple points at which an element should undergo a transition, use the @keyframes rule. The @keyframes rule includes the animation name.

* Animation Duration, Timing Function, & Delay:
The animation-duration property include a duration, timing function, and delay if desired.


**8 SIMPLE CSS3 TRANSITIONS THAT WILL WOW YOUR USERS**

First, we’ll set up a div in an HTML page, after that Having done so, set its width and height (so it has dimensions), its background color (so we can see it) and its transition property.

1- Fade in: Fade in effects are coded in two steps: first, you set the initial state; next, you set the change.

2- Change color: We just set the div’s class to “color” and specify the color we want in our CSS.

3- Grow & Shrink: To grow an element, you used to have to use its width and height, or its padding. But now we can use CSS3’s transform to enlarge. Shrinking an element is as simple as growing it. To enlarge an element we specify a value greater than 1, to shrink it, we specify a value less than 1.

4- Rotate elements: CSS transforms have a number of different uses, and one of the best is transforming the rotation of an element. Give your div the class “rotate” and add the following to your CSS:
.rotate:hover{
        -webkit-transform: rotateZ(-30deg);
        -ms-transform: rotateZ(-30deg);
        transform: rotateZ(-30deg);
}

5- Square to circle: With CSS, it’s a simple effect to achieve, we just transition the border-radius property.

6- 3D shadow: This effect is achieved by adding a box shadow, and then moving the element on the x axis using the transform and translate properties so that it appears to grow out of the screen.

7- Swing: This animation simply moves the element left and right.

8- Inset border: We can add a border to an element simply.



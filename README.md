# Motion- Design for the Web

Exercises and project starter files to follow along with the Motion Design For the Web course

## My takeaways or keynotes from the lessons

Lessons 1 & 2 [exercise 1, 2, 3](./starter%20kit/exercise-3.html) - Videos:

- If you're self-hosting the video, using the `<video>` element to add them anywhere in the oage is the best bet.
- You can then finetune the video functionality by using HTML attributes like `muted`, `autoplay`, `loop`, `controls`.
- Controlling the appearance of the video player can be done easily by using frameworks like `[VideoJS](https://videojs.com/)`
- You need to always optimize video formats and size to ensure faster page loading times. MP4 is a reliable option in terms of video format that is supported by all browsers and media players... however WebM is also viable and offers smaller file sizes without sacrificing quality even if it is not as widely supported by browsers.
- Tool for reducing the file size of videos (to compress or convert to different format) to add to your website: [Handbrake](https://handbrake.fr/).

Lesson 3 [exercise 4](./starter%20kit/exercise-4.html) - CSS Transitions:

- CSS transitions are a CSS feature that allows for smooth and gradual changes in element properties.
- Transitions are different from animations mainly because they go from point A to B with nothing in between.
- Applying transitions in CSS is done by using the `transition-property`, `transition-duration`, `transition-timing-function`, `transition-delay` properties.
- We can also use the shorthand notation of `transition`. You can transition multiple element properties at the same time by separating them with commas.
- The broswer can be instructed to transition all available properties at the same time by using the value `all`. However this should be avoided due to possible performance issues.

Lesson 4 [exercise 5 & 6](./starter%20kit/exercise-6.html) - Adding Motion via CSS transitions:

- Note all CSS properties support trasitions, like `background`. However, there are workarounds, one of which being the use of pseudo-elements.
- Not all transition in a page need the same duration. Sometimes, using a longer transition among shorter ones can create a very satisfying movement.
- Transitions are not limited to hover states. For example, they can be triggered when an element receives a certain class.

## Introduction to CSS Animations

A CSS animation is a way to make elements `gradually change` their appearance or position over time. It is done by defining `keyframes`, which are the in-between states of this change. The animation is then created by smoothly `transitioning` between these keyframes.

2 parts:

- Define the keyframes: essentially describing the animation, step-by-step.
- Apply that animation to the elements that you want.

Format -

```css
.box {
  animation: duration | easing-function | delay | iteration-count | direction |
    fill-mode | play-state | name;
}
```

- To create keyframes, use `@keyframes` followed by a chosen name. Then, inside curly braces, describr the animation steps. You can use `from {}` and `to {}` for the easiest setup.
- You cam apply animations using properties like `animation-name`, `animation-duration`, and `animation-delay`. You can also use a shorthand `animation` property with values for **duration**, **easing**, **delay**, **iteration-count**, **direction**, **fill-mode**, **play-state**, and name.
- At a minimum, we need to specify the animation name and duration; the rest can be added as needed.
- Adding `alternate` as the direction causes the animation to alternate between **forward** and **reverse** at the end of each iteration, creating a **back-and-forth** effect.
- Tim values are important when using the shorthand notation; the first one is assigned to `animation-duration` and the second one to `animation-delay`.
- Finally, remember that animations consist of multiple keyframes and support looping, direction changes and play/pause.
- Transitions - on the other hand, only have two steps (start and end) and run once with a fixed direction.

Lessons 8 - 11:

- **Loading animations** have the task of keeping users **informed** and sometimes showing the **progress** of a certain action.
- Most of the time these animations will be used as website **preloaders**. However, they can be used in other parts of the UI, like for example in a button.
- You can easily create simple **spinners** by making certain **borders** transparent and then using a `rotate` or `scale` transform.
- To display a loading animation while a page is loading, add an event listener for the load event in JavaScript. Once that kicks in, hide your loader and display the page content.
- To create an **animated SVG text**, consider using the `stroke-dasharray` and `stroke-dashoffset` properties. The first one defines the pattern of **dashes and gaps**, while the second one defines the **offset** of the starting point for the dashes.
- When creating a loading animation that has multiple elements, consider adding a different animation-delay to each element for a unique movement pattern.

Lesson 5 [exercise 14](./starter%20kit/exercise-14.html) - Animated Avatars

- Animated illustrations and icons can enhance the user experience if used properly.
- Animated illustrations and icons can increase the engagement, catching the user's attention and often making them more likely to stay and explore.
- They can also be used for guiding a user through a process or drawing the focus to certain key elements.
- The UX is also enhanced when animation is used to provide instant feedback on actions, like for example changing a hamburger icon to a close icon on click.
- On the technical side, an illustration is easily done by first **grouping** the elements, then loading the illustration as an **`inline SVG`** and then animating the individual elements.
- Another option is to set the illustration as a background-image and then animate the background-position. This approach works best for creating animated characters. The key part is to use the `steps()` timing function to break the animation into segments.

Lesson 6 [exercise 16](./starter%20kit/exercise-16.html) - Creating Accent Animations

- They enhance the visual appeal without being the main focus.
- Accent animations are the thoughtful touches that make a website not just usable but enjoyable. They are like the spices in a dish - not the main ingredient but essential for the flavour.
- They can be used for guiding users to important elements in the page, for enhancing interaction by providing feedback, and for improving usability by visually signalling what can be interacted with.
- Learnt about `GSAP` which stands for GreenSock Animation Platform. With GSAP you can animate anything you want but also creat timelines whioch are basically animation sequences.
- Also, creating custom easings are super simple with tools like [Cubic Bezier](cubic-bezier.com) which allows you to create custom easing curves.
- You can create a pause in a looping CSS animation by adjusting the keyframe percentages. this trick extends the time an element stays still, giving a delay effect without extra code.

Lesson 7 [exercise 17](./starter%20kit/exercise-17.html) - Mouse effect

How the CSS Animation Works
Key CSS Properties

    stroke-dasharray: 1500; (for stems) / 500; (for dots):

        Creates a dashed line pattern where the dash length equals the gap length

        For stems, the pattern is 1500px dash followed by 1500px gap

        For dots, it's 500px dash followed by 500px gap

    stroke-dashoffset: 3000;:

        Shifts the starting position of the dash pattern

        At 3000px offset (which is twice the stem's dasharray), the path becomes invisible

    Animation:

        The @keyframes lines animation changes stroke-dashoffset from 0 to 3000

        This creates the illusion of the path being drawn and then erased

        The animation runs infinitely with a 4-second duration

    Animation Delay:

        animation-delay: calc(var(--item) * 1s); creates staggered start times

        Each path has a different --item value (1, 2, or 3) resulting in 1s, 2s, and 3s delays

    Color System:

        Colors are defined as CSS variables (--color) in the SVG's style attribute

        The .stem and .dot classes apply these colors to their respective paths

Animation Process

    Initial State:

        The entire path is visible because the dash pattern starts at position 0

    Animation Progress:

        The dashoffset increases, shifting the pattern along the path

        This creates the appearance of the path being "drawn" as the dash moves

        As the offset approaches 1500 (for stems), the path becomes completely visible

        As the offset continues to 3000, the path disappears

    Reset and Repeat:

        When the animation completes (100%), the offset is 3000 and the path is invisible

        The animation resets to the beginning, making the path visible again

        This creates a continuous drawing and erasing effect

The combination of the dash pattern manipulation with staggered animation delays creates the mesmerizing effect of the letter "i" being continuously drawn and erased in a sequential manner.

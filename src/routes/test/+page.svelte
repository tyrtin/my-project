<script>
    let width = 400;
    let height = 300;


</script>




<main>
<!-- The main SVG element with a class "img", a coordinate system (viewBox), and SVG namespace -->
<svg class="img" viewBox="0 0 {width} {height}" xmlns="http://www.w3.org/3000/svg">

<!-- <defs> is used to define reusable elements like patterns, gradients, clipPaths, etc. -->
<defs>

<!-- Define a pattern with an ID so it can be referenced later.
- patternUnits="userSpaceOnUse" makes the pattern use the same coordinate space as the SVG.
- width and height define the size of the pattern area. -->
<pattern id="imgPattern" patternUnits="userSpaceOnUse" {width} {height}>

<!-- This image is embedded into the pattern.
- href: the URL of the image to be used.
- x and y: position the image at the top-left corner of the pattern.
- width and height: size of the image to match the SVG viewBox.
- preserveAspectRatio: controls how the image scales/crops to fit the shape. -->
<image
href="kapten.jpg" 
x="0" y="0"
{width} {height}
preserveAspectRatio="xMidYMid slice"
/>

</pattern>
</defs>

<!-- The actual shape you want to fill: a polygon with custom points.
- points define the corners of the polygon (custom shape).
- fill uses the pattern defined above to fill the shape with the image. -->
<svg class="img" viewBox="0 0 {width} {height}" xmlns="http://www.w3.org/3000/svg">
<defs>
<pattern id="imgPattern" patternUnits="userSpaceOnUse" {width} {height}>

</pattern>
</defs>

<!-- The actual shape you want to fill: a polygon with custom points.
- points define the corners of the polygon (custom shape).
- fill uses the pattern defined above to fill the shape with the image. -->

<!-- Polygon shape filled with the image pattern
"
0 0, Top-left corner (x=0, y=0)
1300 0, Top-right corner (x=1300, y=0) — same height as top-left, so it's a straight top edge
1300 300, Bottom-right corner (x=1300, y=300) — full height on the right
0 180, Bottom-left corner (x=0, y=180) — lower than the top but higher than the bottom-right
0 0 Back to the start to close the shape
"


-->
<polygon
points="0 0, {width} 0, {width} {height}, 0 150, 0 0"
fill="url(#imgPattern)"
/>
</svg>


</svg>

<!-- The main SVG element with a class "img", a coordinate system (viewBox), and SVG namespace -->
<svg  style="margin-top: -100px;" class="img" viewBox="0 0 1300 300" xmlns="http://www.w3.org/3000/svg">

    <!-- <defs> is used to define reusable elements like patterns, gradients, clipPaths, etc. -->
    <defs>
    
    <!-- Define a pattern with an ID so it can be referenced later.
    - patternUnits="userSpaceOnUse" makes the pattern use the same coordinate space as the SVG.
    - width and height define the size of the pattern area. -->
    <pattern id="imgPattern" patternUnits="userSpaceOnUse" width="1300" height="300">
    
    <!-- This image is embedded into the pattern.
    - href: the URL of the image to be used.
    - x and y: position the image at the top-left corner of the pattern.
    - width and height: size of the image to match the SVG viewBox.
    - preserveAspectRatio: controls how the image scales/crops to fit the shape. -->
    <image
    href="kapten.jpg" 
    x="0" y="0"
    width="1300" height="300"
    preserveAspectRatio="xMidYMid slice"
    />
    
    </pattern>
    </defs>
    
    <!-- The actual shape you want to fill: a polygon with custom points.
    - points define the corners of the polygon (custom shape).
    - fill uses the pattern defined above to fill the shape with the image. -->
    <svg class="img" viewBox="0 0 1300 300" xmlns="http://www.w3.org/3000/svg">
    <defs>
    <pattern id="imgPattern" patternUnits="userSpaceOnUse" width="1300" height="300">
    
    </pattern>
    </defs>
    
    <!-- The actual shape you want to fill: a polygon with custom points.
    - points define the corners of the polygon (custom shape).
    - fill uses the pattern defined above to fill the shape with the image. -->
    
    <!-- Polygon shape filled with the image pattern
    "
    0 0, Top-left corner (x=0, y=0)
    1300 0, Top-right corner (x=1300, y=0) — same height as top-left, so it's a straight top edge
    1300 300, Bottom-right corner (x=1300, y=300) — full height on the right
    0 180, Bottom-left corner (x=0, y=180) — lower than the top but higher than the bottom-right
    0 0 Back to the start to close the shape
    "
    
    
    -->
    <polygon
    points="0 0, 1300 150, 1300 300, 0 300, 0 0"
    fill="url(#imgPattern)"
    />
    </svg>
    
    
    </svg>

</main>

<style>
    main{
        width: 70vw;
        height: 100vh;
        border: solid 5px black;
        justify-self: center;
    }
</style>
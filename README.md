Responsive Image Breakpoint for jQuery
======================================

This is jQuery plugin that allows the images to be specifed depending on the viewing devices screen size.

To implement 
------------

include jQuery - currently only tested with 1.7.1
include to the 'jQuery.responsiveBreakpointJQ.js' file or the minimised version and then update your images with the data attribute for the breakpoints

<img src="small.jpg" data-480="medium.jpg" data-960="large.jpg" alt="Image Alt text" />

Use the document ready to use the plugin. The following will test all img elements in the body.

<script>
$(document).ready(function() {
	$('body img').replaceResponsiveImages();
});
</script>

The breakpoint are specified using the 'data-480' with the number being the pixel width at which that image comes into play above. An image specified with 'data-480' will be used for all devices with a screen width of over 480px. If there are multiple breakpoints the screen with with be tested against each of them and only then will the maximum one that passed the width test be used.




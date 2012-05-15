Responsive Image Breakpoint for jQuery
======================================

This is jQuery plugin that allows the images to be specifed depending on the viewing devices screen size.

To implement 
------------

include jQuery - currently only tested with 1.7.2

	<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js"></script>

include to the 'jQuery.responsiveBreakpointJQ.js' file or the minimised version.

	script src="../jQuery.responsiveBreakpointJQ.js"></script>
	
	Update your image elements with the data attribute for the breakpoints

	<img src="small.jpg" data-480="medium.jpg" data-960="large.jpg" alt="Image Alt text" />

Use the document ready to use the plugin. The following will test all img elements in the body.

	<script>
	$(document).ready(function() {
		$('body img').replaceResponsiveImages();
	});
	</script>

The breakpoint are specified using the 'data-480' with the number being the pixel width at which that image comes into play above. An image specified with 'data-480' will be used for all devices with a screen width of over 480px. If there are multiple breakpoints the screen with with be tested against each of them and only then will the maximum one that passed the width test be used.

For retina images the plugin simply doubles the screen width and tests against that to get the double with images if they are specified. e.g. data-960 will be the retina image for a device of 480 width.




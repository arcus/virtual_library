<!--
dart_module_id: sql_basics
dart_author: Test Author
dart_title: Test Module
author:   Rose Hartman
version:  1.0.0
language: en
narrator: UK English Female
title: Module Macros
comment:  This is placeholder module to save macros used in other modules.

@make_dart_url
<script modify="false">

function makeURL(module_id) {
const url = `https://liascript.github.io/course/?https://raw.githubusercontent.com/arcus/education_modules/main/${module_id}/${module_id}.md#1`;
  return url;
}

var dartURL = makeURL(@0);
var dartTitle = @1

send.html(`<a href="${dartURL}" target="_blank">${dartTitle}</a>`)
</script>

@end

@dart_citation

This module was adapted from a DART module on the same topic originally written by @dart_author and shared under a [creative commons license](https://github.com/arcus/education_modules/blob/main/LICENSE). 
You can access the original module online here: @make_dart_url('@dart_module_id', '@dart_title')

@end

@overview

## Overview
@comment

**Is this module right for me?** @long_description

**Estimated time to completion:** @estimated_time_in_minutes minutes

**Pre-requisites**

@pre_reqs

**Learning Objectives**

After completion of this module, learners will be able to:

@learning_objectives

@end

@gifPreload
<script>
(function($) {

  // Get the .gif images from the "data-alt".
	var getGif = function() {
		var gif = [];
		$('img').each(function() {
			var data = $(this).data('alt');
			gif.push(data);
		});
		return gif;
	}

	var gif = getGif();

	// Preload all the gif images.
	var image = [];

	$.each(gif, function(index) {
		image[index]     = new Image();
		image[index].src = gif[index];
	});

	// Change the image to .gif when clicked and vice versa.
	$('figure').on('click', function() {

		var $this   = $(this),
				$index  = $this.index(),

				$img    = $this.children('img'),
				$imgSrc = $img.attr('src'),
				$imgAlt = $img.attr('data-alt'),
				$imgExt = $imgAlt.split('.');

		if($imgExt[1] === 'gif') {
			$img.attr('src', $img.data('alt')).attr('data-alt', $imgSrc);
		} else {
			$img.attr('src', $imgAlt).attr('data-alt', $img.data('alt'));
		}

		// Add play class to help with the styling.
		$this.toggleClass('play');

	});

})(jQuery);
</script>
@end

link:  https://cdn.jsdelivr.net/gh/arcus/education_modules@main/assets/styles.css

script: https://kit.fontawesome.com/83b2343bd4.js
script:  https://code.jquery.com/jquery-3.6.0.slim.min.js

-->

# Module Macros

@overview

@dart_citation

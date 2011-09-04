## jQuery Detect TimeZone Plugin

This jQuery plugin leverages Jon Nylander's [jstimezonedetect](https://bitbucket.org/pellepim/jstimezonedetect) (based on work by Josh Fraser). 

## Why? 

There are plenty of javascript examples out there showing how to work with the timezone offset. Unfortunately this approach has some disadvantages, especially in regards to day light savings. 

> Determining timezones using javascript is not trivial out of the box. Different browsers use different acronyms and conventions for representing names of timezones, it also differs depending on the user's operating system.

## How to use



First, add the required scripts to your page (jquery, detect_timezone.js, and jquery.detect_timezone.js)

Then use one of the two timezone functions. 

1. set_timezone - sets the current timezone value by calling .val on the selector. This generally assumes the selector is an input (text or hidden). 
1. get_timezone - this method will return the current Olson timezone name.

Options: 

* debug - defaults to false. When true, it let you know that for some reason a timezone could not be found. 
* default - allows you to set a default value in the case no timezone could be found. Defaults to 'America/New_York'

## Example:

	<script>
		$(document).ready(function(){
				$('#tzvalue').set_timezone({
					'default' : 'America/Los_Angeles'
				});
		});
	</script>

_Note: There is an extremely minimal example in this repository._

## Disclaimers

Blah, blah, blah....use it, tweak it, etc. 

Always feel free to drop me a line at scottwater@gmail, but please use GitHub issues for any bugs/etc. 
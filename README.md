# jQuery TimePicker

jQuery TimePicker is a plugin to help users easily input time entries. It works by allowing the user to type times in a free format or selecting them from a dropdown menu.

The plugin will automatically convert all time entries using a format that can be changed passing the timeFormat option; the default value is hh:mm p which will give something like 02:16 PM.

The following are a few examples of the strings an user can type and how the plugin understands them:

| Input | Output (using the default format) |
| ------------- | ------------- |
| 1234 | 12:34 AM |
| 1234p | 12:34 PM |
| 456 | 04:56 AM |
| 1656 | 04:56 PM |
| 1:1 P | 1:10 PM |
| 1:9 A | 1:09 AM |
| 8:59 | 8:59 AM |
| 12030 | 1:20:30 AM |
| 46 | 05:00 AM (it's interpreted as 4 hours plus 60 minutes) |

There are other supported formats, all inspired by the behavior of a similar timepicker used in Google Calendar. To see more, try the demos.

## How to Use
To use jQuery TimePicker you'll need to include two files: jquery.timepicker.js and jquery.timepicker.css. Then, assuming you have an <input> element in your document, you can use the following code to initialize the plugin:

```javascript
$(document).ready(function(){
  $('input.timepicker').timepicker({});
});
```

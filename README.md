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

## Options
| ------------- | ------------- |
| `timeFormat` | (string) The format of the time string displayed in the input and the menu items in the combobox. Available modifiers are: ( `h`: 12 hour without leading 0. `hh`: 12 hour with leading 0. `H`: 24 hour without leading 0. `HH`: 24 hour with leading 0. `m`: minutes without leading 0. `mm`: minutes with leading 0. `s`: seconds without leading 0. `ss`: seconds with leading 0. `p`: AM or PM) |
| `defaultTime` | A `Date` object, `string` or the word `'now`. Only the time parts (getHours, getMinutes) of the object are important. It must be a valid time, according to `minTime`, `minHour`, `minMinutes`, `maxTime`, `maxHour` and `maxMinutes`. If `'now'` is passed, the current time as returned by `new Date()` will be used as the defaul |
| `minTime` | A `Date` object or `string`. Only the time parts (getHours, getMinutes) of the object are important. Time entries before minTime won't be displayed/allowed. |
| `minHour` | `int`. Time entries with an 24-hour part before `minHour` won't be displayed/allowed. Ignored if `minTime` is set. |
| `minMinutes` | `int` Time entries with minutes part before `minMinutes` won't be displayed/allowed. Ignored if `minTime` is set. |
| `maxTime` | A `Date` object or `string`. Only the time parts (getHours, getMinutes) of the object are important. Time entries after minTime won't be displayed/allowed. |
| `maxHour` | `int`. Time entries with an 24-hour part after `maxHour` won't be displayed/allowed. Ignored if `maxTime` is set. |
| `maxMinutes` | `int`. Time entries with minutes part after `maxHour` won't be displayed/allowed. Ignored if `maxTime` is set. |
| `startTime` | A `Date` object or `string`. The time of the first item in the combobox when the input field is empty. If the input field is not empty the first item will be the next allowed time entry. |
| `startHour` | `int` The 24-hour part of the first item in the combobox when the input field is emptye. If input field is not empty the first item will be the next allowed time entry. Ignored if `startTime` is set. |
| `startMinutes` | `int` The minutes part of the first item in the combobox when the input field is emptye. If input field is not empty the first item will be the next allowed time entry. Ignored if `startTime` is set. |
| `interval` | `int` Separation in minutes between time entries in the dropdown menu. |
| `dropdown` | `boolean` Whether the dropdown should be displayed or not. |
| `dynamic` | `boolean` If a date is already selected and `dynamic` is true, the items in the dropdown will be arranged so that the first item is chronologically right after the selected time entry. |
| `scrollbar` | `boolean` Whether the scrollbars should be displayed or not. |

## Events
| ------------- | ------------- |
| `change` | Event triggerd when the value of the input field changes. A Date object containing the selected time is passed as the first argument of the callback. |
</article>

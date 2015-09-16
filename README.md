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
| `timeFormat` | (string) The format of the time string displayed in the input and the menu items in the combobox. Available modifiers are: ( `h`: 12 hour without leading 0. `hh`: 12 hour with leading 0. `H`: 24 hour without leading 0. `HH`: 24 hour with leading 0. `m`: minutes without leading 0. `mm`: minutes with leading 0. `s`: seconds without leading 0. `ss`: seconds with leading 0. `p`: AM or PM) |

<div class="highlight"><pre><code class="language-javascript" data-lang="javascript"><span class="nx">$</span><span class="p">(</span><span class="nb">document</span><span class="p">).</span><span class="nx">ready</span><span class="p">(</span><span class="kd">function</span><span class="p">(){</span>
    <span class="nx">$</span><span class="p">(</span><span class="s1">'input.timepicker'</span><span class="p">).</span><span class="nx">timepicker</span><span class="p">({</span> <span class="nx">timeFormat</span><span class="o">:</span> <span class="s1">'h:mm:ss p'</span> <span class="p">});</span>
<span class="p">});</span></code></pre></div>

            <form><input id="options-time-format"></form>
        </div>
    </div>

    <div class="row">
        <div class="span2 columns"><code>defaultTime</code></div>
        <div class="span10 columns">
            <p>A <span class="label important">Date</span> object, <span class="label important">string</span> or the word <span class="label important">'now'</span>. Only the time parts (getHours, getMinutes) of the object are important. It must be a valid time, according to <code>minTime</code>, <code>minHour</code>, <code>minMinutes</code>, <code>maxTime</code>, <code>maxHour</code> and <code>maxMinutes</code>.</p>
            <p>If <code>'now'</code> is passed, the current time as returned by <code>new Date()</code> will be used as the default value.</p>
        </div>
    </div>

    <div class="row">
        <div class="span2 columns"><code>minTime</code></div>
        <div class="span10 columns">
            <p>A <span class="label important">Date</span> object or <span class="label important">string</span>. Only the time parts (getHours, getMinutes) of the object are important. Time entries before minTime won't be displayed/allowed.</p>
        </div>
    </div>

    <div class="row">
        <div class="span2 columns"><code>minHour</code></div>
        <div class="span10 columns">
            <p><span class="label important">int</span>. Time entries with an 24-hour part before <code>minHour</code> won't be displayed/allowed. Ignored if <code>minTime</code> is set.</p>
        </div>
    </div>

    <div class="row">
        <div class="span2 columns"><code>minMinutes</code></div>
        <div class="span10 columns">
            <p><span class="label important">int</span> Time entries with minutes part before <code>minMinutes</code> won't be displayed/allowed. Ignored if <code>minTime</code> is set.</p>
        </div>
    </div>

    <div class="row">
        <div class="span2 columns"><code>maxTime</code></div>
        <div class="span10 columns">
            <p>A <span class="label important">Date</span> object or <span class="label important">string</span>. Only the time parts (getHours, getMinutes) of the object are important. Time entries after minTime won't be displayed/allowed.</p>
        </div>
    </div>

    <div class="row">
        <div class="span2 columns"><code>maxHour</code></div>
        <div class="span10 columns">
            <p><span class="label important">int</span>. Time entries with an 24-hour part after <code>maxHour</code> won't be displayed/allowed. Ignored if <code>maxTime</code> is set.</p>
        </div>
    </div>

    <div class="row">
        <div class="span2 columns"><code>maxMinutes</code></div>
        <div class="span10 columns">
            <p><span class="label important">int</span>. Time entries with minutes part after <code>maxHour</code> won't be displayed/allowed. Ignored if <code>maxTime</code> is set.</p>
        </div>
    </div>

    <div class="row">
        <div class="span2 columns"><code>startTime</code></div>
        <div class="span10 columns">
            <p>A <span class="label important">Date</span> object or <span class="label important">string</span>. The time of the first item in the combobox when the input field is empty. If the input field is not empty the first item will be the next allowed time entry.</p>
        </div>
    </div>

    <div class="row">
        <div class="span2 columns"><code>startHour</code></div>
        <div class="span10 columns">
            <p><span class="label important">int</span> The 24-hour part of the first item in the combobox when the input field is emptye. If input field is not empty the first item will be the next allowed time entry. Ignored if <code>startTime</code> is set.</p>
        </div>
    </div>

    <div class="row">
        <div class="span2 columns"><code>startMinutes</code></div>
        <div class="span10 columns">
            <p><span class="label important">int</span> The minutes part of the first item in the combobox when the input field is emptye. If input field is not empty the first item will be the next allowed time entry. Ignored if <code>startTime</code> is set.</p>
        </div>
    </div>

    <div class="row">
        <div class="span2 columns"><code>interval</code></div>
        <div class="span10 columns">
            <p><span class="label important">int</span> Separation in minutes between time entries in the dropdown menu.</p>

<div class="highlight"><pre><code class="language-javascript" data-lang="javascript"><span class="nx">$</span><span class="p">(</span><span class="nb">document</span><span class="p">).</span><span class="nx">ready</span><span class="p">(</span><span class="kd">function</span><span class="p">(){</span>
    <span class="nx">$</span><span class="p">(</span><span class="s1">'input.timepicker'</span><span class="p">).</span><span class="nx">timepicker</span><span class="p">({</span>
        <span class="nx">timeFormat</span><span class="o">:</span> <span class="s1">'HH:mm:ss'</span><span class="p">,</span>
        <span class="nx">minTime</span><span class="o">:</span> <span class="s1">'11:45:00'</span> <span class="c1">// 11:45:00 AM,</span>
        <span class="nx">maxHour</span><span class="o">:</span> <span class="mi">20</span><span class="p">,</span>
        <span class="nx">maxMinutes</span><span class="o">:</span> <span class="mi">30</span><span class="p">,</span>
        <span class="nx">startTime</span><span class="o">:</span> <span class="k">new</span> <span class="nb">Date</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">15</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">)</span> <span class="c1">// 3:00:00 PM - noon</span>
        <span class="nx">interval</span><span class="o">:</span> <span class="mi">15</span> <span class="c1">// 15 minutes</span>
    <span class="p">});</span>
<span class="p">});</span></code></pre></div>

            <form><input id="options-time-constraints"></form>
        </div>
    </div>

    <div class="row">
        <div class="span2 columns"><code>dropdown</code></div>
        <div class="span10 columns">
            <p><span class="label important">boolean</span> Whether the dropdown should be displayed or not.</p>
        </div>
    </div>

    <div class="row">
        <div class="span2 columns"><code>dynamic</code></div>
        <div class="span10 columns">
            <p><span class="label important">boolean</span> If a date is already selected and <code>dynamic</code> is true, the items in the dropdown will be arranged so that the first item is chronologically right after the selected time entry.</p>
        </div>
    </div>

    <div class="row">
        <div class="span2 columns"><code>scrollbar</code></div>
        <div class="span10 columns">
            <p><span class="label important">boolean</span> Whether the scrollbars should be displayed or not.</p>
        </div>
    </div>

    <div class="page-header"><h2>jQuery TimePicker events</h2></div>

    <div class="row">
        <div class="span2 columns"><code>change</code></div>
        <div class="span10 columns">
            <p>Event triggerd when the value of the input field changes. A Date object containing the selected time is passed as the first argument of the callback.</p>

<div class="highlight"><pre><code class="language-javascript" data-lang="javascript"><span class="nx">$</span><span class="p">(</span><span class="nb">document</span><span class="p">).</span><span class="nx">ready</span><span class="p">({</span>
    <span class="nx">$</span><span class="p">(</span><span class="s1">'input.timepicker'</span><span class="p">).</span><span class="nx">timepicker</span><span class="p">({</span>
        <span class="nx">change</span><span class="o">:</span> <span class="kd">function</span><span class="p">(</span><span class="nx">time</span><span class="p">)</span> <span class="p">{</span>
            <span class="c1">// the input field</span>
            <span class="kd">var</span> <span class="nx">element</span> <span class="o">=</span> <span class="nx">$</span><span class="p">(</span><span class="k">this</span><span class="p">),</span> <span class="nx">text</span><span class="p">;</span>
            <span class="c1">// get access to this TimePicker instance</span>
            <span class="kd">var</span> <span class="nx">timepicker</span> <span class="o">=</span> <span class="nx">element</span><span class="p">.</span><span class="nx">timepicker</span><span class="p">();</span>
            <span class="nx">text</span> <span class="o">=</span> <span class="s1">'Selected time is: '</span> <span class="o">+</span> <span class="nx">timepicker</span><span class="p">.</span><span class="nx">format</span><span class="p">(</span><span class="nx">time</span><span class="p">);</span>
            <span class="nx">element</span><span class="p">.</span><span class="nx">siblings</span><span class="p">(</span><span class="s1">'span.help-line'</span><span class="p">).</span><span class="nx">text</span><span class="p">(</span><span class="nx">text</span><span class="p">);</span>
        <span class="p">}</span>
    <span class="p">});</span>
<span class="p">});</span></code></pre></div>
            <form>
                <input id="options-change-event">
                <span class="help-line"></span>
            </form>
        </div>
    </div>
</article>

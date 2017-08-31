# MXTimer
Timer Plugin for JavaScript
## 1\. Installation MXTimer

1.  Download files !

2.  Add the code inside the body tag.

    > ```
    > <script src="mx-timer.js"></script>
    > 

3.  Start coding freely :)

## 2\. Examples

1.  Easily create timers.

    > ```
    > var myTimer = new Timer({
    >   func: function () {
    >       console.log('is timer function');
    >   },
    >   interval: 1000, // interval 1 second.
    >   autoStart: true // Automatic start timer.
    > });

2.  Define events within options.

    > ```
    > var myTimer = new Timer({
    >   func: function () {
    >       console.log('is timer function');
    >   },
    >   interval: 2000, // interval 2 second.
    >   autoStart: true, // Automatic start timer.
    >   initializer: function () {
    >       console.log('On initialize timer.'); // This function calls the timer constructor.
    >   },
    >   onafterstart: function () {
    >       console.log('After start timer.'); // This function is executed every time after the timer runs.
    >   },
    >   onstart: function () {
    >       console.log('Start timer.'); // This function is executed every time the timer runs.
    >   },
    >   onafterstop: function () {
    >       console.log('After stop timer.'); // This function is executed after it has been stopped in time.
    >   },
    >   onstop: function () {
    >       console.log('Stop timer.'); // This function is executed when the timer is stopped.
    >   },
    >   callback: function () {
    >       console.log('Callback timer.'); // Callback function
    >   }
    > );

3.  Define events after create timer.

    > ```
    > var myTimer = new Timer({
    >     func: function () {
    >         console.log('is timer function');
    >     },
    >     interval: 2000, // interval 2 second.
    >     autoStart: true, // Automatic start timer.
    > });
    > myTimer.on('start', function ($this) {
    >     console.log('Starting');
    > }).on('stop', function () {
    >     console.log('stopping');
    > });

## 3\. Options

<table border="1" width="100%" cellpadding="0" cellspacing="0">

<thead>

<tr>

<th width="100">Option Name</th>

<th width="100">Type</th>

<th>Details</th>

</tr>

</thead>

<tbody>

<tr>

<td class="title">func</td>

<td class="title">function</td>

<td>Function to be called</td>

</tr>

<tr>

<td class="title">interval</td>

<td class="title">int</td>

<td>Interval in miliseconds. (1s = 1000 ms)</td>

</tr>

<tr>

<td class="title">group_name</td>

<td class="title">string</td>

<td>If you want to group the timer, enter the group name. Note: The _global group name is used by the plugin.</td>

</tr>

<tr>

<td class="title">autoStart</td>

<td class="title">bool</td>

<td>Auto start timer.</td>

</tr>

<tr>

<td class="title">initializer</td>

<td class="title">function</td>

<td>This function calls the timer constructor.</td>

</tr>

<tr>

<td class="title">onafterstart</td>

<td class="title">function|function[]</td>

<td>This function is executed every time after the timer runs.</td>

</tr>

<tr>

<td class="title">onstart</td>

<td class="title">function|function[]</td>

<td>This function is executed every time the timer runs.</td>

</tr>

<tr>

<td class="title">onafterstop</td>

<td class="title">function|function[]</td>

<td>This function is executed after it has been stopped in time.</td>

</tr>

<tr>

<td class="title">onstop</td>

<td class="title">function|function[]</td>

<td>This function is executed when the timer is stopped.</td>

</tr>

<tr>

<td class="title">callback</td>

<td class="title">function|function[]</td>

<td>Callback function</td>

</tr>

</tbody>

</table>

## 4\. Methods

<table border="1" width="100%" cellpadding="0" cellspacing="0">

<thead>

<tr>

<th width="100">Method Name</th>

<th width="100">Return Type</th>

<th>Details</th>

</tr>

</thead>

<tbody>

<tr>

<td class="title">getCount</td>

<td class="title">int</td>

<td>The number of times the timer works</td>

</tr>

<tr>

<td class="title">trigger</td>

<td class="title">Timer</td>

<td>Trigger timer events.</td>

</tr>

<tr>

<td class="title">on</td>

<td class="title">Timer</td>

<td>Binding events.</td>

</tr>

<tr>

<td class="title">start</td>

<td class="title">Timer</td>

<td>Start timer.</td>

</tr>

<tr>

<td class="title">reset</td>

<td class="title">Timer</td>

<td>Reset timer. Like myTimer.stop(true).start();</td>

</tr>

<tr>

<td class="title">stop</td>

<td class="title">Timer</td>

<td>Stop timer.</td>

</tr>

</tbody>

</table>

## 5\. Events

<table border="1" width="100%" cellpadding="0" cellspacing="0">

<thead>

<tr>

<th width="100">Event Name</th>

<th>Details</th>

</tr>

</thead>

<tbody>

<tr>

<td class="title">onafterstart</td>

<td>This function is executed every time after the timer runs.</td>

</tr>

<tr>

<td class="title">onstart</td>

<td>This function is executed every time the timer runs.</td>

</tr>

<tr>

<td class="title">onafterstop</td>

<td>This function is executed after it has been stopped in time.</td>

</tr>

<tr>

<td class="title">onstop</td>

<td>This function is executed when the timer is stopped.</td>

</tr>

</tbody>

</table>

## 6\. Errors
<table border="1" width="100%" cellpadding="0" cellspacing="0" id="errors">
<thead>
<tr>
<th>Error</th>
<th width="100">Class</th>
<th>Details</th>
</tr>
</thead>
<tbody>


<tr>

<td class="title">Invalid argument was sent for adding timer.</td>
<td class="title">TimerInvalidAddArgs</td>

<td>If a value other than object type is entered while adding the timer, you will get this error message. You can get help from the examples above when adding timers.</td>

</tr>
<tr>

<td class="title">Timer function not defined correctly.</td>
<td class="title">TimerIsNotFunction</td>

<td>The timer has to be defined as a function. The reason for encountering this error is to define a real function.</td>

</tr>
<tr>

<td class="title">Timer function not defined correctly.</td>
<td class="title">TimerIsNotFunction</td>

<td>The timer has to be defined as a function. The reason for encountering this error is to define a real function.</td>

</tr>
<tr>

<td class="title">Invalid Interval value. Interval to be bigger than zero.</td>
<td class="title">TimerInvalidAddArgs</td>

<td>Timer interval must be greater than zero.</td>
</tr>
<tr>

<td class="title">Invalid Interval value. Interval to be bigger than zero.</td>
<td class="title">TimerInvalidAddArgs</td>

<td>Timer interval must be greater than zero.</td>
</tr>

</tbody>

</table>

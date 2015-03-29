fourier.js
==========

A Javascript library for visualizing time series. Right now it only supports area charts, but adding more graph types is fairly trivial.

Right now the smoothing is a little awkward, and the auto-sizing is very rough. There's also a strange bug where the x-axis transformations get queued when the window isn't in focus. But enough of the negatives!

The basic usage is as such:

    var myObj = new Object();
    myObj.val = 0;
    myObj.index = 0;
    setInterval(function () {myObj.val = Math.sin(myObj.index*.1); myObj.index++;}, 300);
    myGraph = new graph('#graph', myObj, 20);

All you need to do is pass it a selector, an object with a value property which can be updated with whatever method you please (websockets etc...) and the size of your window in seconds and presto you got yourself a timeseries:

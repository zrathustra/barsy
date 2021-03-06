# Barsy - animated barcodes

Barcodes are boring, there's no doubt about that.

Barsy makes them better.

Check out a quick video demo [here](http://f.cl.ly/items/2i2f3g3T0Y1O1S3f1t0h/Untitled.mov) (or clone and check out the example.html file).

This version of barsy is done using CSS3 animations via the Move.js library, rather than JavaScript animations via jQuery.

*A note about performance: in limited tests, this version consumes about the same amount of CPU cycles, but takes up about a third of the memory. YMMV.*

This version also adds stop and restart methods.  In the example, clicking the barcode will start/stop it.  You can supply a callback function to stop or restart to call upon finishing.

# Usage

    var barsy = $('.class').barsy({
            value: '123456', // defaults to text in container
            speed: 500, // defaults to 1000
            distance: .3, // defaults to .3
            height: '200px', // defaults to 150px
            color: '#3399CC' // defaults to black
    });

    // to stop the animation, call stop
    barsy.stop();

    // or supply a callback function
    barsy.stop(function (shout, out) { console.log(shout + out) }, "now ", "stopping");

    // to restart the animation, call restart
    barsy.restart();

    // or supply a callback function
    barsy.stop(function (shout, out) { console.log(shout + out) }, "now", "restarting");


# Unsubscribe-all-Youtube-channels-
How to unsubscribe from all the Youtube channels at once?

##Step 1:
Go to https://www.youtube.com/feed/channels and scroll to the bottom of the page to populate all items to the screen.

##Step 2:
Right-click anywhere on the page and click "Inspect Element" (or just "Inspect"), then click "Console", then copy–paste the below script, then hit return.

##Step 3:

```
var i = 0;

var myVar = setInterval(myTimer, 3000);

function myTimer () {

    var els = document.getElementById("grid-container").getElementsByClassName("ytd-expanded-shelf-contents-renderer");

    if (i < els.length) {

        els[i].querySelector("[aria-label^='Unsubscribe from']").click();

        setTimeout(function () {

            var unSubBtn = document.getElementById("confirm-button").click();

        }, 2000);

        setTimeout(function () {

            els[i].parentNode.removeChild(els[i]);

        }, 2000);

    }

    i++;

    console.log(i + " unsubscribed by 9c9a");

    console.log(els.length + " remaining");

}
```

##Step 4:
Sit back and watch the magic!

Enjoy!!

##NOTE: If the script stops somewhere, please refresh the page and follow all four steps again.

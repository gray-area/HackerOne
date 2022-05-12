# Flag 1 - cURL

In order to get flag 1, we need to be able to edit the page. Admittedly, I did this flag last. 

I wasnt sure what the edit page looked like or where it was, but I knew we could test using ``curl`` and form a request. 

``curl -v -X POST [hackeroneurl]/page/edit/1``

The above command has a ``-v`` switch that outputs in verbose. 

The ``-X`` switch is used to designate a request, followed by the method. In our case, I used ``-X POST``.

Finally, I entered the hackerone url, followed by ``/page/edit/1``.

After entering this command, the flag will be displayed at the bottom of the output. 

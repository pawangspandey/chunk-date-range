
# chunk-date-range

  Split a date range into a certain amount of equal sized chunks, or into boundaries by 'day', 'week', 'year', etc.

## Quickstart

```javascript
var chunk = require('chunk-date-range');

var start = new Date('5/11/2013');
var end = new Date('5/20/2013');
var chunks = 2;

chunk(start, end, chunks);

/**
 * [ { start: Sat May 11 2013 00:00:00 GMT-0700 (PDT),
 *   end: Wed May 15 2013 12:00:00 GMT-0700 (PDT) },
 * { start: Wed May 15 2013 12:00:00 GMT-0700 (PDT),
 *   end: Mon May 20 2013 00:00:00 GMT-0700 (PDT) } ]
 */

chunk(start, end, 'day');

/**
 * [ { start: Sat May 11 2013 00:00:00 GMT-0700 (PDT),
 *   end: Sat May 11 2013 17:00:00 GMT-0700 (PDT) },
 * [...]
 * { start: Sun May 19 2013 17:00:00 GMT-0700 (PDT),
 *   end: Mon May 20 2013 00:00:00 GMT-0700 (PDT) }
 */

```

## API

### chunkDateRange(start, end, chunks)

  * start - Date to start from
  * end - Date to end with
  * chunks - number of chunks to split into, or the duration

  returns `chunks` evenly spaced intervals beginning with `start` and ending with `end` in the form

```javascript
[
  {
    start: Date
    end: Date
  }
]
```

## License

(The MIT License)

Copyright (c) 2013 segmentio &lt;friends@segment.io&gt;

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
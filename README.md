phantomjs-ajax-snapshot
=======================

Simple script that generates static pages from ajax / non-ajax source pages. Allows stripping of DOM elements identifying them by id, class, name or meta-property (only for meta tags). 

## Usage

  Options:

    (sourceFile | sourceUrl)

    -sourceFile    (string) file with json array format, containing the set of urls to generate.

    -sourceUrl    (string) single url to visit.

    -basePath    (string) common basepath among urls.

    -separator    (string) separator to replace '/' in file names ([---] by default).

    -waitingTime    (miliseconds) Use specified waiting time to load javascript of every page (3000 by default).

    -outputDir    (string) place to write the output files (static/ by default).

    -idlist    (Array) elements id to strip in html (empty by default).

    -classlist    (Array) elements class to strip in html (empty by default).

    -metalist    (Array) elements metaname to strip in html (empty by default).

    -debug    (boolean) Enables debug messages (false by default).

## Examples

**Snapshot from url:**

phantomjs phantomjsAjaxSnapshot.js  --ssl-protocol=any --web-security=false --disk-cache=no -sourceurl www.my-cool-ajax-web.com -outputdir snapshots\


**Snapshot from url stripping DOM elements with classes a,b,c:**

phantomjs phantomjsAjaxSnapshot.js  --ssl-protocol=any --web-security=false --disk-cache=no -sourceurl www.my-cool-ajax-web.com -outputdir snapshots\ -classlist a,b,c


**Snapshots from json array of urls:**

phantomjs phantomjsAjaxSnapshot.js  --ssl-protocol=any --web-security=false --disk-cache=no -sourceFile myUrls2visit.json -basepath www.my-cool-ajax-web.com/common/path -outputdir snapshots\


## Tests

  not yet :(

## Dependencies

  [Phantomjs](http://phantomjs.org/ "Phantomjs' Homepage") headless webkit with JS API.

## Contributing

In lieu of a formal styleguide, take care to maintain the existing coding style.
Add unit tests for any new or changed functionality. Lint and test your code.

## Author

[Eric Lara](https://www.twitter.com/EricLaraAmat), supported by [Ondho](http://www.ondho.com).

## License

  MIT

## Changelog

* 0.0.1 Initial commit

## Roadmap

* connect with [node-ajax-snapshot](https://github.com/ericzon/node-ajax-snapshot) (WIP).



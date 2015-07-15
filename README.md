# US National Debt Widget

The debt widgets aka "debt clocks" I found[^1] weren't available over a secure connection, this one doesn't require an external website, just upload a single file to your server.

# Usage

1. Upload `debtClock.min.js` to your public webroot.
2. Add the script to your HTML with the correct path to the above file.
3. Call the script after your DOM has loaded.

````html
<h1 id="debtClock">Calculating debt...</h1>
<script src="debtClock.min.js" type="text/javascript"></script>
<script type="text/javascript">
  (function() {
    // the DOM will be available here
    var options = {};
    var debtClock = new DebtClock(options);
  })();
</script>
````

[See available options](https://github.com/shennyg/us-national-debt-widget/blob/master/src/app.js#L27).

# Development

For fun this was built using [ES2015](https://babeljs.io/).

1. Install [broccoli](https://github.com/broccolijs/broccoli)
2. Install required development modules, run `npm install`
3. Run `npm run serve` or `broccoli serve` and open [http://localhost:4200/](http://localhost:4200/). Broccoli will watch for modifications to `src/app.js` and recompile so all you need to do is refresh your browser.

# Build

1. To build the files into `dist/` and test on [http://localhost:8000/](http://localhost:8000/), run `npm run build` or `sh ./build.sh`

The file you will want is `dist/debtClock.min.js`.

# Todo

- [ ] Add to free CDN service so people can use without hosting the file.

# Footnotes

[^1]: US Debt Widgets without a valid SSL cert: http://www.usadebtclock.com/debt-clock-widget-for-website.php & http://zfacts.com/p/789.html
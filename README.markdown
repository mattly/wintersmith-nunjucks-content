# wintersmith-nunjucks-content

A Content Plugin for rendering [nunjucks][] pages for [wintersmith][].

[nunjucks]: http://nunjucks.jlongster.com/
[wintersmith]: http://jnordberg.github.com/wintersmith/

## How to Use

1. Add to your wintersmith project: `npm install wintersmith-nunjucks-content`
2. Add to your wintersmith config.json: `"plugins": ["wintersmith-nunjucks-content"]`
3. Create nunjucks content templates ending in `.html` or `.nunjucks`

How to add custom filters
---------------------------

From the nunjucks documentation at http://jlongster.github.io/nunjucks/templating.html#filters:

>Filters are essentially functions that can be applied to variables. They are called with a pipe operator (|) and can take arguments.

For more information on how to write custom Filters, take a look at the API documentation page at: http://jlongster.github.io/nunjucks/api#custom-filters

To use custom filters with wintersmith, put the filter in its own file stored in a filters directory. The filename has to be the name of the filter + '.js'.

so if your filter is in './filters/myfirstfilter.js' add a nunjucks section like this to your config.json:

```javascript
"nunjucks": {  
    "filterdir": "filters",
    "filters": ["myfirstfilter"]
}
```

It will be available in your content as 'myfirstfilter'

## TODO

2. Custom Tags

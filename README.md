# Serverless SEO
## A custom element to technically optimize SEO for javascript based websites

[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/p3sn/serverless-seo)

Use this webcomponent to optimize your application for the googlebot. Your application can be crawled, indexed and ranked by Google with javascript optimization only. 

This custom element takes care of updating the meta information in the `<head>` of your website and it supports structured data as well.

### Installation

```javascript
bower install -save p3sn/serverless-seo
```
Import the element in your app, for example in my-app.html

```html
<link rel="import" href="../bower_components/serverless-seo/serverless-seo.html">
```
Inside the `template` tag you can place the custom  `serverless-seo` element.

```html
<serverless-seo meta="[[metadata]]" schema="[[schemadata]]"></serverless-seo>
```
### Very basic example
It depends on the framework of your choice, but this example should give you an idea of how you can set it up.

```html
<script>
var metadata = {
	"title": 'Title of my awesome javascript generated page',
	"description": "If you see this description in the search results, you know it's working.",
	"canonical": "https://www.domain.com/preferred/url/to/index/",
}
</script>
<serverless-seo meta="{{metadata}}"></serverless-seo>
```


### Properties

#### settings
Use the settings property to set the meta fields. It should be an object like this:

```javascript
var metadata = {
	title: 'Example Title',
	description: 'Description of your page, which show up in search results',
	canonical: "https://www.domain.com/your/canonical/url", //optional
	follow: "follow", //optional, can be "follow" or "nofollow"
	index: "index" //optional, can be "index" or "noindex"
}
```

#### schema
Use the [schema.org](https://schema.org/) property to dynamically add structured data to the document. The googlebot can crawl this structured data. 

To test your structured data you can use the code snippets in the [structured data testing tool.](https://search.google.com/structured-data/testing-tool)


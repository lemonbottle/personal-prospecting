# personal-prospecting
CDN hosting for fonts, css files and javascript for Harry Sims Kajabi website Personal Prospecting. 


### How to deliver files
From this article: ![https://medium.com/javarevisited/how-to-host-your-repository-js-css-on-open-source-cdn-jsdelivr-4de252d6fbad]

Here’s how it works.

jsDelivr CDN service’s base URL is https://cdn.jsdelivr.net/gh/{username}/{repo}/, where you replace {username} with the GitHub username and {repo} with the repository name for the project.
Append that URL with the path to the file you want to access in the project. For example, consider my sample project Github-As-CDN , the JavaScript file(dummy-js-file.js) is located in the /dist directory.

```html
<html>
...
...
<script src="https://cdn.jsdelivr.net/gh/root0109/github-cdn/dist/dummy-js-file.js"></script>
...
...
</html>
```

You can also take advantage of semantic versioning by adding @{version-number} to the repository name. You can target major, minor, and patch releases as desired.

Load the latest version

```html
<script src="https://cdn.jsdelivr.net/gh/root0109/github-cdn/dist/dummy-js-file.js"></script>
Load with Major Version only
<script src="https://cdn.jsdelivr.net/gh/root0109/github-cdn@2/dist/dummy-js-file.js"></script>
Load with Major.Minor Version
<script src="https://cdn.jsdelivr.net/gh/root0109/github-cdn@2.1/dist/dummy-js-file.js"></script>
Load Exact version
<script src="https://cdn.jsdelivr.net/gh/root0109/github-cdn@1.0.0/dist/dummy-js-file.js"></script>
Load minified version
```

Add “.min” to any JS/CSS file to get a minified version — if one doesn’t exist, it will be automatically generated for you.


For this file, the link would be:
```
https://cdn.jsdelivr.net/gh/lemonbottle/personal-prospecting/styles.css
```

To import the above css file inside another css, use this code:

```
@import url('https://cdn.jsdelivr.net/gh/lemonbottle/personal-prospecting/styles.css');
```
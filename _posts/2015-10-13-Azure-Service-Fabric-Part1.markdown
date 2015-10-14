---
layout: post
title:  Azure Service Fabric, part 1&#58; Applications, Services, and Code Packages
date:   2015-10-13 17:44:33
categories: azure-service-fabric
custom_css:
- mermaid
custom_js:
- mermaid.min
---

<!--
You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve --watch`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:
-->

<div class="mermaid">
graph LR;
    app[ApplicationManifest];
    s1[ServiceManifest];
    s2[ServiceManifest];
    s1st[ServiceTypes];
    s1cp[CodePackages];
    s2st[ServiceTypes];
    s2cp[CodePackages];
    app --> s1;
    app --> s2; 
    s1 --> s1st;
    s1st --> BurgerFactory
    s1st --> MilkshakeFactory
    s1 --> s1cp;
    s1cp --> Kitchen.exe
    s1cp --> KitchenHealthMonitor.exe
    s2 --> s2st;
    s2st --> CleaningService
    s2 --> s2cp;
    s2cp --> Cleanup.exe
</div>

<!--
Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll’s dedicated Help repository][jekyll-help].

[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
-->
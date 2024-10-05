# Content Management Systems

## GitHub Pages

- [Creating and Hosting a Personal Site on GitHub](http://jmcglone.com/guides/github-pages/)
- [GitHub Pages Themes](https://pages.github.com/themes/)
- [How to set up MULTIPLE GitHub Pages websites with custom domains](https://deanattali.com/blog/multiple-github-pages-domains/)

## WordPress

- [How to install Apache, PHP and MYSQL on Windows 10 Machine](https://www.znetlive.com/blog/how-to-install-apache-php-and-mysql-on-windows-10-machine/)
- [Error With Apache 2.4 on Windows](http://weblogic-tips.com/2012/05/15/error-with-apache-2-4-on-windows-7-64-bit/)
- [HOW CAN I CREATE A PHPINFO.PHP PAGE?](https://mediatemple.net/community/products/dv/204643880/how-can-i-create-a-phpinfo.php-page)
- [How to install phpMyAdmin on Windows (youtube video)](https://www.youtube.com/watch?v=KFYXY3MT-XA)
- [The mysqli extension is missing. Please check your PHP configuration](https://stackoverflow.com/questions/10646655/the-mysqli-extension-is-missing-please-check-your-php-configuration/17413783)
- [How To Fix "No Working Transports Found" Error In EasyPHP/](http://www.howtosolutions.net/2017/01/easyphp-wordpress-no-working-transports-found-error/)

## Hugo

- [The world’s fastest framework for building websites](https://gohugo.io/)
- [Tutorial: Publish a Hugo site to Azure Static Web Apps](https://learn.microsoft.com/en-us/azure/static-web-apps/publish-hugo)
- [Youtube - Hugo Beginner Tutorial](https://www.youtube.com/watch?v=SVvihs0WfhQ&list=PLrxYIq_0LFJfimciGTP5bQhYSEu5EdAuA)
- [A Comprehensive Guide on Building Your First Site with Hugo](https://anikett.com/blog/hugo-beginner-guide/)
- [How To Build a Blazing Fast Static Site With Hugo](https://kinsta.com/blog/hugo-static-site/)
- [BUILDING YOUR HUGO SITE LOCALLY (PART 2)](https://qualityandinnovation.com/2020/12/22/building-your-hugo-site-locally-part-2/)
- [The Ultimate Guide to Understanding Hugo in 2023](https://www.markusantonwolf.com/blog/the-ultimate-guide-to-understanding-hugo-in-2023/)
- [Getting Started With Hugo - FREE COURSE YouTube](https://www.youtube.com/watch?v=hjD9jTi_DQ4)
- [Hugo - Open External Links in a New Tab](https://digitaldrummerj.me/hugo-links-to-other-pages/)

```shell
layouts/_defaults/_markup/render-link.html is incorrect, should be
layouts/_default/_markup/render-link.html
```

To include a link and target attribute in the Hugo figure shortcode, you can modify the shortcode to handle these parameters. Here’s how you can do it:

Create or Edit the Shortcode:
If you haven’t already, create the shortcodes directory in your Hugo site’s layouts directory.
Inside the shortcodes directory, create or edit the figure.html file.
Add the Following Code:
Update the figure.html file with the following code to include link and target attributes:
HTML

```shell
<style>
  .image-container {
    position: relative;
    display: inline-block;
  }
  .image-title {
    position: absolute;
    bottom: 10px;
    left: 10px;
    color: white;
    background-color: rgba(0, 0, 0, 0.5);
    padding: 5px;
    border-radius: 3px;
  }
</style>
<figure class="image-container">
  {{ if .Get "link" }}
    <a href="{{ .Get "link" }}" target="{{ .Get "target" }}">
      <img src="{{ .Get "src" }}" alt="{{ .Get "alt" }}">
    </a>
  {{ else }}
    <img src="{{ .Get "src" }}" alt="{{ .Get "alt" }}">
  {{ end }}
  <figcaption class="image-title">{{ .Get "title" }}</figcaption>
</figure>
AI-generated code. Review and use carefully. More info on FAQ.
Use the Shortcode in Your Content:
In your markdown file, use the shortcode like this:
{{< figure src="/path/to/image.jpg" alt="Alt text" title="Image Title" link="https://example.com" target="_blank" >}}

```

This will render the image with a clickable link that opens in a new tab (or the specified target) and overlay the title on the image itself.

- To run site locally
install hugo
clone repo
run

```shell
git submodule init
git submodule update
```

This creates "resources folder outside repo ?

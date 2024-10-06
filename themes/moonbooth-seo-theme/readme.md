# Readme

Thank you for purchasing the MoonBooth SEO Theme for Hugo.

It has more SEO features than any other theme. You can read more about the theme [here](https://moonbooth.com/hugo/seo-theme/), and see the documentation [here](https://moonbooth.com/hugo/seo-theme-documentation/).

## Licence

You can use this theme on as many of your websites as you wish, including unlimited client websites. However, if people outside your organisation wish to use it, please ask them to purchase it here. Thank you.

## Version

This is version 1.0.8 of the theme.

## Changelog

All dates below AEST / AEDT.

### Version 1.0.8

_November 21st, 2022_

In this update:

-  New mobile breakpoints at 1060 and 530 pixels; these replace the previous solitary breakpoint at 900 pixels. This means the theme now looks better on tablets such as iPad.
-  CSS support for H4 headings: H4 headings are now visually distinct from H3 headings.
- CSS support for a second level inside the (always-optional) table of contents for blog posts. Previously, only H2 headings were visually supported; now you can enable H3 headings as well. To enable this, apart from updating the theme to this version (`v.1.0.8`), you'll need to change the relevant parts of your config.toml so it goes from this:

```
[markup]
	[markup.tableOfContents]
		endLevel = 2
		ordered = false
		startLevel = 2
```

... to this:

```
[markup]
	[markup.tableOfContents]
		endLevel = 3
		ordered = true
		startLevel = 2
```

When configured this way, your table of contents will feature:

- H2 headings with no indent and no bullet/number/decoration of any sort
- H3 headings with an indent and a checkmark in pure CSS (no HTTP request) in your specified accent colour.
- You can see an example [here](https://moonbooth.com/hugo/vs-code/)

### Version 1.0.7

_April 5th, 2022_

Now if you include parameter called `netlify_cms` in your config file `[params]` and set it to `true`, the two Netlify CMS scripts will automatically be included on the homepage; one just before the closing `</head>` tag and the other just before the closing `</body>` tag, [as required by Netlify CMS](https://www.netlifycms.org/docs/add-to-your-site/). (It will also appear on paginated versions of the homepage.)

Note that there are more steps required than just the above when it comes to setting up Netlify CMS for Hugo.

For more, see the link above or the [theme documentation](https://moonbooth.com/hugo/seo-theme-documentation/).

### Version 1.0.6

_April 5th, 2022_

Now if you include a Google Analytics id (e.g. `UA-123456789-1`) as the value of a parameter called `ga_id` in the `[params]` section of your config file, your GA code will automatically be included at the top of the `<head>` section of every page in production.

Localhost (i.e. local server) pages won't render the GA code, so you don't inflate your page views and other metrics when working on or testing your site.

If you want to test the GA code locally, you can simulate production mode with `hugo server --environment production`.

For more, see the [theme documentation](https://moonbooth.com/hugo/seo-theme-documentation/).


### Version 1.0.5

_April 4th, 2022_

Now if you include a `.png` logo called `opengraph.png` (should be 1200px wide x 630px high) in the root of `/static`, you'll get Facebook and Twitter Open Graph metadata, which means your content will look better when shared on those platforms.

You can see an example of the required `.png` image at [moonbooth.com/opengraph.png](https://moonbooth.com/opengraph.png/). For more, see the [theme documentation](https://moonbooth.com/hugo/seo-theme-documentation/).

### Version 1.0.4

_March 25th, 2022_

Instead of the pure CSS "active dot" released in v1.0.3 of the theme, the active footer link now gets a pure CSS triangle arrow indicator. See [MoonBooth.com/about/](https://moonbooth.com/about/) for an example.

### Version 1.0.3

_March 20th, 2022_

The active footer link now gets an "active dot" displayed before its anchor text. See [MoonBooth.com/about/](https://moonbooth.com/about/) for an example. Previously, the anchor text was bolded and there was no "active dot" displayed.

Also, list items `<li>` in the body copy or anywhere other than the footer now get a checkmark in your accent colour---built in pure CSS---instead of a bullet. See [MoonBooth.com/about/](https://moonbooth.com/about/) for an example.

### Version 1.0.2

_March 17th, 2022_

**Breaking change:** Updated footer link logic to reflect forthcoming changes to Hugo behaviour around `.Path`.

As per the warning when serving locally:

> `.Path` when the page is backed by a file is deprecated and will be removed in a future release.

This change isn't required as of the current Hugo version (0.94.2), but it will be at some unspecified point in the future.

The breaking change is that you now need an `_index.md` file (can be totally blank, mine is) in the root of your `/content/` folder if you want your footer links to work on the homepage.

### Version 1.0.1

_March 9th, 2022_

Posts with `noindex: true` in their YAML front matter will no longer appear in the list of posts in the section homepage. This change is retroactive.

### Version 1.0

_February 2nd, 2021_

Initial commit.

## Author & contact

This theme was made by me, Ron Erdos. You can contact me [here](https://moonbooth.com/about/#how-to-contact-me).

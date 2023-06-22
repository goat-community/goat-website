## Content File Name Format
Avoid:
- Spaces
- Brackets
- Uppercase 
- Underscores

Standardise :
- Lower case only
- Use letters, numbers and dashes only

Example collections:
```
_docs/some-file-name.md
_docs/some-file-name-de.md
```

Example post (posts require date prefix):
```
_posts/2020-06-26-some-file-name.md
```

## Post Excerpt
The blog post cards display the first paragraph of the posts content as excerpt. Alternatively you can define a custom excerpt in the post front matter:
```yml
excerpt: Some custom excerpt text
```
## Post Image Overlay
Overlay color can be overridden in the post front matter:

Semi-transparent overlay using RGBA color:
```yml
image_overlay: "rgba(255,255,255,0.7)"
```

Or set full color background when not using an image:
```yml
image_overlay: "#19B037"
```

## Page Alert
Display a page alert (abover navigation) on any page by using the following front matter:
```yml
alert:
  content: "[Help us to improve GOAT by participating in this survey](https://www.umfrage.sv.bgu.tum.de/index.php/837925?lang=en)"
```

## Content includes

### Mark text
Emphasis, aka italics, restyled to *mark some text* in content, use `*asterisks*` or `_underscores_`.

### Image sources
All images are located in `/uploads/` folder, this location reference can be changed in `_config.yml`:
```yml
uploads: /uploads/
```
Upload images to `/uploads/` directory or it's subfolders eg `/uploads/blog/`.

All images accros the theme (logo, content, authors, headers) can be set either as full external URL that includes `http`:

```yml
image: https://website.com/someimage.jpg
```

or local image located directly in `/uploads/` folder or it's subfolders:


```yml
image: some-image.jpg
```
```yml
image: blog/some-image.jpg
```

### Image Include
Use the following include to add an image to a page:

```yml
{% include image.html src="alexander.jpg" alt="Alt for image" %}
```

#### Attributes

| Attribute | Description | Choices |
| --- | --- | --- |
| src | Image file source | image file name, upload the image to `/uploads/` directory or external image URL |
| alt | Image alt text | string |
| align | Align within text | left, right |
| caption | Image caption | string |
| lightbox | Display image in popup lightbox on a click | true |
| maxwidth | Maximum image width | px |
| maxheight | Maximum image height | px |

### Responsive Videos
Add the `data-uk-responsive` attribute to `iframe` tag to make the video responsive, example:
```
<iframe class="embed-responsive-item" src="https://player.vimeo.com/video/333129999" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen data-uk-responsive width="1920" height="1080"></iframe>
```
Note: the iframe must have `width` and `height` specified for the responsiveness to work.

### Alerts Include
Add alerts to content using the following include:

```yaml
{% include alert.html style="primary" text="Cras at dolor eget urna varius faucibus tempus in elit." %}
```
#### Attributes

| Attribute | Description | Choices |
| --- | --- | --- |
| text | Alert text | string |
| style | Alert style | primary, success, warning, danger, leave blank for default |

### Label Include
Add labels to content using the following include:

```yaml
{% include label.html text="Success" style="success" %}
```

#### Attributes

| Attribute | Description | Choices |
| --- | --- | --- |
| text | Label text | string |
| style | Label style | success, warning, danger, leave blank for primary |


### Button Include
Add buttons to content using the following include:

```yaml
{% include button.html text="Button text" url="#" style="primary" size="xlarge" width="full" %}
```

#### Attributes

| Attribute | Description | Choices |
| --- | --- | --- |
| text | Button text | string |
| url | Button url | page permalink or full URL |
| style | Button style | default, primary, success, warning, danger, primary-outline, success-outline, warning-outline, danger-outline, custom hex or rgb color value |
| size | Button size | small, large, xlarge, leave blank for default size |
| width | Button will take up full width | full |


### Scroll to Top Include
Add scroll to top icon to content using the following include:
```yaml
{% include totop.html %}
```

### Markdown
For general markdown syntax see [Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

## Team Members / Authors
Add/edit team authors info in `data/authors.yml:
```yml
pajares:                # Author handle that is referenced in post front matter
  name:                 Elias Pajares
  avatar:               https://via.placeholder.com/380
  title:              
    en:                 Chair for Urban Structure and Transport Planning    
    de:                 Chair for Urban Structure and Transport Planning
  avatar:               https://via.placeholder.com/380
  bio:
    en:                 En Lorem Ipsum is simply dummy text of the printing and typesetting industry
    de:                 De Lorem Ipsum is simply dummy text of the printing and typesetting industry
  url:                  # website url
  email:                
  website:
  facebook:             
  flickr:
  dribbble:
  github:               "https://github.com/username"
  googleplus:
  instagram:            
  linkedin:             
  pinterest:
  twitter:              
  vimeo:
  youtube:
```

Assign single or multiple authors to a blog post in the from matter:

Single author:
```yml
---
title:  "Major extensions are coming"
author: [pajares]
---
```
Multiple authors:

```yml
---
title:  "Major extensions are coming"
author: [pajares, jehle, hassine]
---
```

## Translation

### Theme Strings

Theme strings can be translated in `_data/translation.yml`:

```yml
en:
  previous:                   "Previous"
  next:                       "Next"
  related_posts:              "Related Posts"
  menu:                       "Menu"
  navigate_docs:              "Navigate Documentation"
  recent_posts:               "Recent Posts"

de:
  previous:                   "Previous"
  next:                       "Next"
  related_posts:              "Related Posts"
  menu:                       "Menu"
  navigate_docs:              "Navigate Documentation"
  recent_posts:               "Recent Posts"
```

### Navigation
Header, footer and mobile navigation strings can be translated in the following files:
```
_data/navbar.yml
_data/mobile.yml
_data/footer.yml
```
Example:
```yml
- title: 
    en: GOAT
    de: GOAT
  url: versions/

- title: 
    en: Quickstart
    de: Quickstart
  url: videos/
```

### Pages
Create English pages in theme root folder with the following example front matter:
```yml
---
title: Imprint & Privacy
width: small
lang: en
---
```
The page width can accept the following options: `full | small| xsmall`.

German languages pages are loacated in `/de/` folder with the following example front matter:
```yml
---
title: Imprint & Privacy
width: small
lang: de
---
``` 

### Docs Posts

Both English and German docs posts are located in `_docs/` folder.

Example English doc front matter:
```yml
---
title: What is GOAT?
permalink: /docs/about/
lang: en
---
```

Example German doc front matter:
```yml
---
title: What is GOAT?
permalink: /de/docs/about/
lang: de
---
```

### Blog Posts

English blog posts are located in `_posts/` folder, German blog posts are located in `/de/_posts/` folder.

Example English post front matter:
```yml
---
title:  "Development path of GOAT"
author: [pajares]
lang: en
tags: [en]
categories: [news]
---
```

Example German post front matter:
```yml
---
title:  "Development path of GOAT"
permalink: /de/goat-goes-public/
author: [pajares]
lang: de
tags: [de]
categories: [news]
---
```

Categories eg `categories: [news, updates]` are required for displaying related posts on single post page. 

German post requires a permalink with a `/de/` prefix. Both `lang` and `tag` values are required.

Setting multiple posts authors:

```yml
---
author: [pajares, jehle, hassine]
---
```

### Video Posts
Both English and German video posts are located in `_videos` folder.

Example English video post front matter:
```yml
---
title: Comparison population density and walkability
image: videos/walkability_population_heatmap.png
vimeo: 370376888 
lang: en
---
```

Example German video post front matter:
```yml
---
title: Comparison population density and walkability
image: videos/walkability_population_heatmap.png
vimeo: 370376888
lang: de
---
```

The `vimeo: 370376888` variable requires Vimeo video ID.

## Customization

To modify the primary color, open `/_sass/theme/variables.scss` and replace the color values e.g.:

```scss
$global-primary-background:                   #05c896;
```

Further style customization can be done in the following files:
```
/_sass/theme/mixins.scss
/_sass/theme/variables.scss
/assets/css/main.scss
```

## Development

### Build process
Install [UIkit](https://getuikit.com/) font end framework dependency via Npm:
```bash
npm install
```
Enable live browser reload with the following:
```bash
bundle install && bundle exec jekyll s --livereload
```

Use the following commands to compile js scripts:
```bash
npm run dev
```
Compile and minify:
```bash
npm run build
```

### Hooks
There are two hook include files that simplify adding content or scripts in the theme locations:
- `_includes/hook-head.html`
- `_includes/hook-pre-closing-body.html`


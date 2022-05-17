![Obsidian Image Gallery](assets/obsidian-image-gallery-header.jpg)

# Obsidian Image Gallery
Obsidian Image Gallery is a zero setup masonry image gallery for [Obsidian](https://obsidian.md/).

**Table of Contents**
- [Requirements](#requirements)
- [Usage](#usage)
- [Settings](#settings)
- [Notes](#notes)
- [Examples](#examples)
- [Acknowledgments](#acknowledgments)
- [License](#license)
- [Contacts](#contacts)

## Requirements

- [Obsidian](https://obsidian.md/) `(ver >= 0.14.6)`
- A folder(s) of local images located somewhere in your vault

## Installation

Obsidian Image Gallery can be installed from within Obsidian, as for [every other community plugin](https://help.obsidian.md/Advanced+topics/Community+plugins#Discover+and+install+community+plugins).

## Usage

To create a dynamic gallery, add one of the following code blocks to a note (make sure to customize the path!):

For a horizontal masonry:
````
```img-gallery
path=Attachments/Folder
type=horizontal
```
````

For a vertical masonry:
````
```img-gallery
path=Attachments/Folder
type=vertical
```
````

Take a look at [settings](#settings) to see how to tweak some properties of the gallery; the examples available above are the most minimal configuration possible.

In *[Live Preview](https://help.obsidian.md/Live+preview+update)* mode, the gallery will be generated after moving the cursor outside the code block. Using the regular *Source Mode*, press `cmd+e` (or `ctrl+e`) to trigger Obsidian's Note Preview.

## Settings

Settings can be customized in any order, and optional properties default to the values outlined in the list of bullet points below:
- `path=Attachments/Folder` (**Required**, path relative to the root of your vault)
- `type=horizontal` (**Optional**, type of masonry `horizontal` or `vertical`)
- `gutter=8` (**Optional**, spacing between the images)
- `radius=0` (**Optional**, border radius of the images)
- `sortby=ctime` (**Optional**, sort by `ctime`, `mtime`, or `name`)
- `sort=desc` (**Optional**, order of sorting: `desc` or `asc`)

Applicable to `type=horizontal` only:
- `height=260` (**Optional**, height in px of all rows)

Applicable to `type=vertical` only:
- `columns=3` (**Optional**, number of columns for desktop)
- `mobile=1` (**Optional**, number of columns for mobile)

## Notes:
- For `path` there is no need to specify the name of the vault
- As mentioned in the [Requirements](#requirements) section, only local images are accepted. This plugin was designed with a specific use case in mind: create a gallery from a folder of images with as little setup as possible.
- Make sure the images to embed have a reasonable size: generating a masonry with 60 4k photos will most likely slow down the app to a crawl!

An additional note about the orientation of the masonry vs. the distribution of its images: [until a true masonry layout](https://drafts.csswg.org/css-grid-3/) is available for native `css` grids, the sorting of the vertical version is a hit or miss. This is because the flow of its elements goes from top to bottom (see [this article](https://css-tricks.com/piecing-together-approaches-for-a-css-masonry-layout) for more info about it.) If sorting is critical, please rely on the horizontal version; its images are sometimes cropped, but their ordering is way more intuitive.

## Examples:
![Obsidian Image Gallery - Examples](assets/obsidian-image-gallery-examples.jpg)

## Acknowledgments
All photos in the header are by various photographers and available on [Unsplash](https://unsplash.com/s/photos/architecture).

## License
![https://github.com/lucaorio/obsidian-image-gallery/blob/master/license](https://img.shields.io/badge/license-MIT-blue.svg)

## Contacts
- Twitter: [@lucaorio_](http://twitter.com/@lucaorio_)
- Website: [lucaorio.com](http://lucaorio.com)
- Email: [luca.o@me.com](mailto:luca.o@me.com)

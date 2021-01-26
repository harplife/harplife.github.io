# Image Manipulation on Multiple Images

[Repository](https://github.com/harplife/image_view)

Desktop Application where user can browse local images in a grid-like fashion, with a bit of image manipulation.

For example,

- user can select "grey" and all images will be shown in grey-scale.
- user can select "complementary" and all the images will be shown in colors that are complement to the original colors.
- blur
- rain drops
- sort by dominant color
- sort by aspect

## Functions

- [ ] Web Application (w/ Node.js http)
- [ ] Grid Layout
- [ ] Image Preload with Promise
- [ ] Image Manipulation
- [ ] Scroll & Load

## Thoughts, Notes, Issues

- I've tried two grid systems, and each of them have some kind of flaws.
- Loading all images at once causes issues.
- Scroll & Load seems to break one of the grid system. Perhaps it's best to query list of images, preload grid system with image size, and then load images with promise.

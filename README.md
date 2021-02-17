# React Photo Gallery

* Simple responsive photo gallery
* Creates a grid of images, depending on how many images you give to it
* Comes with an integrated lightbox (built with Swipper JS)
* Handles basic keyboard control (for computer users), and touch control for mobile devices

# Minimal Setup Example

To build some examples locally, clone this repository :
> git clone https://github.com/oulanbator/react-photo-gallery

Then install dependencies and run:
> npm install
> 
> npm start

For the purpose of this demo, you can simply run the React App and then open localhost:3000 in a browser. The gallery will load images from https://picsum.photos/.

By default, 23 images will be loaded (starting on id 11) from the picsum API. You can play with this behaviour with "picsumStartId" and "numberOfImages" props :

Open "/src/index.js", then change this line as follow (e.g.) :
> \<Gallery picsumStartId={123} numberOfImages={50} /\>

That's it !

# How it works

This layout uses an algorithm to "split" the source image stream into different blocks (divs) of 8 images each. The remaining images will then be divided, according to their number, into blocks of 4, 2 or 1 image.  This will allow the React component to always adapt to the size of the gallery.

The layout is ensured thanks to the CSS file, and can easily be adapted if necessary, if the classes used and the basic HTML structure are respected. 

Designed to be responsive, this grid adapts to different screen sizes.
The lightbox module has been integrated with the SwiperJS library in order to easily integrate onTouch events. The additional CSS allows the lightbox to adapt to different image formats, and different screens, in order to always display the entire image in the viewport.

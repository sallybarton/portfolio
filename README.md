# portfolio
A simple, responsive portfolio website designed to make content updates and playing with color platettes easy. You can see the end result here:
http://brightumbrella.com

The navigation is for a home page and 3 flat content pages: Process, About and Contact. 

****************** HOME PAGE ******************
The home page has 4 tiles that navigate to pages not on the main navigation. In an attempt making keeping my portfolio up-to-date I have structured it such that the tile images and pages are named generically to indicate their position in the 2x2:

-------------------------------------------------
| Top Left              | Top Right             |
| /images/tile_tl.svg   | /images/tile_tr.svg   |
| featured_tl.php       | featured_tr.php       |
|                       |                       |
-------------------------------------------------
| Bottom Left           | Bottom Right          |
| /images/tile_tl.svg   | /images/tile_tr.svg   |
| featured_tl.php       | featured_tr.php       |
|                       |                       |
-------------------------------------------------

When updating a featured project, the page currently titled "featured_*.php" can be renamed to something logical for the project it describes and put in the /portfolio directory. The PHP include for the footer of that file should be updated to "/inc_footBack.html" and the "tile_*" image put in the /portfolio/images directory, replacing "*" to match the new project file name. You can then update the /portfolio/index.php to add the new tile as appropriate. The portfolio directory page is not available from the main navigation but can be found at: yourURL.com/porfolio, useful if you want to send out a complete list of your work or if - mid-presentation - it is relevant to show a project that isn't currently featured.

****************** COLORS AND WASH ******************
The palette has 4 colors in it and each color has a HEX, RGA and ALPHA versions. The number associated with each indicates the order it appears in the nav: therefore color for home is @1HEX (plus, @1rga and @1alpha). The current implementation doesn't use the RGB values but I left them there because it was useful for some of the variations I played with.

NOTE: These colors are used for links too.

****************** IMAGE BANDS ******************
While the single full-width images each require their own class (see image bands on process page for example and update to show your own images by editing classes starting .bgImg_ in the LESS file), you can also put 2 images side-by side in the band, as seen in /portfolio/OL_vision.php. These pages are responsive, so on phones and smaller tablets only the first image will show.

****************** IMAGE LABELS ******************
The image bands have short explainer text that appears in the bottom right of the area occupied by the images and the homepage tiles also have labels that appear on rollover. These are simply spans with a .hexBG class to match the alpha wash on the featured pages, or a link in the homepage LIs with color assigned to match the wash at that position. 

****************** MAIN.LESS ******************
This file has the HEX, RGA, and ALPHA values for the colors. It also has the a variety of alternative palettes that I played with and kept in there because rainbows or shade of blue might be more your thing. This file also declares the text color and font for the site.

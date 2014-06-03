<!-- ## Examples (each section below contains link to example post) -->

## Headings and Paragraphs

Paragraphs are separated by pressing the `enter` key in the visual editor, and pressing it twice in the text editor. 

To make a paragraph into a heading, wrap it in a header tag:

	<h1>Header one</h1>
	<h2>Header two</h2>
	<h3>Header three</h3>
	<h4>Header four</h4>
	<h5>Header five</h5>
	<h6>Header six</h6>

Lower-numbered header tags are more important than higher-numbered header tags, and have additional weight when search engines index your content. 

## Photos and Video

Inserting photos and videos is as easy as clicking the "Add Media" button, uploading the media, adding the caption, description, alternate text, title and credit, and then saving. Click "Insert into Post" to insert the image at the current location of the cursor in the post editor. 

### Slideshows

To create a slideshow in a post, click the "Add Media" button in the post editor. In the left-hand sidebar of the popup, choose "Create Gallery." Click on images you want to add to the gallery. To remove an image from the selection, un-check it. Once you have chosen all items for your slideshow and checked their captions, click "Create a new gallery." Order your images by drag-and-drop, then click "Insert gallery."

In the visual editor, you will see a representation of your gallery. In the text editor, you will see a shortcode similar to `[gallery link="file" columns="1" ids="1628,1686,1687,1045"]`

## Tabular Data

Inserting tables is as easy as opening the text editor tab and writing a table using the HTML `<table>` tag. For more information about `<table>`, try these resources:

- http://teamtreehouse.com/library/html/tables/rows-and-cells
- http://www.idocs.com/tags/tables/index_famsupp_27.html

If you are embedding a Google Doc, consider using INN's [responsive tables](https://github.com/INN/responsive-tables) tool to make sure that your table is easily readable on all devices. 

## Lists

Lists can be made with the numbered or bulleted list buttons in the visual editor, or with the `ol` and `ul` buttons in the text editor. It is possible to have a list within a list, for an indented liest. 

## Asides, blockquotes, and pull quotes

In the visual editor, find the "Module Wrapper" button. Highlight the text for your quote, then click the Module Wrapper button. Choose whether the text is an aside or a pull quote, which way to align it, and how wide it should be.

To remove aside or pull quote formatting, switch to the text editor and remove the `<aside ... > </aside>` tags from around the text. You can also change the formatting in this fashion, by editing the classes listed in the aside's `class=""` attribute:

- `align-left`/`align-center`/`align-right`: Quote alignment. Text will flow around 
- `half`/`full`: width of the aside, in terms of the column of text containing the story
- `type-aside`/`type-pull-quote`: changes visual styling of aside

## Embedding videos

If you are embedding a video from YouTube, Vimeo or another site, simply paste that site's embed code into the WordPress text editor. 

    <iframe width="560" height="315" src="//www.youtube.com/embed/sGpxfVxQkfE" frameborder="0" allowfullscreen></iframe>
    
    <iframe src="//player.vimeo.com/video/84713706" width="500" height="375" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
    
You may want to replace the fixed-width `width` attribute `width="500"` with the responsive attribute `width="100%"`. This will ensure that your video is sized appropriately on all screens.

## Page Breaks

## Less Common HTML Elements

Try them out and see what happens. If it's massively broken, [file an issue](https://github.com/inn/Largo/issues/new) to let us know. 

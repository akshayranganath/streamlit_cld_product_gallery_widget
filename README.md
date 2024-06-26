# streamlit_cld_product_gallery_widget

Streamlit component that allows you to embed Cloudinary's [Product Gallery Widget](https://cloudinary.com/documentation/product_gallery) into your application.

## Installation instructions 

```sh
pip install streamlit_cld_product_gallery_widget
```

## Usage instructions

```python
import streamlit as st

from streamlit_cld_product_gallery_widget import cld_product_gallery_widget

cld_product_gallery_widget(
    cloudName = 'demo',
    mediaAssets=[{'tag':'logo'}]
)
```

## Detailed Usage

Cloudinary's Product Gallery is an interactive user interface for displaying your products to your users on your website or application. In this Streamlit app, we expose a few of the available options for the product gallery. For full details, please refer to the [api documentation](https://cloudinary.com/documentation/product_gallery_reference).

| Parameter           | Purpose                                                                                                                                                                                                            | Default Value                                 |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------- |
| cloud_name          | Name of your Cloudinary product environment                                                                                                                                                                        | None. Required value                          |
| mediaAssets         | Populates the widget with all the media assets given as an array of assets. The individual assets in the array can be described either by an Asset object or by a PublicID string (as a shortcut for images only). | None. Required value                          |
| placeholderImage    | Whether to load and display a low-quality blurred placeholder image while waiting for the higher quality image, instead of a loading spinner.                                                                      | TRUE                                          |
| sortProps           | An object that defines how to sort the assets for display in the Product Gallery.                                                                                                                                  | { "source": "public_id", "direction": "asc" } |
| viewportBreakpoints | An array of breakpoints for the viewport (browser window), together with the Product Gallery configuration parameters to override when the width of the Product Gallery widget is less than the given breakpoint   | None                                          |
| aspectRatio         | The aspect ratio of the main viewer.                                                                                                                                                                               | "square"                                      |
| imageBreakpoint     | The step size for rounding up the width of responsive images in pixels.                                                                                                                                            | 250                                           |
| videoBreakpoint     | The step size for rounding up the width of responsive videos in pixels.                                                                                                                                            | 250                                           |
| preload             | An array indicating which media assets should be preloaded into the browser cache when the Product Gallery widget is initialized. [] indicates load the first image                                                | []                                            |
| transition          | The effect to apply while transitioning between assets.                                                                                                                                                            | slide                                         |
| zoom                | Whether to activate the zoom functionality for images.                                                                                                                                                             | TRUE                                          |

## Git Repo

The code is available here: [https://github.com/akshayranganath/streamlit_cld_product_gallery_widget](https://github.com/akshayranganath/streamlit_cld_product_gallery_widget)
# Data
__Patch__ --> 1 sq km2 area<br>

__S2__ --> 128x128 Image - 10 bands - 10 m* - 43 dates so (43, 10, 128, 128)**<br>
__Annotations__ --> panoptic: instance segmentation + semantic segmentation<br>
i.e., instance index + semantic label for each pixel<br>
TODO<br>
assigning a unique index to each object instance<br>
assigning a label to each pixel indicating the type of object or land cover<br>
Instance Index: Each object or instance within the images is assigned a unique index, allowing for individual identification and tracking.<br>
Semantic Label: In addition to instance indices, semantic labels are assigned to each pixel, providing information about the type of object or land cover represented by that pixel.<br>

__S1__ --> 128x128 Image - __ bands - __m _(varies across bands?)_ - 70+70 dates so (43, 10, 128, 128)






# Note
*All bands are resampled to a 10m/pixel resolution with bilinear interpolation<br>
*asfd [S2 Bands](https://content.satimagingcorp.com/media2/filer_public_thumbnails/filer_public/44/9c/449caa01-64b9-417f-9547-964b66465554/cms_page_media1530image001.png__525.0x426.0_q85_subsampling-2.jpg)
**(T, C, H, W)


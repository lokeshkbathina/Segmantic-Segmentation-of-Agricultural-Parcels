# Data
__Patch__ --> 1 sq km2 area<br>

__S2__ --> 128x128 Image - 10 bands - 10 m* - 43 dates<br>
__Annotations__ --> ANNOTATIONS (ParcelIDs, TARGET) + INSTANCE ANNOTATIONS (HEATMAP, INSTANCES, ZONES)<br>

ANNOTATIONS - Semantic?<br>
INSTANCE ANNOTATIONS - Instance?

_Semantic segmentation_ involves classifying each pixel in an image into predefined classes or categories. Each pixel is assigned a label that represents the category it belongs to.<br>
_Instance segmentation_ goes a step further by not only assigning semantic labels to pixels but also distinguishing between individual instances of the same class. Each object or instance in the image is assigned a unique identifier.

__Each patch pixel is annotated with a semnatic label (class) corresponsing to either the parcels' crop type or the background class.__ <br>
__The pixels of each unique parcel in the patch receive a corresponsing instance label.__

| -         | -                  | -       | Pixel Values |      
|-----------|:------------------:|---------|:------------:|
| S2        | (43, 10, 128, 128) | YES     | Class Values |
| ParcelIDs | (128, 128)         |         | Class Values |
| TARGET    | (3, 128, 128)      |         | Class Values |
| HEATMAP   | (128, 128)         | aon NO  | Class Values |
| INSTANCES | (128, 128)         |         | Class Values |
| ZONES     | (128, 128)         | aon NO  | Class Values |

--> panoptic: instance segmentation + semantic segmentation<br>
i.e., instance index + semantic label for each pixel<br>
TODO<br>
assigning a unique index to each object instance<br>
assigning a label to each pixel indicating the type of object or land cover<br>
Instance Index: Each object or instance within the images is assigned a unique index, allowing for individual identification and tracking.<br>
Semantic Label: In addition to instance indices, semantic labels are assigned to each pixel, providing information about the type of object or land cover represented by that pixel.<br>

# Mismatch
S2 - 2433 but got 2468
Annotations - 2433x2+1 + 2433x3


__S1__ --> 128x128 Image - __ bands - __m _(varies across bands?)_ - 70+70 dates so (43, 10, 128, 128)


Optical images contain spectral information and C-band radar captures useful geometrical information and is immune to cloud cover<br>






# Note
*All bands are resampled to a 10m/pixel resolution with bilinear interpolation<br>
*All Bands except the atmospheric bands B01, B09, and B10 [(S2 Bands)](https://content.satimagingcorp.com/media2/filer_public_thumbnails/filer_public/44/9c/449caa01-64b9-417f-9547-964b66465554/cms_page_media1530image001.png__525.0x426.0_q85_subsampling-2.jpg)<br>
**(T, C, H, W)


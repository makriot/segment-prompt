# Object segmentation with SAM and CLIP using prompts
Pipeline for segmenting objects in images using text prompts with SAM (Segment Anything Model) and CLIP models.

## How it works
First, images are passed to the Segment Anything Model (SAM) to obtain segmentation masks. Next, the segmented objects are enclosed in bounding boxes, which are then used to create new images. These new images are passed to the CLIP model to retrieve embeddings for the segmentation masks. Following this, text embeddings are obtained, and cosine similarities between the text and segmentation masks are measured. The masks are then filtered based on a specified threshold and concatenated using an "or" operation. This final result represents the output of the pipeline.

## Examples of work
### Chairs in a kitchen
![](/.github/images/chairs_kitchen.png)
### Bed in a bedroom
![](/.github/images/bed_bedroom.png)
### Chairs in a bedroom
![](/.github/images/chairs_bedroom.png)

# WasteDatasets Dataset Catalogue
A curated catalogue of waste-related openly available image datasets, organized for browsing, filtering, and downloading detection, segmentation, and classification data.

Website - https://wastedatasets.com/

## Dataset Summary

| Dataset | Slug | Task | Annotation fields | Samples | Classes | Source |
| --- | --- | --- | --- | ---: | --- | --- |
| COCO | `coco` | Object detection, instance segmentation | `detections`, `segmentations` | 22,958 | `cell phone`, `clock`, `hair drier`, `keyboard`, `laptop`, `microwave`, `mouse`, `oven`, `refrigerator`, `remote`, `toaster`, `toothbrush`, `tv` | [COCO Dataset](https://cocodataset.org/#home) |
| TrashNet | `trashnet` | Image classification | `classification` | 2,527 | `cardboard`, `glass`, `metal`, `paper`, `plastic`, `trash` | [TrashNet](https://github.com/garythung/trashnet) |

## Class Coverage

| Class | Dataset | Task |
| --- | --- | --- |
| `cardboard` | TrashNet | Classification |
| `cell phone` | COCO | Detection, segmentation |
| `clock` | COCO | Detection, segmentation |
| `glass` | TrashNet | Classification |
| `hair drier` | COCO | Detection, segmentation |
| `keyboard` | COCO | Detection, segmentation |
| `laptop` | COCO | Detection, segmentation |
| `metal` | TrashNet | Classification |
| `microwave` | COCO | Detection, segmentation |
| `mouse` | COCO | Detection, segmentation |
| `oven` | COCO | Detection, segmentation |
| `paper` | TrashNet | Classification |
| `plastic` | TrashNet | Classification |
| `refrigerator` | COCO | Detection, segmentation |
| `remote` | COCO | Detection, segmentation |
| `toaster` | COCO | Detection, segmentation |
| `toothbrush` | COCO | Detection, segmentation |
| `trash` | TrashNet | Classification |
| `tv` | COCO | Detection, segmentation |

## Downloaded File Structure

Downloads from the WasteDatasets website are exported as ZIP files. A ZIP contains the selected images, or the current filtered view if no samples are selected. When labels are filtered on the website, the downloaded annotations are filtered to the same selected labels.

```text
download.zip
  coco/
    cell_phone/
      image_001.jpg
    tv/
      image_002.jpg
  trashnet/
    cardboard/
      cardboard1.jpg
    plastic/
      plastic1.jpg

  annotations/
    README.txt
    fiftyone_samples.json
    coco_instances.json
    classifications.csv
    per_image/
      coco/
        cell_phone/
          image_001.jpg.json
      trashnet/
        cardboard/
          cardboard1.jpg.json

  download_manifest.txt
```

| Path | Present when | Description | Common use |
| --- | --- | --- | --- |
| `<source>/<label>/<image>` | Always | Downloaded media files grouped by dataset/source and label | Direct image training or manual inspection |
| `annotations/fiftyone_samples.json` | Always | Full FiftyOne sample records for every downloaded image | Re-import into FiftyOne or preserve complete metadata |
| `annotations/per_image/...json` | Always | One JSON sidecar for each image, matching the image folder path | Easy per-image lookup without parsing one large file |
| `annotations/coco_instances.json` | Detection/segmentation labels are present | COCO-style `images`, `annotations`, and `categories` with boxes and masks where available | Train/evaluate detection or segmentation models with COCO-compatible tooling |
| `annotations/classifications.csv` | Classification labels are present | CSV rows containing image path, source dataset, label field, and class label | Train/evaluate classification models or load into pandas |
| `annotations/README.txt` | Always | Short explanation of the ZIP contents | Quick reference after download |
| `download_manifest.txt` | Always | Download metadata such as sample count and export time | Reproducibility and bookkeeping |

## How To Use Downloads

### Classification

For classification datasets such as TrashNet, use `annotations/classifications.csv` as the label file and load images from the `media_path` column.

```python
import pandas as pd

labels = pd.read_csv("annotations/classifications.csv")
print(labels[["media_path", "label"]].head())
```

Each `media_path` points to an image inside the ZIP, for example:

```text
trashnet/cardboard/cardboard1.jpg
```

### Detection And Segmentation

For COCO-style detection or segmentation data, use:

```text
annotations/coco_instances.json
```

This file follows the standard COCO structure:

```text
images[]       image records and file paths
annotations[]  bounding boxes and segmentation masks where available
categories[]   class names and category IDs
```

The `file_name` field in each COCO image record points to the downloaded image path inside the ZIP, for example:

```text
coco/tv/000000123456.jpg
```

## Notes
- Dataset ownership, citation requirements, and license terms remain with the original dataset publishers.

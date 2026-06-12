# WasteDatasets Dataset Catalogue
A curated catalogue of waste-related openly available image datasets, organized for browsing, filtering, and downloading detection, segmentation, and classification data.

Website - https://wastedatasets.com/

## Dataset Summary

| Dataset | Slug | Task | Annotation fields | Samples | Classes | Source |
| --- | --- | --- | --- | ---: | --- | --- |
| COCO | `coco` | Object detection, instance segmentation | `detections`, `segmentations` | 22,958 | `cell phone`, `clock`, `hair drier`, `keyboard`, `laptop`, `microwave`, `mouse`, `oven`, `refrigerator`, `remote`, `toaster`, `toothbrush`, `tv` | [COCO Dataset](https://cocodataset.org/#home) |
| TACO | `taco` | Object detection, instance segmentation | `detections`, `segmentations` | 1,500 | `Aluminium foil`, `Battery`, `Aluminium blister pack`, `Carded blister pack`, `Other plastic bottle`, `Clear plastic bottle`, `Glass bottle`, `Plastic bottle cap`, `Metal bottle cap`, `Broken glass`, `Food Can`, `Aerosol`, `Drink can`, `Toilet tube`, `Other carton`, `Egg carton`, `Drink carton`, `Corrugated carton`, `Meal carton`, `Pizza box`, `Paper cup`, `Disposable plastic cup`, `Foam cup`, `Glass cup`, `Other plastic cup`, `Food waste`, `Glass jar`, `Plastic lid`, `Metal lid`, `Other plastic`, `Magazine paper`, `Tissues`, `Wrapping paper`, `Normal paper`, `Paper bag`, `Plastified paper bag`, `Plastic film`, `Six pack rings`, `Garbage bag`, `Other plastic wrapper`, `Single-use carrier bag`, `Polypropylene bag`, `Crisp packet`, `Spread tub`, `Tupperware`, `Disposable food container`, `Foam food container`, `Other plastic container`, `Plastic glooves`, `Plastic utensils`, `Pop tab`, `Rope & strings`, `Scrap metal`, `Shoe`, `Squeezable tube`, `Plastic straw`, `Paper straw`, `Styrofoam piece`, `Unlabeled litter`, `Cigarette` | [TACO](https://zenodo.org/records/3587843) |
| TrashNet | `trashnet` | Image classification | `classification` | 2,527 | `cardboard`, `glass`, `metal`, `paper`, `plastic`, `trash` | [TrashNet](https://github.com/garythung/trashnet) |

## Website Label Groups

The website shows these simpler group names in the left label panel. Selecting a group selects all listed source classes by default; the individual source classes are then shown below the search box and can be deselected before viewing or downloading. Source class names are written with their dataset prefix so it is clear where each label comes from.

| Website group | Source dataset classes |
| --- | --- |
| `plastic bottle` | TACO: `Clear plastic bottle`, `Other plastic bottle` |
| `plastic cap/lid` | TACO: `Plastic bottle cap`, `Plastic lid` |
| `metal cap/lid` | TACO: `Metal bottle cap`, `Metal lid`, `Pop tab` |
| `metal` | TACO: `Aluminium foil`, `Food Can`, `Aerosol`, `Drink can`, `Scrap metal`; TrashNet: `metal` |
| `blister pack` | TACO: `Aluminium blister pack`, `Carded blister pack` |
| `glass` | TACO: `Glass bottle`, `Glass cup`, `Glass jar`, `Broken glass`; TrashNet: `glass` |
| `paper` | TACO: `Normal paper`, `Magazine paper`, `Wrapping paper`, `Tissues`, `Paper bag`, `Paper straw`; TrashNet: `paper` |
| `cardboard/carton` | TACO: `Other carton`, `Egg carton`, `Drink carton`, `Corrugated carton`, `Meal carton`, `Pizza box`, `Toilet tube`; TrashNet: `cardboard` |
| `cup` | TACO: `Paper cup`, `Disposable plastic cup`, `Foam cup`, `Glass cup`, `Other plastic cup` |
| `plastic bag/wrapper` | TACO: `Plastic film`, `Six pack rings`, `Garbage bag`, `Other plastic wrapper`, `Single-use carrier bag`, `Polypropylene bag`, `Crisp packet`, `Plastified paper bag` |
| `food container` | TACO: `Spread tub`, `Tupperware`, `Disposable food container`, `Foam food container`, `Other plastic container` |
| `small plastic item` | TACO: `Other plastic`, `Plastic glooves`, `Plastic utensils`, `Squeezable tube`, `Plastic straw`, `Styrofoam piece`; TrashNet: `plastic` |
| `organic/food waste` | TACO: `Food waste` |
| `e-waste` | COCO: `tv`, `laptop`, `mouse`, `remote`, `keyboard`, `cell phone`, `microwave`, `oven`, `toaster`, `refrigerator`, `clock`, `hair drier`, `toothbrush` |
| `other` | TACO: `Battery`, `Rope & strings`, `Shoe`, `Cigarette`, `Unlabeled litter`; TrashNet: `trash` |

## Class Coverage

| Class | Dataset | Task |
| --- | --- | --- |
| `Aerosol` | TACO | Detection, segmentation |
| `Aluminium blister pack` | TACO | Detection, segmentation |
| `Aluminium foil` | TACO | Detection, segmentation |
| `Battery` | TACO | Detection, segmentation |
| `Broken glass` | TACO | Detection, segmentation |
| `cardboard` | TrashNet | Classification |
| `Carded blister pack` | TACO | Detection, segmentation |
| `cell phone` | COCO | Detection, segmentation |
| `Cigarette` | TACO | Detection, segmentation |
| `Clear plastic bottle` | TACO | Detection, segmentation |
| `clock` | COCO | Detection, segmentation |
| `Corrugated carton` | TACO | Detection, segmentation |
| `Crisp packet` | TACO | Detection, segmentation |
| `Disposable food container` | TACO | Detection, segmentation |
| `Disposable plastic cup` | TACO | Detection, segmentation |
| `Drink can` | TACO | Detection, segmentation |
| `Drink carton` | TACO | Detection, segmentation |
| `Egg carton` | TACO | Detection, segmentation |
| `Foam cup` | TACO | Detection, segmentation |
| `Foam food container` | TACO | Detection, segmentation |
| `Food Can` | TACO | Detection, segmentation |
| `Food waste` | TACO | Detection, segmentation |
| `Garbage bag` | TACO | Detection, segmentation |
| `glass` | TrashNet | Classification |
| `Glass bottle` | TACO | Detection, segmentation |
| `Glass cup` | TACO | Detection, segmentation |
| `Glass jar` | TACO | Detection, segmentation |
| `hair drier` | COCO | Detection, segmentation |
| `keyboard` | COCO | Detection, segmentation |
| `laptop` | COCO | Detection, segmentation |
| `Magazine paper` | TACO | Detection, segmentation |
| `Meal carton` | TACO | Detection, segmentation |
| `metal` | TrashNet | Classification |
| `Metal bottle cap` | TACO | Detection, segmentation |
| `Metal lid` | TACO | Detection, segmentation |
| `microwave` | COCO | Detection, segmentation |
| `mouse` | COCO | Detection, segmentation |
| `Normal paper` | TACO | Detection, segmentation |
| `Other carton` | TACO | Detection, segmentation |
| `Other plastic` | TACO | Detection, segmentation |
| `Other plastic bottle` | TACO | Detection, segmentation |
| `Other plastic container` | TACO | Detection, segmentation |
| `Other plastic cup` | TACO | Detection, segmentation |
| `Other plastic wrapper` | TACO | Detection, segmentation |
| `oven` | COCO | Detection, segmentation |
| `paper` | TrashNet | Classification |
| `Paper bag` | TACO | Detection, segmentation |
| `Paper cup` | TACO | Detection, segmentation |
| `Paper straw` | TACO | Detection, segmentation |
| `Pizza box` | TACO | Detection, segmentation |
| `plastic` | TrashNet | Classification |
| `Plastic bottle cap` | TACO | Detection, segmentation |
| `Plastic film` | TACO | Detection, segmentation |
| `Plastic glooves` | TACO | Detection, segmentation |
| `Plastic lid` | TACO | Detection, segmentation |
| `Plastic straw` | TACO | Detection, segmentation |
| `Plastic utensils` | TACO | Detection, segmentation |
| `Plastified paper bag` | TACO | Detection, segmentation |
| `Polypropylene bag` | TACO | Detection, segmentation |
| `Pop tab` | TACO | Detection, segmentation |
| `refrigerator` | COCO | Detection, segmentation |
| `remote` | COCO | Detection, segmentation |
| `Rope & strings` | TACO | Detection, segmentation |
| `Scrap metal` | TACO | Detection, segmentation |
| `Shoe` | TACO | Detection, segmentation |
| `Single-use carrier bag` | TACO | Detection, segmentation |
| `Six pack rings` | TACO | Detection, segmentation |
| `Spread tub` | TACO | Detection, segmentation |
| `Squeezable tube` | TACO | Detection, segmentation |
| `Styrofoam piece` | TACO | Detection, segmentation |
| `Tissues` | TACO | Detection, segmentation |
| `toaster` | COCO | Detection, segmentation |
| `Toilet tube` | TACO | Detection, segmentation |
| `toothbrush` | COCO | Detection, segmentation |
| `trash` | TrashNet | Classification |
| `Tupperware` | TACO | Detection, segmentation |
| `tv` | COCO | Detection, segmentation |
| `Unlabeled litter` | TACO | Detection, segmentation |
| `Wrapping paper` | TACO | Detection, segmentation |

## Downloaded File Structure

Downloads from the WasteDatasets website are exported as ZIP files. A ZIP contains the selected images, or the current filtered view if no samples are selected. When labels are filtered on the website, the downloaded annotations are filtered to the same selected labels.

```text
download.zip
  coco/
    cell_phone/
      image_001.jpg
    tv/
      image_002.jpg
  taco/
    Plastic bottle cap/
      batch_1_000006.jpg
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

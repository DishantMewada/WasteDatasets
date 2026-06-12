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

## Catalogue Format

Each dataset is represented by a folder containing a `manifest.json` file. The folder name is used as the dataset slug in the website.

```text
datasets/
  coco/
    manifest.json
    data/
    labels.json
  trashnet/
    manifest.json
    data/
```

Example manifest:

```json
{
  "slug": "dataset_slug",
  "name": "Dataset Name",
  "type": "classification_dir",
  "dataset_dir": "data",
  "task": "image classification",
  "classes": ["class_a", "class_b"],
  "source_url": "https://example.com/dataset",
  "license": "check upstream dataset terms",
  "description": "Short dataset description."
}
```

## Notes
- Dataset ownership, citation requirements, and license terms remain with the original dataset publishers.

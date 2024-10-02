---
comments: true
description: Discover YOLO11, the latest advancement in state-of-the-art object detection, offering unmatched accuracy and efficiency for diverse computer vision tasks.
keywords: YOLO11, state-of-the-art object detection, YOLO series, Ultralytics, computer vision, AI, machine learning, deep learning
---

# Ultralytics YOLO11

## Overview

YOLO11 is the latest iteration in the [Ultralytics](https://www.ultralytics.com) YOLO series of real-time object detectors, redefining what's possible with cutting-edge [accuracy](https://www.ultralytics.com/glossary/accuracy), speed, and efficiency. Building upon the impressive advancements of previous YOLO versions, YOLO11 introduces significant improvements in architecture and training methods, making it a versatile choice for a wide range of [computer vision](https://www.ultralytics.com/glossary/computer-vision-cv) tasks.

![Ultralytics YOLO11 Comparison Plots](https://github.com/user-attachments/assets/a311a4ed-bbf2-43b5-8012-5f183a28a845)

<p align="center">
  <br>
  <iframe loading="lazy" width="720" height="405" src="https://www.youtube.com/embed/rfI5vOo3-_A?si=uLCEBVVXwAHiOYqq&amp;start=5500"
    title="YouTube video player" frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    allowfullscreen>
  </iframe>
  <br>
  <strong>Watch:</strong> Ultralytics YOLO11 Announcement at <a href="https://www.ultralytics.com/events/yolovision">YOLO Vision 2024</a>
</p>

## Key Features

- **Enhanced Feature Extraction:** YOLO11 employs an improved backbone and neck architecture, which enhances [feature extraction](https://www.ultralytics.com/glossary/feature-extraction) capabilities for more precise object detection and complex task performance.
- **Optimized for Efficiency and Speed:** YOLO11 introduces refined architectural designs and optimized training pipelines, delivering faster processing speeds and maintaining an optimal balance between accuracy and performance.
- **Greater Accuracy with Fewer Parameters:** With advancements in model design, YOLO11m achieves a higher [mean Average Precision](https://www.ultralytics.com/glossary/mean-average-precision-map) (mAP) on the COCO dataset while using 22% fewer parameters than YOLOv8m, making it computationally efficient without compromising accuracy.
- **Adaptability Across Environments:** YOLO11 can be seamlessly deployed across various environments, including edge devices, cloud platforms, and systems supporting NVIDIA GPUs, ensuring maximum flexibility.
- **Broad Range of Supported Tasks:** Whether it's object detection, instance segmentation, image classification, pose estimation, or oriented object detection (OBB), YOLO11 is designed to cater to a diverse set of computer vision challenges.

## Supported Tasks and Modes

YOLO11 builds upon the versatile model range introduced in YOLOv8, offering enhanced support across various computer vision tasks:

| Model       | Filenames                                                                                 | Task                                         | Inference | Validation | Training | Export |
| ----------- | ----------------------------------------------------------------------------------------- | -------------------------------------------- | --------- | ---------- | -------- | ------ |
| YOLO11      | `yolo11n.pt` `yolo11s.pt` `yolo11m.pt` `yolo11l.pt` `yolo11x.pt`                          | [Detection](../tasks/detect.md)              | ✅        | ✅         | ✅       | ✅     |
| YOLO11-seg  | `yolo11n-seg.pt` `yolo11s-seg.pt` `yolo11m-seg.pt` `yolo11l-seg.pt` `yolo11x-seg.pt`      | [Instance Segmentation](../tasks/segment.md) | ✅        | ✅         | ✅       | ✅     |
| YOLO11-pose | `yolo11n-pose.pt` `yolo11s-pose.pt` `yolo11m-pose.pt` `yolo11l-pose.pt` `yolo11x-pose.pt` | [Pose/Keypoints](../tasks/pose.md)           | ✅        | ✅         | ✅       | ✅     |
| YOLO11-obb  | `yolo11n-obb.pt` `yolo11s-obb.pt` `yolo11m-obb.pt` `yolo11l-obb.pt` `yolo11x-obb.pt`      | [Oriented Detection](../tasks/obb.md)        | ✅        | ✅         | ✅       | ✅     |
| YOLO11-cls  | `yolo11n-cls.pt` `yolo11s-cls.pt` `yolo11m-cls.pt` `yolo11l-cls.pt` `yolo11x-cls.pt`      | [Classification](../tasks/classify.md)       | ✅        | ✅         | ✅       | ✅     |

This table provides an overview of the YOLO11 model variants, showcasing their applicability in specific tasks and compatibility with operational modes such as Inference, Validation, Training, and Export. This flexibility makes YOLO11 suitable for a wide range of applications in computer vision, from real-time detection to complex segmentation tasks.

## Performance Metrics

!!! performance

    === "Detection (COCO)"

        See [Detection Docs](../tasks/detect.md) for usage examples with these models trained on [COCO](../datasets/detect/coco.md), which include 80 pre-trained classes.

{% filter indent(width=8, first=False, blank=True) %}
{% include "macros/yolo-det-perf.md" %}
{% endfilter %}

    === "Segmentation (COCO)"

        See [Segmentation Docs](../tasks/segment.md) for usage examples with these models trained on [COCO](../datasets/segment/coco.md), which include 80 pre-trained classes.

{% filter indent(width=8, first=False, blank=True) %}
{% include "macros/yolo-seg-perf.md" %}
{% endfilter %}

    === "Classification (ImageNet)"

        See [Classification Docs](../tasks/classify.md) for usage examples with these models trained on [ImageNet](../datasets/classify/imagenet.md), which include 1000 pre-trained classes.

{% filter indent(width=8, first=False, blank=True) %}
{% include "macros/yolo-cls-perf.md" %}
{% endfilter %}

    === "Pose (COCO)"

        See [Pose Estimation Docs](../tasks/pose.md) for usage examples with these models trained on [COCO](../datasets/pose/coco.md), which include 1 pre-trained class, 'person'.

{% filter indent(width=8, first=False, blank=True) %}
{% include "macros/yolo-pose-perf.md" %}
{% endfilter %}

    === "OBB (DOTAv1)"

        See [Oriented Detection Docs](../tasks/obb.md) for usage examples with these models trained on [DOTAv1](../datasets/obb/dota-v2.md#dota-v10), which include 15 pre-trained classes.

{% filter indent(width=8, first=False, blank=True) %}
{% include "macros/yolo-obb-perf.md" %}
{% endfilter %}

## Usage Examples

This section provides simple YOLO11 training and inference examples. For full documentation on these and other [modes](../modes/index.md), see the [Predict](../modes/predict.md), [Train](../modes/train.md), [Val](../modes/val.md), and [Export](../modes/export.md) docs pages.

Note that the example below is for YOLO11 [Detect](../tasks/detect.md) models for [object detection](https://www.ultralytics.com/glossary/object-detection). For additional supported tasks, see the [Segment](../tasks/segment.md), [Classify](../tasks/classify.md), [OBB](../tasks/obb.md), and [Pose](../tasks/pose.md) docs.

!!! example

    === "Python"

        [PyTorch](https://www.ultralytics.com/glossary/pytorch) pretrained `*.pt` models as well as configuration `*.yaml` files can be passed to the `YOLO()` class to create a model instance in Python:

        ```python
        from ultralytics import YOLO

        # Load a COCO-pretrained YOLO11n model
        model = YOLO("yolo11n.pt")

        # Train the model on the COCO8 example dataset for 100 epochs
        results = model.train(data="coco8.yaml", epochs=100, imgsz=640)

        # Run inference with the YOLO11n model on the 'bus.jpg' image
        results = model("path/to/bus.jpg")
        ```

    === "CLI"

        CLI commands are available to directly run the models:

        ```bash
        # Load a COCO-pretrained YOLO11n model and train it on the COCO8 example dataset for 100 epochs
        yolo train model=yolo11n.pt data=coco8.yaml epochs=100 imgsz=640

        # Load a COCO-pretrained YOLO11n model and run inference on the 'bus.jpg' image
        yolo predict model=yolo11n.pt source=path/to/bus.jpg
        ```

## Citations and Acknowledgements

If you use YOLO11 or any other software from this repository in your work, please cite it using the following format:

!!! quote ""

    === "BibTeX"

        ```bibtex
        @software{yolo11_ultralytics,
          author = {Glenn Jocher and Jing Qiu},
          title = {Ultralytics YOLO11},
          version = {11.0.0},
          year = {2024},
          url = {https://github.com/ultralytics/ultralytics},
          orcid = {0000-0001-5950-6979, 0000-0002-7603-6750, 0000-0003-3783-7069},
          license = {AGPL-3.0}
        }
        ```

Please note that the DOI is pending and will be added to the citation once it is available. YOLO11 models are provided under [AGPL-3.0](https://github.com/ultralytics/ultralytics/blob/main/LICENSE) and [Enterprise](https://www.ultralytics.com/license) licenses.

## FAQ

### What are the key improvements in Ultralytics YOLO11 compared to previous versions?

Ultralytics YOLO11 introduces several significant advancements over its predecessors. Key improvements include:

- **Enhanced Feature Extraction:** YOLO11 employs an improved backbone and neck architecture, enhancing [feature extraction](https://www.ultralytics.com/glossary/feature-extraction) capabilities for more precise object detection.
- **Optimized Efficiency and Speed:** Refined architectural designs and optimized training pipelines deliver faster processing speeds while maintaining a balance between accuracy and performance.
- **Greater Accuracy with Fewer Parameters:** YOLO11m achieves higher mean Average [Precision](https://www.ultralytics.com/glossary/precision) (mAP) on the COCO dataset with 22% fewer parameters than YOLOv8m, making it computationally efficient without compromising accuracy.
- **Adaptability Across Environments:** YOLO11 can be deployed across various environments, including edge devices, cloud platforms, and systems supporting NVIDIA GPUs.
- **Broad Range of Supported Tasks:** YOLO11 supports diverse computer vision tasks such as object detection, [instance segmentation](https://www.ultralytics.com/glossary/instance-segmentation), image classification, pose estimation, and oriented object detection (OBB).

### How do I train a YOLO11 model for object detection?

Training a YOLO11 model for object detection can be done using Python or CLI commands. Below are examples for both methods:

!!! Example

    === "Python"

        ```python
        from ultralytics import YOLO

        # Load a COCO-pretrained YOLO11n model
        model = YOLO("yolo11n.pt")

        # Train the model on the COCO8 example dataset for 100 epochs
        results = model.train(data="coco8.yaml", epochs=100, imgsz=640)
        ```

    === "CLI"

        ```bash
        # Load a COCO-pretrained YOLO11n model and train it on the COCO8 example dataset for 100 epochs
        yolo train model=yolo11n.pt data=coco8.yaml epochs=100 imgsz=640
        ```

For more detailed instructions, refer to the [Train](../modes/train.md) documentation.

### What tasks can YOLO11 models perform?

YOLO11 models are versatile and support a wide range of computer vision tasks, including:

- **Object Detection:** Identifying and locating objects within an image.
- **Instance Segmentation:** Detecting objects and delineating their boundaries.
- **[Image Classification](https://www.ultralytics.com/glossary/image-classification):** Categorizing images into predefined classes.
- **Pose Estimation:** Detecting and tracking keypoints on human bodies.
- **Oriented Object Detection (OBB):** Detecting objects with rotation for higher precision.

For more information on each task, see the [Detection](../tasks/detect.md), [Instance Segmentation](../tasks/segment.md), [Classification](../tasks/classify.md), [Pose Estimation](../tasks/pose.md), and [Oriented Detection](../tasks/obb.md) documentation.

### How does YOLO11 achieve greater accuracy with fewer parameters?

YOLO11 achieves greater accuracy with fewer parameters through advancements in model design and optimization techniques. The improved architecture allows for efficient feature extraction and processing, resulting in higher mean Average Precision (mAP) on datasets like COCO while using 22% fewer parameters than YOLOv8m. This makes YOLO11 computationally efficient without compromising on accuracy, making it suitable for deployment on resource-constrained devices.

### Can YOLO11 be deployed on edge devices?

Yes, YOLO11 is designed for adaptability across various environments, including edge devices. Its optimized architecture and efficient processing capabilities make it suitable for deployment on edge devices, cloud platforms, and systems supporting NVIDIA GPUs. This flexibility ensures that YOLO11 can be used in diverse applications, from real-time detection on mobile devices to complex segmentation tasks in cloud environments. For more details on deployment options, refer to the [Export](../modes/export.md) documentation.
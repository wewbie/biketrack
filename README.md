Bike Rider Detection and Tracking Using YOLO
=========================================

A computer vision project focused on bike rider detection, tracking, counting, and traffic-flow visualisation at congested intersections.


--------

This project explores the application of YOLO-based object detection and multi-object tracking to bicycle-dominated traffic analysis. The model tracks bike **riders** instead of bikes themselves, in order to avoid unnecessary detection of parked bikes.

The project includes:

* Rider detection

* Individual rider tracking

* Rider counting

* Rider traffic heatmap generation

Models
------

| Model            | Description                         |
| ---------------- | ----------------------------------- |
| `ridertrack.pt`  | Trained rider detection model       |
| `ridertrack2.pt` | Alternative rider detection model   |
| `biketrack.pt`   | Low resoultion bike detection model |

**Class mapping:** 0 = bicycle
Installation

------------

    git clone https://github.com/wewbie/biketrack-yolo.gitcd biketrack-yolo
    pip install -r requirements.txt

Usage
-----

Run bicycle detection:
    python scripts/detect.py

Run bicycle tracking:
    python scripts/track.py

Generate a bicycle traffic heatmap:
    python scripts/heatmap.py
Requirements

------------

* Python

* PyTorch

* Ultralytics YOLO

* OpenCV

* NVIDIA GPU (recommended)

-----------------

## Performance

| Model            | mAP_50 | mAP_50-95 | Precision | Recall |
| ---------------- | ------ | --------- | --------- | ------ |
| `ridertrack.pt`  | 87.6%  | 54.9%     | 77.8%     | 82.1%  |
| `ridertrack2.pt` | 93.0%  | 62.2%     | 86.3%     | 88.8%  |
| `biketrack.pt`   | 83.6%  | 37.9%     | 89.9%     | 70.7%  |

License
-------

This project is distributed under the GNU Affero General Public License v3.0 (AGPL-3.0), subject to the applicable licensing requirements of Ultralytics YOLO.

Third-party dependencies, pretrained weights, datasets, and other external materials may have separate licensing terms. Please consult their respective licenses before redistribution or commercial use.

See [LICENSE](LICENSE) for the full license text.

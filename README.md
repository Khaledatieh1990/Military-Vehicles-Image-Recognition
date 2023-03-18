# Military Vehicles Image Recognition

Fine-Tuning YOLOv5 to detect Military Vehicles in Aerial ARMA 3 Imagery

<p align="center">
  <img src="media/crossroad.png" alt="Crossroad" width="70%"/>
</p>

Currently, the model is able to detect the following classes:
- CSAT Marid
- CSAT Zamak (Transport)

The model is a YOLOv5 fine tuned using 100 images of each class using various environments and angles at noon clear sky using a UAV at around 100 meters altitude.

The dataset used is available on [Kaggle](https://www.kaggle.com/datasets/alexandresajus/arma3cvdataset).

## How to use

1. Clone the repository

```bash
git clone https://github.com/AlexandreSajus/Military-Vehicles-Image-Recognition.git
```

2. Install the requirements

```bash
pip install -r requirements.txt
```

3. Add your images to the `input` folder

4. Run the model

```bash	
python detect.py --source ./input/ --weights runs/train/yolo_road_det10/weights/best.pt --conf 0.25 --name yolo_road_det
```

5. The results will be available in the `runs/detect/yolo_road_det` folder
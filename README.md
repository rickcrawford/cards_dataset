Cards Image Dataset
------------

This is a card detection dataset built for Bicycle Jumbo playing cards for Darknet YOLOv3. This is heavily based off of the work done in [geaxgx/playing-card-detection](https://github.com/geaxgx/playing-card-detection) to generate the training set. I have based the notebook in this project based on the work done in the notebook avaiable in the project above.

This dataset includes cards that are labeled from `[2-A]` for the 4 suits `[c,d,h,s]`, plus 2 jokers `JK`

Based this dataset off of the [Racoons Dataset](https://github.com/datitran/raccoon_dataset)

The `create_validation_set.sh` file is from [experiencor/keras-yolo3](https://github.com/experiencor/keras-yolo3)

Create a Virtual Python environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

Run the notebook:

```bash
jupyter notebook
```


To build the dataset using YOLO v3 Darknet, first download the darknet53.conv.74 file, and then kick off the training based on the instructions from the yolo website.

```bash
darknet detector train data/obj.data cfg/yolov3.cfg darknet53.conv.74 -map
```

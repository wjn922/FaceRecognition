# Face Recognition

face recognition using python and mysql

*******

## Useage

### Environment

```
conda create -n face python=3.x

conda activate face

pip install -r requirements.txt
```

### MySQL Install

[Mac](https://dev.mysql.com/doc/mysql-osx-excerpt/5.7/en/osx-installation-pkg.html)

[Ubuntu](https://dev.mysql.com/doc/mysql-linuxunix-excerpt/5.7/en/linux-installation.html)

[Windows](https://dev.mysql.com/downloads/installer/)

You'll obtain an account and password after installation, then you should modify the `faces.py`, with the corresponding
`user` and `passwd`:
```
# create database connection
myconn = mysql.connector.connect(host="localhost", user="root", passwd="xxxxx", database="facerecognition")
```

*******

## Run

### 1. Face Recognition

#### 1.1 Collect Face Data
```
"""
user_name = "Jack"   # the name
NUM_IMGS = 400        # the number of saved images
"""
python face_capture.py
```
The camera will be activated and the captured images will be stored in `data/Jack` folder.
**Note:** Only one person’s images can be captured at a time.

#### 1.2 Train a Face Recognition Model
```
python train.py
```
`train.yml` and `labels.pickle` will be created at the current folder.


### Import `facerecognition.sql`

The `facerecognition.sql` only has one example, "RYAN" now. It can be directly used without any modification by:

```
# login the mysql command
mysql -u root -p

# create database.  'mysql>' indicates we are now in the mysql command line
mysql> CREATE DATABASE facerecognition;
mysql> USE facerecognition;

# import from sql file
source facerecognition.sql
```
## Collect Face Data
```
"""
user_name = "Jack"   # the name
NUM_IMGS = 400        # the number of saved images
"""
python face_capture.py
```

## run train.py
```
python train.py
```

## run faces.py
```
python faces.py
```

The webcam will be active.

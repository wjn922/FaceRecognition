# Face Recognition

face recognition using python and mysql

## Useage

### Packages

```
conda create -n face python=3.x

conda activate face

pip install -r requirements.txt
```

### MySQL Install

[Mac](https://dev.mysql.com/doc/mysql-osx-excerpt/5.7/en/osx-installation-pkg.html)

[Ubuntu]()

[Windows]()

You'll obtain an account and password after installation, then you should modify the `faces.py`, with the corresponding
`user` and `passwd`:
```
# create database connection
myconn = mysql.connector.connect(host="localhost", user="root", passwd="xxxxx", database="facerecognition")
```

### Import `facerecognition.sql`

The `facerecognition.sql` only has one example, "RYAN" now. It can be directly used without any modification by:

```
# login the mysql command
mysql -u root -p

# create database.  'mysql>' indicates we are now in the mysql command line
mysql> create DATABASE facerecognition;
mysql> use facerecognition;

# import from sql file
source facerecognition.sql
```
## Collect Face Data
```
"""
user_name = "Jack" # the name
NUM_IMGS = 10  # the number of saved images
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
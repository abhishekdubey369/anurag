# Python Fingerprint Recognition

Fingerprint recognition with SKimage and OpenCV

Requirements:
- NumPy
- SKimage
- OpenCV2


Works by extracting minutiae points using harris corner detection.

Uses SIFT (ORB) go get formal descriptors around the keypoints with brute-force hamming distance and then analyzes the returned matches using thresholds.

Usage:

1. Place 2 fingerprint images that you want to compare inside the database folder
2. Pass the names of the images as arguments in the console

## project explanation

enhance folder contain all the filters required for fingerprint comparision
and code for graph plotting where as app.py contain three functions.

## Run without Docker

```shell
pip install -r requirements.txt

python app.py 101_1.tif 102_2.tif
```

101_1.tif and 102_2.tif can be interchange and can be changed from database even new images can be add and use there name

## Dockerfile

If you don't want to install the libraries, or want a easier way to test the application you can follow the commands:

if using docker then in app.py first uncomment os.chdir("/app/")

```shell
docker build -t <name_of_your_choice> .

docker run -it <name_of_your_choice> <fingerprint_1> <fingerprint_2>
```

If you don't have Docker Engine installed, you can get the instructions to install it here: [Install Docker](https://docs.docker.com/v17.09/engine/installation/)

NOTE: the fingerprints must be in the `/database` folder

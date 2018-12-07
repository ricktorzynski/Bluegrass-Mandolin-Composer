# Bluegrass Mandolin Picker

This is a clone of Classic-Piano-Composer, https://github.com/Skuldur/Classical-Piano-Composer and instead of piano music, I used bluegrass mandolin songs from Mandolin Cafe TablEdit Library (converted to midi), https://www.mandolincafe.com/cgi-bin/tabledit/search?name=Bluegrass for training.

I converted the TablEdit files of the songs into midi files.  I trained the model on a Linux computer running Ubuntu 18.04 with 32GB RAM and a GeForce GTX 1070 Ti graphics card.  Took approximately 10 hours to train the model and 30secs to generated 2 minutes of random music.




This project allows you to train a neural network to generate midi music files that make use of a single instrument

## Requirements

* Python 3.x
* Installing the following packages using pip:
	* Music21
	* Keras
	* Tensorflow
	* h5py

## Training

To train the network you run **lstm.py**.

E.g.

```
python lstm.py
```

The network will use every midi file in ./midi_songs to train the network. The midi files should only contain a single instrument to get the most out of the training.

**NOTE**: You can stop the process at any point in time and the weights from the latest completed epoch will be available for text generation purposes.

## Generating music

Once you have trained the network you can generate text using **predict.py**

E.g.

```
python predict.py
```

You can run the prediction file right away using the **weights.hdf5** file

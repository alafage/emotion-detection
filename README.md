# emotion-detection

## Dependencies

This project requires [PyTorch](https://pytorch.org/) and [OpenCV](https://docs.opencv.org/3.4/da/df6/tutorial_py_table_of_contents_setup.html).

## Structure

* doc: documentation
* rel: results released in pdf file.
* src:
  * lib: definitions of custom Python classes
  * models: neural network back-ups

## Change the neural network architecture

You can change the neural network architecture by modifying the `Net` class in `network.py`.

## Train a neural network

To train and save a new neural network with the balanced dataset you can use the following script:

```sh
python3.7 src/training.py
```

All the networks saved will be in `src/models` folder.

## Run the live application

You have to change the path used in `face_detection.py` to prevent errors.
You can change the neural network loaded and used in the application by changing the path at the 19th line in `main.py`:

```py
CNN_PATH = './models/network_v2.pth'
```

Commands to run the live application:

```sh
python src/main.py
```

You can see the prediction results on the terminal.

# CSN-Group-Project
Computer System and Networks Group Project

### References
https://github.com/tensorlayer/srgan

### Training
This repo does NOT ionlcude all the neccesarry data and file to train the netork.
Images and model files would take up way to much space and training would take ages anyways.

In case you want to go through all the effort you will also need the vgg19 pretrained model
Download the [VGG19 model](https://drive.google.com/file/d/1pZ0v-sLj-glfSx3Cssk_aBFRI8mF0hiq/view?usp=sharing) and place it in the folder `models/`

### Evaluating
The notebook.ipynb shows the evaluation of a input image

### Notes
Depending on the installed versions of the dependecies, executing the evaluation or the training locally can be difficult.

If errors occur in the files mentioned below, then make the following modifications:

Modify multiple lines of `python-installation/site-packages/tensorlayer/files/util.py`

`layer_names = [n.decode('utf8') for n in f.attrs["layer_names"]]` or similar
to `layer_names = f.attrs["layer_names"]`

Modify multiple lines of `python-installation/site-packages/tensorlayer/models/core.py`

`if isinstance(check_argu, tf_ops._TensorLike) or tf_ops.is_dense_tensor_like(check_argu):` 
to `if isinstance(check_argu, (tf.Tensor, tf.SparseTensor, tf.Variable)) or tf_ops.is_dense_tensor_like(check_argu):`

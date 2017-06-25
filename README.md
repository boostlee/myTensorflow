# myTensorflow
details  https://www.tensorflow.org/install/install_sources
To clone the latest TensorFlow repository, issue the following command:
$ git clone https://github.com/tensorflow/tensorflow 
$ cd tensorflow
$ git checkout Branch # where Branch is the desired branch
$ git checkout r1.2

cd tensorflow
./configure

To build a pip package for TensorFlow with CPU-only support, invoke the following command:
$ bazel build --config=opt //tensorflow/tools/pip_package:build_pip_package

To build a pip package for TensorFlow with GPU support, invoke the following command:
$ bazel build --config=opt --config=cuda //tensorflow/tools/pip_package:build_pip_package

The bazel build command builds a script named build_pip_package. Running this script as follows will build a .whl file within the /tmp/tensorflow_pkg directory:

$ bazel-bin/tensorflow/tools/pip_package/build_pip_package /tmp/tensorflow_pkg
$ sudo pip install /tmp/tensorflow_pkg/tensorflow-1.2.0-py2-none-any.whl

validation installation
cd to other dir, and then
$python
$import tensorflow as tf
$hello = tf.constant('Hello, TensorFlow!')
$sess = tf.Session()
$print(sess.run(hello))

If the system outputs the following, then you are ready to begin writing TensorFlow programs:
Hello, TensorFlow!

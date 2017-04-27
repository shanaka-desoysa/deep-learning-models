# Install
conda create -n keras python=3.5
activate keras
conda install theano
conda install mingw libpython
pip install tensorflow
pip install keras
pip install scikit-learn
pip install pillow
pip install h5py
pip install tensorflow-gpu
pip install imagenet_utils
## Open CV
conda install -c menpo opencv3

# Verify
python -c "from keras import backend; print(backend._BACKEND)"

# Config
python -c "import os; print(os.path.expanduser('~') + '\.keras\\keras.json')"

# Verify GPU
python -c "import tensorflow as tf; sess = tf.Session(); hello = tf.constant('Hello, TensorFlow!'); print(sess.run('hello'))"

# Run
activate keras
python test_imagenet.py --image images/kodiak-bear.png

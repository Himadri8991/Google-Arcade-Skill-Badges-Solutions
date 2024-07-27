# TensorFlow: Qwik Start || [GSP637](https://www.cloudskillsboost.google/course_templates/646/labs/476323) ||

## *Copy the IDE URL from the lab panel.

## **Paste it into a new browser window.

### Navigation Menu > Terminal > New Terminal

### Run the following Commands in Terminal

```

pip install google-cloud-logging
pip install ---upgrade protobuf
pip install --upgrade tensorflow

python --version
python -c "import tensorflow;print(tensorflow.__version__)"

import logging
import google.cloud.logging as cloud_logging
from google.cloud.logging.handlers import CloudLoggingHandler
from google.cloud.logging_v2.handlers import setup_logging

cloud_logger = logging.getLogger('cloudLogger')
cloud_logger.setLevel(logging.INFO)
cloud_logger.addHandler(CloudLoggingHandler(cloud_logging.Client()))
cloud_logger.addHandler(logging.StreamHandler())

import tensorflow as tf
import numpy as np

xs = np.array([-1.0, 0.0, 1.0, 2.0, 3.0, 4.0], dtype=float)
ys = np.array([-2.0, 1.0, 4.0, 7.0, 10.0, 13.0], dtype=float)

model = tf.keras.Sequential([tf.keras.layers.Dense(units=1, input_shape=[1])])

model.compile(optimizer=tf.keras.optimizers.SGD(), loss=tf.keras.losses.MeanSquaredError())

model.fit(xs, ys, epochs=500)

cloud_logger.info(str(model.predict(np.array([10.0]))))

python model.py

```

### Congratulations 🎉 for completing the Challenge Lab !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

#### Don't Forget to Join the [WhatsApp Group](https://chat.whatsapp.com/CcX9gXycV1lKmOjnZQCk7g) 

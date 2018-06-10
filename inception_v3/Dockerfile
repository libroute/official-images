FROM tensorflow/tensorflow
COPY classify_image.py.patch /notebooks/
RUN mkdir /tmp/imagenet \
    && curl -o /tmp/imagenet/inception-2015-12-05.tgz http://download.tensorflow.org/models/image/imagenet/inception-2015-12-05.tgz \
    && cd /tmp/imagenet/ ; tar xf inception-2015-12-05.tgz \
    && rm /tmp/imagenet/inception-2015-12-05.tgz \
    && curl -o /notebooks/classify_image.py https://raw.githubusercontent.com/tensorflow/models/86ecc9730d751c1f72e3bfecac958166390f4125/tutorials/image/imagenet/classify_image.py \
    && patch -i /notebooks/classify_image.py.patch /notebooks/classify_image.py
CMD python classify_image.py

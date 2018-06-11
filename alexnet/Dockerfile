FROM tensorflow/tensorflow
RUN curl -o /notebooks/bvlc_alexnet.npy http://www.cs.toronto.edu/%7Eguerzhoy/tf_alexnet/bvlc_alexnet.npy 
COPY myalexnet_forward_newtf.py.patch /notebooks/myalexnet_forward_newtf.py.patch
RUN cd /notebooks \
    && curl -o myalexnet_forward_newtf.py http://www.cs.toronto.edu/%7Eguerzhoy/tf_alexnet/myalexnet_forward_newtf.py \ 
    && echo "9436aa6dfcedef664306f46a15b9c095f70ff4bd536c84d9b2b0a395e1872cb8  myalexnet_forward_newtf.py" | sha256sum -c \
    && curl -o caffe_classes.py http://www.cs.toronto.edu/%7Eguerzhoy/tf_alexnet/caffe_classes.py \
    && patch -i myalexnet_forward_newtf.py.patch myalexnet_forward_newtf.py
CMD python myalexnet_forward_newtf.py

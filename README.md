1. First up install Python  3.7.4. Download and install the package for your OS that has the words 2019.07 in it from here https://repo.anaconda.com/archive/. 
This should give you 3.7.4 to work with. 

2. Then install Visual Studio C++ 2015 from here: https://go.microsoft.com/fwlink/?LinkId=691126. Tensorflow needs this in order to compile 

3. OPTIONAL IF YOU HAVE A GPU - Install Cuda and Cudnn. Install Cuda first, then install Cudnn. 
- Cuda: 10.1 - https://developer.nvidia.com/cuda-10.1-download-archive-base
- Cudnn: 7.6.5 - https://developer.nvidia.com/rdp/cudnn-download

Once Cudnn is installed you need to copy the Cudnn files into their respective folders inside the Cuda directory. I used this as a guide: https://towardsdatascience.com/installing-tensorflow-with-cuda-cudnn-and-gpu-support-on-windows-10-60693e46e781 
 
4. Then install Protoc 3.13 from here: https://github.com/protocolbuffers/protobuf/releases. For windows, download the repository and then add it to your PATH file. 

5. Then install python packages using the pip command: 
  Tensorflow: 2.3.1 - pip install tensorflow==2.3.1
  OpenCV: 4.4.0  - pip install tensorflow==4.4.0

6. Install the object detection API. To do this, run these commands from a command prompt or terminal:
  git clone https://github.com/tensorflow/models 
  cd tensorflow/models/research 
  protoc object_detection/protos/*.proto --python_out=.
  cp object_detection/packages/tf2/setup.py .
  python -m pip install .


Note : use PyYamil == 5.3.1 temporary
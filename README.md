# Human-Behaviour-analysis-using-OpenCV
Detect human time spend infront of camera. Predict his/her emotion based on facial expression,  eye movement, hand gesture infront of camera. Show the behavioural result in graphical format.




Error Resolve
-------------

1. CUDA Error

UnknownError:  Failed to get convolution algorithm. This is probably because cuDNN failed to initialize, so try looking to see if a warning log message was printed above.
	 [[node conv2d_1_1/convolution (defined at C:\Users\Ajay\Anaconda3\lib\site-packages\keras\backend\tensorflow_backend.py:3009) ]] [Op:__inference_keras_scratch_graph_749]

Function call stack:
keras_scratch_graph:

Solution: - 
----------
import tensorflow as tf
config = tf.compat.v1.ConfigProto()
config.gpu_options.allow_growth = True
sess = tf.compat.v1.Session(config=config)

--------------------------------------------------------------------------------------------------------------
2. OpneCL error
OpenCL error CL_MEM_OBJECT_ALLOCATION_FAILURE (-4)

solution : - Disable OpenCL
-----------
cv2.ocl.setUseOpenCL(False)
#export OPENCV_OPENCL_DEVICE=disabled

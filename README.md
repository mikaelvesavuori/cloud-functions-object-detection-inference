# TensorFlow 1.15-based object detection in Google Cloud Functions

This sample function is a fairly minimal implementation of how you can do object detection inference in a Google Cloud Function. It will not assist in any of the training steps, for which I recommend Colaboratory or some other dedicated environment.

**Note**:

- This notebook should be able to "emulate" the experience of the function, but you will likely need to do a bit of copy-paste back-and-forth to ensure your real Cloud Function works as intended, as you make any changes of your own.
- There are very small differences between using this in Colab and in a real function. For example: In Colab you'll need to run the first two cells to prep the environments. Those two cells should not be part of your Cloud Function source code!
- This implementation is not optimized for container reuse and performance
- Images will be loaded from source as a file, NOT as Base64 (in which case you probably need to modify the below code, as well as use a model that takes in encoded_image_string_tensor)

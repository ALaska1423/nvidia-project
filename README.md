# Traffic Cone Detection

To help drivers with awareness of the road. By using machine learning to identify when traffic cones are present on the road, safety for drivers can be improved.

![](https://user-images.githubusercontent.com/95560015/175785847-53bd1812-1fe9-47db-a4d1-d44d1699cdf3.png)


In the test image, the algorithm detects the presence of a traffic cone.


## The Algorithm

Using samples of traffic cones and empty roads, this network has been trained to detect cones using resnet18. 

## Running this project

1. Install the [jetson inference project]([url](https://github.com/dusty-nv/jetson-inference)) to your home directory

2. Install this project into the home directory.

3. Change directory to this project 

   cd nvidia-project

4. Set the DATASET and NET variables

   NET=models/cone_road

   DATASET=data/cone_road

5. To process image of choice, place the image into 'data/cone_road/test/cone'
6. Run the imagenet.py using a image of choice. The command should be written as below, replacing the directory with image of choice.
 
   imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/cone/("name of file")  ("name of output file".png)


[View a video explanation here](https://youtu.be/a6ecYL6QiJs)

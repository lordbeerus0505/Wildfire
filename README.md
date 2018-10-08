# Idea for codefundo++ - Wildfire(change the name of app here)
A wildfire detection and prediction application with facilities to contact for assistance

## Product description
The application being developed is for the detection of wildfires using live video feed. Video processing is a much faster way of fire detection than more simplistic approaches such as temperature changes as they can provide close to real time detection. This application would require hardware to record video feed from the forest and transmit it to the system. This portion is not implemented as a part of the application and hence, supply of video feed is to be taken care of by the user. Once the system detects a fire at that location, a signal is sent out to the nearest specified emergency station (by an automated phone call) stating the coordinates of fire which would allow the station to respond in real time so as to supress the fire as soon as possible.

## Working specification
The approach of fire detection in the forest involves the use of a supervised training model over a convolutional neural network using the YOLO algorithm. This allows for real time object detection with minimal computation as YOLO runs a sliding window through the image only once. To train the model, datasets having images or fire are used which help detect the shape and colour of fire amongst other features. Since YOLO looks at the entire image at one go and takes into consideration the global context, addition of greenary to the fire will help yolo detect a wildfire more effectively. For this sake the network will be fed with sample videos of forest fires as well.
  
While transmitting video feed, the GPS coordinates of the camera making the recording are also transmitted which allows the system to know the source location of the fire thereby being able to curtail it early on.
#### The steps followed would include:
* Train the model by providing it with feed on forest fires that are well annotated.
* Pass actual video feed to the model along with its GPS coordinates.
* The model, when it detects the presence of fire in the feed generates a signal.
* The application sends an automated response to the closest station providing the coordinates of the fire.
* The fire is then subdued.
  

## How to start off with the project
## Datasets being used
## Technologies used


### Problem Statement:
In this work, we propose and address a new computer vision task, which we call fashion item detection, where the aim is to detect various fashion items a person in the image is wearing or carrying. The types of fashion items we consider in this work include hat, glasses, bag, pants, shoes and so on. The detection of fashion items can be an important first step of various e-commerce applications for fashion industry. Our method is based on state-of-the-art object detection method pipeline which combines object proposal methods with a Deep Convolutional Neural Network.

#### Configuration
* We are using **SSD(single shot detector)** [TFOD API](https://github.com/tensorflow/models) to build this model.

#### Overview of dataset

* You can see a example of the labeled cell image.

  We have three kind of labels :

  * ear_ring
  * GirlsTopWear
  * glass
  * hat
  * Jacket
  * MensShorts
  * MensTopWear
  * Pant
  * shoes
  * tie
  * watch

![Output](https://github.com/rp926463-arch/Blood-Cell-Detection/blob/main/research/data/BLOOD_CELLS_output/image5.png?raw=true)

### Data preparation
Data preparation is important to use machine learning. In this project, the SSD algorithm for Object Detection is used.

* The structure`

  ```
  ├── clientApp.py
  ├── hat.jpg
  └── output4.jpg
  ```



* The `Annotations` : The VOC format `.xml` for Object Detection, automatically generate by the label tools. Below is an example of `.xml` file.

  ```xml
  <annotation>
  	<folder>JPEGImages</folder>
  	<filename>hat.jpg</filename>
  	<path>/home/pi/detection_dataset/JPEGImages/hat.jpg</path>
  	<source>
  		<database>Unknown</database>
  	</source>
  	<size>
  		<width>640</width>
  		<height>480</height>
  		<depth>3</depth>
  	</size>
  	<segmented>0</segmented>
  	<object>
  		<name>WBC</name>
  		<pose>Unspecified</pose>
  		<truncated>0</truncated>
  		<difficult>0</difficult>
  		<bndbox>
  			<xmin>260</xmin>
  			<ymin>177</ymin>
  			<xmax>491</xmax>
  			<ymax>376</ymax>
  		</bndbox>
  	</object>
      ...
  	<object>
  		...
  	</object>
  </annotation>
  ```



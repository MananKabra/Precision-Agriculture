## The Solution Flow Diagrams
The Sugarcane Field Detection and Yield Prediction project seeks to revolutionize sugarcane farming by employing cutting-edge technologies. Through the integration of image processing and machine learning, the system automates the identification of sugarcane fields using satellite or drone imagery and predicts crop yield based on historical and real-time data. This initiative not only facilitates precision agriculture practices by providing farmers with accurate information about their fields but also contributes to resource efficiency and increased yield. 
<br>
<img src="https://github.com/MananKabra/Precision-Agriculture/assets/89775656/2739c0f3-e060-49cb-915e-cf4192341395" width="800"/>
<br>
<img src="https://github.com/MananKabra/Precision-Agriculture/assets/89775656/67ee8aed-48e8-459f-9808-e45953256158" width="800"/>

## Detectron2 Framework (Model_Zoo)
Detectron2 is an open-source object detection and segmentation framework developed by Facebook AI Research. It is a built on top of PyTorch and provides a unified API for a variety of tasks, including object detection, instance segmentation, and panoptic segmentation. Designed to be flexible and easy-to-use, it puts a focus on enabling rapid research. It includes high-quality implementations of state-of-the-art algorithms like Mask R-CNN, RetinaNet, and DensePose. From the detectron2 framework, we are using the Model Zoo for object detection and instance segmentation. 
<br>

## Layered Architecture Diagram
<img src="https://github.com/MananKabra/Precision-Agriculture/assets/89775656/7095ef2b-4592-4b6c-887a-05aa7cfb30ed" width="800"/>


## Dataset Generation From Satellite Images
The dataset was generated from Google Earth. We Downloaded the images of agricultural fields both containing and not containing sugarcane fields from Google Earth Pro Desktop.
Then Performed Data Augmentation in order to diversify the satellite images. Data Augmentation involves applying various transformations to the existing images, such as rotation, flipping, scaling, and changes in brightness or contrast. 
Divide the final images dataset into 3 parts - Training, Testing and Validation.
Then Performed image augmentation using MakeSenseAI, by marking out the sugarcane fields from the images inside a polygon. The polygons are Labelled as Sugarcane Fields.
A config file a generated after the annotation is completed. The file is of json format containing details about the polygons that were marked, 
like - size, number, base64 data, shape attributes, all x coordinates and all y coordinates.
<br>

<img src="https://github.com/MananKabra/Precision-Agriculture/assets/89775656/b098af5d-a639-4c53-a738-7b52dcfcd8d7" width="800"/>


## Segmentation of Sugarcane Fields
The data set that was generated from Google Earth Pro Desktop helped us to detect sugarcane field of a particular area. The area that reflected sugarcane field was highlighted in different colors while the other field was converted to grayscale.
<br>

Test Run 1
<br>
<img src="https://github.com/MananKabra/Precision-Agriculture/assets/89775656/bcacdf6c-4622-4fb3-bb49-f8e561bed314" width="400"/>
<img src="https://github.com/MananKabra/Precision-Agriculture/assets/89775656/a96e8d88-a55d-4b81-9521-bf4a3c100c78" width="400"/>

Test Run 2
<br>
<img src="https://github.com/MananKabra/Precision-Agriculture/assets/89775656/d8ae164a-f7c8-4f0f-a3d9-737703a8f265" width="400"/>
<img src="https://github.com/MananKabra/Precision-Agriculture/assets/89775656/8629f081-8409-4973-ad99-bb362f3fdd99" width="400"/>

Test Run 3
<br>
<img src="https://github.com/MananKabra/Precision-Agriculture/assets/89775656/b024137e-140e-49d2-88ea-ad85f1749d5c" width="400"/>
<img src="https://github.com/MananKabra/Precision-Agriculture/assets/89775656/bd3c583b-e2bd-44ec-b96f-b31159e87a1b" width="400"/>

Test Run 4
<br>
<img src="https://github.com/MananKabra/Precision-Agriculture/assets/89775656/5b5aa6e7-92f8-4e99-9b37-41806992b391" width="400"/>
<img src="https://github.com/MananKabra/Precision-Agriculture/assets/89775656/5eaa2245-2c73-4c9b-ac76-5e39680762a5" width="400"/>

Test Run 5
<br>
<img src="https://github.com/MananKabra/Precision-Agriculture/assets/89775656/d0a41b39-2339-4fcd-8ea0-2f6eab6c48b3" width="400"/>
<img src="https://github.com/MananKabra/Precision-Agriculture/assets/89775656/244a62da-b0c9-4ff5-9463-ee80736796e8" width="400"/>


## Plotting Linear Regression btw Area and Production
Depending on the area of sugarcane field we calculated the yield per year. The dataset used was a historical data of different states. We have plotted a graph using linear regression which shows an accuracy of 95%. The graph was plotted on the basis of area of sugarcane field detected and production per year.
<br>
<img src="https://github.com/MananKabra/Precision-Agriculture/assets/89775656/23aac992-ea7f-46a2-808e-de18220e69fc" width="800"/>


# CE_DM
for  Paper Implementation
apt-get install tk-dev python-tk
pip install pandas
pip install pycocotools
pip install opencv-python
pip install requests

and download the coco dataset.The coco folder is set up as follows:
--coco
	--annotations
	--image_info_test2017
 	--images
		--train2017
		--val2017
	--test2017
Use the following statements for training:
python train.py --coco_path ../coco --depth 50
The optional parameters for depth are 18,34,50,101,152

If you want to use a pre-trained model use the following statement:
python visualize.py --coco_path ./coco --model ./coco_resnet_50.pt
Enter any key to view the next image, enter q to exit

The training results of the model coco_resnet_50 are as follows：
...
 Average Precision  (AP) @[ IoU=0.50:0.95 | area=   all | maxDets=100 ] = 0.335
 Average Precision  (AP) @[ IoU=0.50      | area=   all | maxDets=100 ] = 0.499
 Average Precision  (AP) @[ IoU=0.75      | area=   all | maxDets=100 ] = 0.357
 Average Precision  (AP) @[ IoU=0.50:0.95 | area= small | maxDets=100 ] = 0.167
 Average Precision  (AP) @[ IoU=0.50:0.95 | area=medium | maxDets=100 ] = 0.369
 Average Precision  (AP) @[ IoU=0.50:0.95 | area= large | maxDets=100 ] = 0.466
 Average Recall     (AR) @[ IoU=0.50:0.95 | area=   all | maxDets=  1 ] = 0.282
 Average Recall     (AR) @[ IoU=0.50:0.95 | area=   all | maxDets= 10 ] = 0.429
 Average Recall     (AR) @[ IoU=0.50:0.95 | area=   all | maxDets=100 ] = 0.458
 Average Recall     (AR) @[ IoU=0.50:0.95 | area= small | maxDets=100 ] = 0.255
 Average Recall     (AR) @[ IoU=0.50:0.95 | area=medium | maxDets=100 ] = 0.508
 Average Recall     (AR) @[ IoU=0.50:0.95 | area= large | maxDets=100 ] = 0.597
...

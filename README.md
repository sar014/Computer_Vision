# Computer Vision Tasks

For Yolo, Harris Corner Detection (video question),Video Analytics and Traffic Monitoring you need to download any open source video for testing purpose. 


### Traffic Monitoring
Developed a YOLO-based video analytics system capable of vehicle detection, tracking, speed estimation, congestion analysis, and stopped-vehicle identification from traffic footage.

### Video Analytics
Built a YOLO-powered retail video analytics solution for people counting, congestion detection, and queue estimation to analyze customer behavior and store traffic patterns.

### Xerox JBIG2 Error
Tasks implemnted include:
1. Extract connected components, measure shape similarity, group similar symbols, and replace with a prototype.
2. Adjust similarity threshold to observe when different characters start merging.
3. Generate multiple compressed versions, compute PSNR/SSIM, and analyze edge detection or OCR outputs.
4. Extract components/contours and quantify structural differences to detect distortions or substitutions.
5. Recognize characters using heuristics and measure accuracy on original vs compressed images.
6. Use image features like entropy, edge density, or component count to decide between lossless, lossy, or no compression.

### Harris Corner Detection
Optimize corner detection by using efficient filtering, tunable non-maximum suppression, adaptive thresholding, sub-pixel accuracy, multi-scale Harris detection, top-N score selection, and score-based FAST suppression.

### SIFT, SURF and ORB
Implemented SURF, ORB, and SIFT feature detectors and descriptors for matching keypoints between two images, using BFMatcher with Lowe’s ratio test for reliable correspondences, and visualized the results with drawMatches.


### LAB1 - CNN
Implemented a convolutional neural network (CNN) for image classification on the CIFAR-10 dataset, designing convolutional, pooling, and fully connected layers to learn feature representations and classify images into 10 categories, and trained the model using Python and Keras/TensorFlow.

The model architecture is a sequential network composed of two primary convolutional blocks—each featuring two Conv2D layers with batch normalization, followed by max-pooling and dropout—and a final classification head consisting of a dense layer with 512 units and a softmax output layer. Trained the model using the Adam optimizer and categorical cross-entropy loss over 30 epochs, achieving significant accuracy improvements on the training and validation sets as the network learned to identify patterns within the ten image classes.

**Dataset Used :** CIFAR-10

### LAB1 - Transfer Learning
Applied transfer learning using the ResNet50 architecture, leveraging pre-trained weights to extract features and fine-tuning the network for a custom image classification task, enabling faster convergence and improved accuracy on the target dataset.

### Lab2 - Yolo
Learned object detection fundamentals by combining classification and localization, applied a modern YOLO model for real-time detection, and understood the distinctions between classification, detection, and segmentation.

Initialized a pre-trained YOLOv8n (nano) model and configured it to perform inference specifically for "person" and "car" classes. The code utilizes OpenCV to capture and read video frames, resizing them for efficiency, and then processes each frame through the model to detect objects and draw bounding boxes.


### Lab2 - Semantic Segmentation 
Implemented and trained a U-Net architecture for semantic segmentation on the Carvana Image Masking Challenge dataset, enabling accurate pixel-level identification of vehicle regions.

Implemented a U-Net architecture in PyTorch, which is a specialized convolutional neural network designed for fast and precise semantic segmentation. After downloading and extracting the high-resolution training images and their corresponding masks, built a custom dataset and data loader to handle the mapping and preprocessing of these pairs. The model was trained using a combination of Binary Cross-Entropy (BCE) loss and monitored using the Dice Score to evaluate the overlap between predicted segmentations and the ground truth

**Dataset Used:** Carvana Image Masking Challenge dataset from Kaggle

### LAB3 - CNN Impact of Padding and Strides
Convolutional Neural Networks (CNNs) are deep learning models specifically designed to process data with a grid-like structure, such as images. Images can be viewed as 2D grids of pixel values, making CNNs highly effective for computer vision tasks.

**Stride** defines how many pixels the filter moves at each step.

Example:

- **Stride = 1** → Filter moves one pixel at a time  
- **Stride = 2** → Filter jumps two pixels  

**Padding** means adding extra pixels (usually zeros) around the image border.

Common types:

- **Valid Padding** → No padding  
- **Same Padding** → Pad so output size matches input size  

CNN performance and behavior are strongly influenced by stride and padding choices, making them critical design parameters.

**Dataset Used :** CIFAR-10


### LAB3 - RCNN
Traditional Convolutional Neural Networks (CNNs) that rely on fully connected layers often struggle with object detection tasks. This is especially true when an image contains multiple objects that vary in size and position.
Instead of exhaustively scanning the image, R-CNN uses a selective search algorithm to generate approximately 2,000 region proposals. These regions are likely to contain objects.

Each proposed region is then:

1. Warped into a fixed size  
2. Passed through a CNN for feature extraction  
3. Classified to determine the object category  
4. Refined using bounding box regression  

**Dataset Used :** Subset of COCO

### LAB4 - Cancer Detection using CNN
Built a Sequential Convolutional Neural Network (CNN) designed for image classification, incorporating layers such as Conv2D for feature extraction, MaxPooling2D for dimensionality reduction, and Dropout to mitigate overfitting. Also implemented the ImageDataGenerator for efficient image loading and data normalization, and employed EarlyStopping and ModelCheckpoint callbacks to optimize training by preventing unnecessary epochs and saving only the highest-performing version of the model.

**Dataset Used :** Breast Histopathology Images dataset from Kaggle

### LAB4 - Facial Recognition using FaceNet
Implemented a facial recognition system following a FaceNet-inspired architecture by building a custom convolutional neural network (CNN) in PyTorch to perform metric learning. Using the CelebA Face Recognition Triplets dataset from Kaggle, you processed images into an anchor-positive-negative structure and trained the model to map faces into a 512-dimensional Euclidean space where identity similarity is determined by distance. The architecture utilizes five convolutional blocks—each integrating batch normalization and ReLU activation—and is optimized through Triplet Margin Loss to ensure embeddings of the same person are clustered together while those of different individuals are pushed apart. Your implementation successfully achieves a triplet accuracy of 85.06% and includes functional components for 1:1 face verification and 1:N identity identification against a stored gallery of image embeddings.

**Dataset Used:** CelebA Face Recognition Triplets dataset from Kaggle

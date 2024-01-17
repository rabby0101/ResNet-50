**ResNet-50**:

ResNet-50 is a convolutional neural network (CNN) introduced in the 2015 paper “Deep Residual Learning for Image Recognition” by He Kaiming, Zhang Xiangyu, Ren Shaoqing, and Sun Jian. It is a specific type of residual neural network (ResNet) that forms networks by stacking residual blocks. ResNet-50 is a 50-layer CNN comprising 48 convolutional layers, one MaxPool layer, and one average pool layer ¹.

**ResNet-50 Architecture**
The original ResNet architecture was ResNet-34, which comprised 34 weighted layers. It provided a novel way to add more convolutional layers to a CNN, without running into the vanishing gradient problem, using the concept of shortcut connections. A shortcut connection “skips over” some layers, converting a regular network to a residual network. The regular network was based on the VGG neural networks (VGG-16 and VGG-19)—each convolutional network had a 3×3 filter. However, a ResNet has fewer filters and is less complex than a VGGNet. A 34-layer ResNet can achieve a performance of 3.6 billion FLOPs, and a smaller 18-layer ResNet can achieve 1.8 billion FLOPs, which is significantly faster than a VGG-19 Network with 19.6 billion FLOPs (read more in the ResNet paper, He et, al, 2015) ¹.

ResNet-50 uses a bottleneck design for the building block. A bottleneck residual block uses 1×1 convolutions, known as a “bottleneck”, which reduces the number of parameters and matrix multiplications. This enables much faster training of each layer. It uses a stack of three layers rather than two layers. The 50-layer ResNet architecture includes the following elements, as shown in the table below ¹:

| **Layer** | **Kernel Size** | **Number of Kernels** |
|-----------|----------------|-----------------------|
| 1         | 7×7            | 64                    |
| 2         | 3×3            | 64                    |
| 3         | 1×1            | 64                    |
| 4         | 3×3            | 64                    |
| 5         | 1×1            | 256                   |
| 6         | 3×3            | 128                   |
| 7         | 1×1            | 128                   |
| 8         | 3×3            | 128                   |
| 9         | 1×1            | 512                   |
| 10        | 3×3            | 256                   |
| 11        | 1×1            | 256                   |
| 12        | 3×3            | 256                   |
| 13        | 1×1            | 1024                  |
| 14        | 3×3            | 512                   |
| 15        | 1×1            | 512                   |
| 16        | 3×3            | 512                   |
| 17        | 1×1            | 2048                  |
| 18        | 3×3            | 512                   |
| 19        | 1×1            | 512                   |
| 20        | 3×3            | 512                   |

**Transfer Learning with ResNet-50**
ResNet-50 is a powerful image classification model that can be trained on large datasets and achieve state-of-the-art results. One of its key innovations is the use of residual connections, which help to mitigate the vanishing gradient problem. Transfer learning with ResNet-50 is a popular technique in deep learning, where the pre-trained model is used as a starting point for a new task. This can help to reduce the amount of data required to train a new model and improve its accuracy ¹.


Source: 
- Conversation with Bing, 17/01/2024
- ResNet-50: The Basics and a Quick Tutorial - Datagen. https://datagen.tech/guides/computer-vision/resnet-50/.
- Understanding ResNet50 architecture - OpenGenus IQ. https://iq.opengenus.org/resnet50-architecture/.
- Exploring ResNet50: An In-Depth Look at the Model Architecture ... - Medium. https://medium.com/@nitishkundu1993/exploring-resnet50-an-in-depth-look-at-the-model-architecture-and-code-implementation-d8d8fa67e46f.

# RoundIcon
You could use RoundIcon to generate round icon from local image or internet image for Android apps. Enjoy yourself!
## Usage
**1. generate jar file by gradle**

```
gradlew.bat jar
```
It will output RoundIcon.jar in the root project path.

**2. generate round icon**

```
java -jar RoundIcon.jar yuanshi.jpg icon.png 144 20 0
```
There are five parameters:

**param1**

The source image the round icon generated from, it could be a local image path or http url.

**param2**

The path for the output round icon, default value is ***icon.png***

**param3**

The width or height of the target round icon, default value is ***96***.

**param4**

The corner radius of the target round icon, default value is ***20***.

**param5**

This parameter will decide transform policy: which part of the original image would be transform to the round icon. Its value should be 0, 1 ,2, or 3. Its default value is ***0***.

***policy 0***

It will scale both side of the original image to the target size (***param3***), and make round corner without any crop operation.
The output image for yuanshi.jpg in the root project with policy 0 is 
![policy 0](https://github.com/baidusoso/RoundIcon/blob/master/icon0.png?raw=true "policy 0")

***policy 1***

It will scale the original image with the ratio: the target size(***param3***)/the smaller side size of the original image, crop at the ***top*** of the scaled output image, and make round corner.
The output image for yuanshi.jpg in the root project with policy 1 is 
![policy 1](https://github.com/baidusoso/RoundIcon/blob/master/icon1.png?raw=true "policy 1")

***policy 2***

It will scale the original image with the ratio: the target size(***param3***)/the smaller side size of the original image, crop at the ***center*** of the scaled output image, and make round corner.
The output image for yuanshi.jpg in the root project with policy 2 is 
![policy 2](https://github.com/baidusoso/RoundIcon/blob/master/icon2.png?raw=true "policy 2")

***policy 3***

It will scale the original image with the ratio: the target size(***param3***)/the smaller side size of the original image, crop at the ***bottom*** of the scaled output image, and make round corner.
The output image for yuanshi.jpg in the root project with policy 3 is 
![policy 3](https://github.com/baidusoso/RoundIcon/blob/master/icon3.png?raw=true "policy 3")

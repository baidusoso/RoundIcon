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

The path for the output round icon.

**param3**

The width or height of the target round icon.

**param4**

The corner radius of the target round icon.

**param5**

This parameter will decide transform policy: which part of the original image would be transform to the round icon. Its value should be 0, 1 ,2, or 3.

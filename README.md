# android-gif-animated-writer
Standalone Android GIF animated writer.

How to use:

```java
AnimatedGIFWriter writer = new AnimatedGIFWriter(true); // True for dither. Will need more memory and CPU
OutputStream os = new FileOutputStream("animated.gif");
Bitmap bitmap; // Grab the Bitmap whatever way you can
writer.prepareForWrite(os, -1, -1) // Use -1 for both logical screen width and height to use the first frame dimension
writer.writeFrame(os, bitmap);
// Keep adding frame here
writer.finishWrite(os);
// And you are done!!!
```

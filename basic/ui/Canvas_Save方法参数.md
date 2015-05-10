## Canvas save()方法参数

根据官方的解释，`Canvas.CLIP_SAVE_FLAG`和`Canvas.MATRIX_SAVE_FLAG`是指在恢复操作时恢复哪些属性。

```java
canvas.save(Canvas.CLIP_SAVE_FLAG);

canvas.rotate(10);
paint.setColor(Color.RED);
canvas.drawRect(centerX - 200, centerY - 200, centerX + 200, centerY + 200, paint);

canvas.restore();
```

这样一段代码，在restore后因为只恢复CLIP_SAVE_FLAG，而不会恢复Canvas旋转的操作，所以restore后的操作都是以rotate(10)这个操作为基础的。

# AndroidSVG

### Differences with the original repo

- Add scale option for rendering. The dpi value of the device can be passed as a parameter while rendering.

Example:

```
SVG svg = SVG.getFromInputStream(source);
svg.setDocumentWidth((int)(svg.getDocumentWidth() * AndroidUnitConverterUtil.density));
svg.setDocumentHeight((int) (svg.getDocumentHeight() * AndroidUnitConverterUtil.density));
var renderOptions = new RenderOptions();
renderOptions.scale(AndroidUnitConverterUtil.density);
Picture picture = svg.renderToPicture(renderOptions);
PictureDrawable drawable = new PictureDrawable(picture);
```

AndroidSVG is a SVG parser and renderer for Android.  It has almost complete support for the static
visual elements of the SVG 1.1 and SVG 1.2 Tiny specifications (except for filters).

*AndroidSVG is licensed under the [Apache License v2.0](http://www.apache.org/licenses/LICENSE-2.0)*.

[More information, including downloads and documentation, is available at the main AndroidSVG site.](http://bigbadaboom.github.io/androidsvg/)


### Find a bug?

Please file a [bug report](https://github.com/BigBadaboom/androidsvg/issues) and include as much detail as you can.
If possible, please include a sample SVG file showing the error.

If you wish to contact the author with feedback on this project, you can email me at
[androidsvgfeedback@gmail.com](mailto:androidsvgfeedback@gmail.com).


### Using AndroidSVG in your app?

If you have found AndroidSVG useful and are using it in your project, please let me know. I'd love to hear about it!

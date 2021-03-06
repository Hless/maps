## <MapboxGL.SymbolLayer />
### SymbolLayer is a style layer that renders icon and text labels at points or along lines on the map.

### props
| Prop | Type | Default | Required | Description |
| ---- | :--: | :-----: | :------: | :----------: |
| id | `string` | `none` | `false` | A string that uniquely identifies the source in the style to which it is added. |
| sourceID | `string` | `MapboxGL.StyleSource.DefaultSourceID` | `false` | The source from which to obtain the data to style. If the source has not yet been added to the current style, the behavior is undefined. |
| sourceLayerID | `string` | `none` | `false` | Identifier of the layer within the source identified by the sourceID property from which the receiver obtains the data to style. |
| aboveLayerID | `string` | `none` | `false` | Inserts a layer above aboveLayerID. |
| belowLayerID | `string` | `none` | `false` | Inserts a layer below belowLayerID |
| layerIndex | `number` | `none` | `false` | Inserts a layer at a specified index |
| filter | `array` | `none` | `false` | Filter only the features in the source layer that satisfy a condition that you define |
| minZoomLevel | `number` | `none` | `false` | The minimum zoom level at which the layer gets parsed and appears. |
| maxZoomLevel | `number` | `none` | `false` | The maximum zoom level at which the layer gets parsed and appears. |
| style | `union` | `none` | `false` | Customizable style attributes |


### styles

* <a href="#name">symbolPlacement</a><br/>
* <a href="#name-1">symbolSpacing</a><br/>
* <a href="#name-2">symbolAvoidEdges</a><br/>
* <a href="#name-3">symbolZOrder</a><br/>
* <a href="#name-4">iconAllowOverlap</a><br/>
* <a href="#name-5">iconIgnorePlacement</a><br/>
* <a href="#name-6">iconOptional</a><br/>
* <a href="#name-7">iconRotationAlignment</a><br/>
* <a href="#name-8">iconSize</a><br/>
* <a href="#name-9">iconTextFit</a><br/>
* <a href="#name-10">iconTextFitPadding</a><br/>
* <a href="#name-11">iconImage</a><br/>
* <a href="#name-12">iconRotate</a><br/>
* <a href="#name-13">iconPadding</a><br/>
* <a href="#name-14">iconKeepUpright</a><br/>
* <a href="#name-15">iconOffset</a><br/>
* <a href="#name-16">iconAnchor</a><br/>
* <a href="#name-17">iconPitchAlignment</a><br/>
* <a href="#name-18">textPitchAlignment</a><br/>
* <a href="#name-19">textRotationAlignment</a><br/>
* <a href="#name-20">textField</a><br/>
* <a href="#name-21">textFont</a><br/>
* <a href="#name-22">textSize</a><br/>
* <a href="#name-23">textMaxWidth</a><br/>
* <a href="#name-24">textLineHeight</a><br/>
* <a href="#name-25">textLetterSpacing</a><br/>
* <a href="#name-26">textJustify</a><br/>
* <a href="#name-27">textAnchor</a><br/>
* <a href="#name-28">textMaxAngle</a><br/>
* <a href="#name-29">textRotate</a><br/>
* <a href="#name-30">textPadding</a><br/>
* <a href="#name-31">textKeepUpright</a><br/>
* <a href="#name-32">textTransform</a><br/>
* <a href="#name-33">textOffset</a><br/>
* <a href="#name-34">textAllowOverlap</a><br/>
* <a href="#name-35">textIgnorePlacement</a><br/>
* <a href="#name-36">textOptional</a><br/>
* <a href="#name-37">visibility</a><br/>
* <a href="#name-38">iconOpacity</a><br/>
* <a href="#name-39">iconColor</a><br/>
* <a href="#name-40">iconHaloColor</a><br/>
* <a href="#name-41">iconHaloWidth</a><br/>
* <a href="#name-42">iconHaloBlur</a><br/>
* <a href="#name-43">iconTranslate</a><br/>
* <a href="#name-44">iconTranslateAnchor</a><br/>
* <a href="#name-45">textOpacity</a><br/>
* <a href="#name-46">textColor</a><br/>
* <a href="#name-47">textHaloColor</a><br/>
* <a href="#name-48">textHaloWidth</a><br/>
* <a href="#name-49">textHaloBlur</a><br/>
* <a href="#name-50">textTranslate</a><br/>
* <a href="#name-51">textTranslateAnchor</a><br/>

___

#### Name
`symbolPlacement`

#### Description
Label placement relative to its geometry.

#### Type
`enum`
#### Default Value
`point`

#### Supported Values
**point** - The label is placed at the point where the geometry is located.<br />
**line** - The label is placed along the line of the geometry. Can only be used on `LineString` and `Polygon` geometries.<br />
**line-center** - The label is placed at the center of the line of the geometry. Can only be used on `LineString` and `Polygon` geometries. Note that a single feature in a vector tile may contain multiple line geometries.<br />


#### Expression

Parameters: `zoom`

___

#### Name
`symbolSpacing`

#### Description
Distance between two symbol anchors.

#### Type
`number`
#### Default Value
`250`

#### Units
`pixels`

#### Minimum
`1`


#### Expression

Parameters: `zoom`

___

#### Name
`symbolAvoidEdges`

#### Description
If true, the symbols will not cross tile edges to avoid mutual collisions. Recommended in layers that don't have enough padding in the vector tile to prevent collisions, or if it is a point symbol layer placed after a line symbol layer.

#### Type
`boolean`
#### Default Value
`false`


#### Expression

Parameters: `zoom`

___

#### Name
`symbolZOrder`

#### Description
Controls the order in which overlapping symbols in the same layer are rendered

#### Type
`enum`
#### Default Value
`auto`

#### Supported Values
**auto** - If `symbol-sort-key` is set, sort based on that. Otherwise sort symbols by their y-position relative to the viewport.<br />
**viewport-y** - Symbols will be sorted by their y-position relative to the viewport.<br />
**source** - Symbols will be rendered in the same order as the source data with no sorting applied.<br />


#### Expression

Parameters: `zoom`

___

#### Name
`iconAllowOverlap`

#### Description
If true, the icon will be visible even if it collides with other previously drawn symbols.

#### Type
`boolean`
#### Default Value
`false`


#### Requires
`iconImage`

#### Expression

Parameters: `zoom`

___

#### Name
`iconIgnorePlacement`

#### Description
If true, other symbols can be visible even if they collide with the icon.

#### Type
`boolean`
#### Default Value
`false`


#### Requires
`iconImage`

#### Expression

Parameters: `zoom`

___

#### Name
`iconOptional`

#### Description
If true, text will display without their corresponding icons when the icon collides with other symbols and the text does not.

#### Type
`boolean`
#### Default Value
`false`


#### Requires
`iconImage, textField`

#### Expression

Parameters: `zoom`

___

#### Name
`iconRotationAlignment`

#### Description
In combination with `symbolPlacement`, determines the rotation behavior of icons.

#### Type
`enum`
#### Default Value
`auto`

#### Supported Values
**map** - When `symbol-placement` is set to `point`, aligns icons east-west. When `symbol-placement` is set to `line` or `line-center`, aligns icon x-axes with the line.<br />
**viewport** - Produces icons whose x-axes are aligned with the x-axis of the viewport, regardless of the value of `symbol-placement`.<br />
**auto** - When `symbol-placement` is set to `point`, this is equivalent to `viewport`. When `symbol-placement` is set to `line` or `line-center`, this is equivalent to `map`.<br />


#### Requires
`iconImage`

#### Expression

Parameters: `zoom`

___

#### Name
`iconSize`

#### Description
Scales the original size of the icon by the provided factor. The new pixel size of the image will be the original pixel size multiplied by `iconSize`. 1 is the original size; 3 triples the size of the image.

#### Type
`number`
#### Default Value
`1`

#### Units
`factor of the original icon size`

#### Minimum
`0`


#### Requires
`iconImage`

#### Expression

Parameters: `zoom, feature`

___

#### Name
`iconTextFit`

#### Description
Scales the icon to fit around the associated text.

#### Type
`enum`
#### Default Value
`none`

#### Supported Values
**none** - The icon is displayed at its intrinsic aspect ratio.<br />
**width** - The icon is scaled in the x-dimension to fit the width of the text.<br />
**height** - The icon is scaled in the y-dimension to fit the height of the text.<br />
**both** - The icon is scaled in both x- and y-dimensions.<br />


#### Requires
`iconImage, textField`

#### Expression

Parameters: `zoom`

___

#### Name
`iconTextFitPadding`

#### Description
Size of the additional area added to dimensions determined by `iconTextFit`, in clockwise order: top, right, bottom, left.

#### Type
`array<number>`
#### Default Value
`[0,0,0,0]`

#### Units
`pixels`


#### Requires
`iconImage, textField`

#### Expression

Parameters: `zoom`

___

#### Name
`iconImage`

#### Description
Name of image in sprite to use for drawing an image background.

#### Type
`string`


#### Expression

Parameters: `zoom, feature`

___

#### Name
`iconRotate`

#### Description
Rotates the icon clockwise.

#### Type
`number`
#### Default Value
`0`

#### Units
`degrees`


#### Requires
`iconImage`

#### Expression

Parameters: `zoom, feature`

___

#### Name
`iconPadding`

#### Description
Size of the additional area around the icon bounding box used for detecting symbol collisions.

#### Type
`number`
#### Default Value
`2`

#### Units
`pixels`

#### Minimum
`0`


#### Requires
`iconImage`

#### Expression

Parameters: `zoom`

___

#### Name
`iconKeepUpright`

#### Description
If true, the icon may be flipped to prevent it from being rendered upsideDown.

#### Type
`boolean`
#### Default Value
`false`


#### Requires
`iconImage`

#### Expression

Parameters: `zoom`

___

#### Name
`iconOffset`

#### Description
Offset distance of icon from its anchor. Positive values indicate right and down, while negative values indicate left and up. Each component is multiplied by the value of `iconSize` to obtain the final offset in pixels. When combined with `iconRotate` the offset will be as if the rotated direction was up.

#### Type
`array<number>`
#### Default Value
`[0,0]`


#### Requires
`iconImage`

#### Expression

Parameters: `zoom, feature`

___

#### Name
`iconAnchor`

#### Description
Part of the icon placed closest to the anchor.

#### Type
`enum`
#### Default Value
`center`

#### Supported Values
**center** - The center of the icon is placed closest to the anchor.<br />
**left** - The left side of the icon is placed closest to the anchor.<br />
**right** - The right side of the icon is placed closest to the anchor.<br />
**top** - The top of the icon is placed closest to the anchor.<br />
**bottom** - The bottom of the icon is placed closest to the anchor.<br />
**top-left** - The top left corner of the icon is placed closest to the anchor.<br />
**top-right** - The top right corner of the icon is placed closest to the anchor.<br />
**bottom-left** - The bottom left corner of the icon is placed closest to the anchor.<br />
**bottom-right** - The bottom right corner of the icon is placed closest to the anchor.<br />


#### Requires
`iconImage`

#### Expression

Parameters: `zoom, feature`

___

#### Name
`iconPitchAlignment`

#### Description
Orientation of icon when map is pitched.

#### Type
`enum`
#### Default Value
`auto`

#### Supported Values
**map** - The icon is aligned to the plane of the map.<br />
**viewport** - The icon is aligned to the plane of the viewport.<br />
**auto** - Automatically matches the value of `icon-rotation-alignment`.<br />


#### Requires
`iconImage`

#### Expression

Parameters: `zoom`

___

#### Name
`textPitchAlignment`

#### Description
Orientation of text when map is pitched.

#### Type
`enum`
#### Default Value
`auto`

#### Supported Values
**map** - The text is aligned to the plane of the map.<br />
**viewport** - The text is aligned to the plane of the viewport.<br />
**auto** - Automatically matches the value of `text-rotation-alignment`.<br />


#### Requires
`textField`

#### Expression

Parameters: `zoom`

___

#### Name
`textRotationAlignment`

#### Description
In combination with `symbolPlacement`, determines the rotation behavior of the individual glyphs forming the text.

#### Type
`enum`
#### Default Value
`auto`

#### Supported Values
**map** - When `symbol-placement` is set to `point`, aligns text east-west. When `symbol-placement` is set to `line` or `line-center`, aligns text x-axes with the line.<br />
**viewport** - Produces glyphs whose x-axes are aligned with the x-axis of the viewport, regardless of the value of `symbol-placement`.<br />
**auto** - When `symbol-placement` is set to `point`, this is equivalent to `viewport`. When `symbol-placement` is set to `line` or `line-center`, this is equivalent to `map`.<br />


#### Requires
`textField`

#### Expression

Parameters: `zoom`

___

#### Name
`textField`

#### Description
Value to use for a text label. If a plain `string` is provided, it will be treated as a `formatted` with default/inherited formatting options.

#### Type
`formatted`
#### Default Value
``


#### Expression

Parameters: `zoom, feature`

___

#### Name
`textFont`

#### Description
Font stack to use for displaying text.

#### Type
`array<string>`
#### Default Value
`[Open Sans Regular,Arial Unicode MS Regular]`


#### Requires
`textField`

#### Supported Style Functions
`camera`
#### Expression

Parameters: `zoom, feature`

___

#### Name
`textSize`

#### Description
Font size.

#### Type
`number`
#### Default Value
`16`

#### Units
`pixels`

#### Minimum
`0`


#### Requires
`textField`

#### Expression

Parameters: `zoom, feature`

___

#### Name
`textMaxWidth`

#### Description
The maximum line width for text wrapping.

#### Type
`number`
#### Default Value
`10`

#### Units
`ems`

#### Minimum
`0`


#### Requires
`textField`

#### Supported Style Functions
`camera`
#### Expression

Parameters: `zoom, feature`

___

#### Name
`textLineHeight`

#### Description
Text leading value for multiLine text.

#### Type
`number`
#### Default Value
`1.2`

#### Units
`ems`


#### Requires
`textField`

#### Expression

Parameters: `zoom`

___

#### Name
`textLetterSpacing`

#### Description
Text tracking amount.

#### Type
`number`
#### Default Value
`0`

#### Units
`ems`


#### Requires
`textField`

#### Supported Style Functions
`camera`
#### Expression

Parameters: `zoom, feature`

___

#### Name
`textJustify`

#### Description
Text justification options.

#### Type
`enum`
#### Default Value
`center`

#### Supported Values
**auto** - The text is aligned towards the anchor position.<br />
**left** - The text is aligned to the left.<br />
**center** - The text is centered.<br />
**right** - The text is aligned to the right.<br />


#### Requires
`textField`

#### Supported Style Functions
`camera`
#### Expression

Parameters: `zoom, feature`

___

#### Name
`textAnchor`

#### Description
Part of the text placed closest to the anchor.

#### Type
`enum`
#### Default Value
`center`

#### Supported Values
**center** - The center of the text is placed closest to the anchor.<br />
**left** - The left side of the text is placed closest to the anchor.<br />
**right** - The right side of the text is placed closest to the anchor.<br />
**top** - The top of the text is placed closest to the anchor.<br />
**bottom** - The bottom of the text is placed closest to the anchor.<br />
**top-left** - The top left corner of the text is placed closest to the anchor.<br />
**top-right** - The top right corner of the text is placed closest to the anchor.<br />
**bottom-left** - The bottom left corner of the text is placed closest to the anchor.<br />
**bottom-right** - The bottom right corner of the text is placed closest to the anchor.<br />


#### Requires
`textField`

#### Supported Style Functions
`camera`
#### Expression

Parameters: `zoom, feature`

___

#### Name
`textMaxAngle`

#### Description
Maximum angle change between adjacent characters.

#### Type
`number`
#### Default Value
`45`

#### Units
`degrees`


#### Requires
`textField`

#### Expression

Parameters: `zoom`

___

#### Name
`textRotate`

#### Description
Rotates the text clockwise.

#### Type
`number`
#### Default Value
`0`

#### Units
`degrees`


#### Requires
`textField`

#### Expression

Parameters: `zoom, feature`

___

#### Name
`textPadding`

#### Description
Size of the additional area around the text bounding box used for detecting symbol collisions.

#### Type
`number`
#### Default Value
`2`

#### Units
`pixels`

#### Minimum
`0`


#### Requires
`textField`

#### Expression

Parameters: `zoom`

___

#### Name
`textKeepUpright`

#### Description
If true, the text may be flipped vertically to prevent it from being rendered upsideDown.

#### Type
`boolean`
#### Default Value
`true`


#### Requires
`textField`

#### Expression

Parameters: `zoom`

___

#### Name
`textTransform`

#### Description
Specifies how to capitalize text, similar to the CSS `textTransform` property.

#### Type
`enum`
#### Default Value
`none`

#### Supported Values
**none** - The text is not altered.<br />
**uppercase** - Forces all letters to be displayed in uppercase.<br />
**lowercase** - Forces all letters to be displayed in lowercase.<br />


#### Requires
`textField`

#### Expression

Parameters: `zoom, feature`

___

#### Name
`textOffset`

#### Description
Offset distance of text from its anchor. Positive values indicate right and down, while negative values indicate left and up.

#### Type
`array<number>`
#### Default Value
`[0,0]`

#### Units
`ems`


#### Requires
`textField`

#### Disabled By
`textRadialOffset`

#### Expression

Parameters: `zoom, feature`

___

#### Name
`textAllowOverlap`

#### Description
If true, the text will be visible even if it collides with other previously drawn symbols.

#### Type
`boolean`
#### Default Value
`false`


#### Requires
`textField`

#### Expression

Parameters: `zoom`

___

#### Name
`textIgnorePlacement`

#### Description
If true, other symbols can be visible even if they collide with the text.

#### Type
`boolean`
#### Default Value
`false`


#### Requires
`textField`

#### Expression

Parameters: `zoom`

___

#### Name
`textOptional`

#### Description
If true, icons will display without their corresponding text when the text collides with other symbols and the icon does not.

#### Type
`boolean`
#### Default Value
`false`


#### Requires
`textField, iconImage`

#### Expression

Parameters: `zoom`

___

#### Name
`visibility`

#### Description
Whether this layer is displayed.

#### Type
`enum`
#### Default Value
`visible`

#### Supported Values
**visible** - The layer is shown.<br />
**none** - The layer is not shown.<br />



___

#### Name
`iconOpacity`

#### Description
The opacity at which the icon will be drawn.

#### Type
`number`
#### Default Value
`1`

#### Minimum
`0`


#### Maximum
`1`

#### Requires
`iconImage`

#### Expression

Parameters: `zoom, feature, feature-state`

___

#### Name
`iconColor`

#### Description
The color of the icon. This can only be used with sdf icons.

#### Type
`color`
#### Default Value
`#000000`


#### Requires
`iconImage`

#### Expression

Parameters: `zoom, feature, feature-state`

___

#### Name
`iconHaloColor`

#### Description
The color of the icon's halo. Icon halos can only be used with SDF icons.

#### Type
`color`
#### Default Value
`rgba(0, 0, 0, 0)`


#### Requires
`iconImage`

#### Expression

Parameters: `zoom, feature, feature-state`

___

#### Name
`iconHaloWidth`

#### Description
Distance of halo to the icon outline.

#### Type
`number`
#### Default Value
`0`

#### Units
`pixels`

#### Minimum
`0`


#### Requires
`iconImage`

#### Expression

Parameters: `zoom, feature, feature-state`

___

#### Name
`iconHaloBlur`

#### Description
Fade out the halo towards the outside.

#### Type
`number`
#### Default Value
`0`

#### Units
`pixels`

#### Minimum
`0`


#### Requires
`iconImage`

#### Expression

Parameters: `zoom, feature, feature-state`

___

#### Name
`iconTranslate`

#### Description
Distance that the icon's anchor is moved from its original placement. Positive values indicate right and down, while negative values indicate left and up.

#### Type
`array<number>`
#### Default Value
`[0,0]`

#### Units
`pixels`


#### Requires
`iconImage`

#### Expression

Parameters: `zoom`

___

#### Name
`iconTranslateAnchor`

#### Description
Controls the frame of reference for `iconTranslate`.

#### Type
`enum`
#### Default Value
`map`

#### Supported Values
**map** - Icons are translated relative to the map.<br />
**viewport** - Icons are translated relative to the viewport.<br />


#### Requires
`iconImage, iconTranslate`

#### Expression

Parameters: `zoom`

___

#### Name
`textOpacity`

#### Description
The opacity at which the text will be drawn.

#### Type
`number`
#### Default Value
`1`

#### Minimum
`0`


#### Maximum
`1`

#### Requires
`textField`

#### Expression

Parameters: `zoom, feature, feature-state`

___

#### Name
`textColor`

#### Description
The color with which the text will be drawn.

#### Type
`color`
#### Default Value
`#000000`


#### Requires
`textField`

#### Expression

Parameters: `zoom, feature, feature-state`

___

#### Name
`textHaloColor`

#### Description
The color of the text's halo, which helps it stand out from backgrounds.

#### Type
`color`
#### Default Value
`rgba(0, 0, 0, 0)`


#### Requires
`textField`

#### Expression

Parameters: `zoom, feature, feature-state`

___

#### Name
`textHaloWidth`

#### Description
Distance of halo to the font outline. Max text halo width is 1/4 of the fontSize.

#### Type
`number`
#### Default Value
`0`

#### Units
`pixels`

#### Minimum
`0`


#### Requires
`textField`

#### Expression

Parameters: `zoom, feature, feature-state`

___

#### Name
`textHaloBlur`

#### Description
The halo's fadeout distance towards the outside.

#### Type
`number`
#### Default Value
`0`

#### Units
`pixels`

#### Minimum
`0`


#### Requires
`textField`

#### Expression

Parameters: `zoom, feature, feature-state`

___

#### Name
`textTranslate`

#### Description
Distance that the text's anchor is moved from its original placement. Positive values indicate right and down, while negative values indicate left and up.

#### Type
`array<number>`
#### Default Value
`[0,0]`

#### Units
`pixels`


#### Requires
`textField`

#### Expression

Parameters: `zoom`

___

#### Name
`textTranslateAnchor`

#### Description
Controls the frame of reference for `textTranslate`.

#### Type
`enum`
#### Default Value
`map`

#### Supported Values
**map** - The text is translated relative to the map.<br />
**viewport** - The text is translated relative to the viewport.<br />


#### Requires
`textField, textTranslate`

#### Expression

Parameters: `zoom`


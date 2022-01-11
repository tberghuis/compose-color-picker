# Android Jetpack Compose Color Picker 🎨

![Maven Central](https://img.shields.io/maven-central/v/com.godaddy.android.colorpicker/compose-color-picker?style=flat-square)

A component that provides an HSV color picker, written in Jetpack compose.

<img src="screenshots/ColorPicker.gif" width="200"  />

## How to get started

Add the dependency to your `build.gradle` file:

```
implementation 'com.godaddy.android.colorpicker:compose-color-picker:<latest-version>'

// with Android ColorInt extensions
implementation 'com.godaddy.android.colorpicker:compose-color-picker-android:<latest-version>'
// desktop jvm version
implementation 'com.godaddy.android.colorpicker:compose-color-picker-jvm:<latest-version>'
```

Add `ClassicColorPicker` to your Compose hierarchy:

```
import com.godaddy.android.colorpicker.HsvColor

Column {
    ClassicColorPicker(
        onColorChanged = { color: HsvColor ->
            // Do something with the color
        }
    )
}
```

## Customizing the control

### Size

To change the size of the control, pass in the `Modifier` option:

```
import com.godaddy.android.colorpicker.HsvColor

ClassicColorPicker(
    modifier = Modifier.height(200.dp),
    onColorChanged = { color: HsvColor ->
        // Do something with the color
    }
)
```

### Alpha

To hide the alpha bar, change the `showAlphaBar` parameter:

```
import com.godaddy.android.colorpicker.HsvColor

ClassicColorPicker(
    showAlphaBar = false,
    onColorChanged = { color: HsvColor ->
        // Do something with the color
    }
)
```


### To make a release

1. Update the version number in color-picker/build.gradle.kts
2. Make a PR into main and get that merged
3. Run "Deploy to Sonatype" GitHub Action.
4. Login to Sonatype and "Close" release. After a few minutes, click "Release". 
5. Release should then be available for download on maven (might take like 30 min to propagate).


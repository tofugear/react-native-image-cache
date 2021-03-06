# Image caching for Android

##### Props:
| Property | Type | Default | Description |
|---------------|----------|--------------|----------------------------------------------------------------|
| src | string | null | http source of the image |
| tintColor | string | null | optional tintColor |
| onLoad | function | null | optional onLoad function |
| borderRadius | number | null | optional borderRadius number |


## Example
```jsx
import Image from 'react-native-image-cache'


<Image onLoad={()=>{
  ToastAndroid.show(`OnLoad`, ToastAndroid.LONG)
}} borderRadius={2} style={styles.image} src={"http://placehold.it/500"}></Image>
```

## Include in your App


Installation
------------

Install the npm package [`react-native-image-cache`](https://www.npmjs.com/package/react-native-image-cache). Inside your React Native project, run ([example](https://github.com/Anthonyzou/react-native-image-cache/tree/master/example)):

```bash
npm install --save react-native-image-cache
```

In `android/settings.gradle` add the following lines

```
include :react-native-image-cache'
project(':react-native-image-cache').projectDir = file('../node_modules/react-native-image-cache/android')
```

**NOTE** : If you have included other libraries in your project, the `include` line will contain the other dependencies too.

In `android/app/build.gradle`, add a dependency to `':react-native-image-cache'`
```
dependencies {
    compile project(':react-native-image-cache')
}
```

Next, you need to change the `MainActivity` of your app to register `ReactImageCache` :
```java
import com.image.cache.ReactImageCache; // add this import

public class MainActivity extends ReactActivity {
    //...

    @Override
    protected List<ReactPackage> getPackages() {
      return Arrays.<ReactPackage>asList(
          new MainReactPackage(),
          new ReactImageCache() // add this manager
      );
    }
```

---

TeamLockr image caching
Team Lockr image caching for react native

These are functions created by the TeamLockr Team created for the TeamLockr platform.

---

# React Native Windows in a Packaging Solution

This is an example of a problem when an RNW application is failing to build if added to Packaging Project. The build error is:

```
8>C:\Users\User\RNWPackagingProblem\node_modules\react-native-windows\PropertySheets\Autolink.props(12,5): error MSB4184: The expression "[MSBuild]::MakeRelative(C:\Users\User\RNWPackagingProblem, *Undefined*)" cannot be evaluated. Illegal characters in path.  C:\Users\User\RNWPackagingProblem\node_modules\react-native-windows\PropertySheets\Autolink.props
```

## Solution

If we open `node_modules/react-natuve-windows/PropertySheets/Autolink.props` and delete line #12, the build succeeds. Not sure if it's a good one, but it's something I was able to find.
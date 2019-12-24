# Sandbox
Patch for RNFetchBlob


This is patch for RNFetchBlob lib to make it allow background downloads.

Please refer to commit "RNFetchBlob patch" (5f88be5ab45e0fc628fe9ddb6aefed8383fe3ebe) to see required changes.

When the patch is done, JS code should be updated as well (ModelTalkerController.js and CereprocDownload.js as I can see, but may be mistaken)
The update is: whenever using RNFetchBlob in iOS and background download required, pass bool option for "IOSBackgroundTask".
Looks like dev was going to add background functionality for lib but dropped it halfway, so the option is already part of the lib,
you can see it's being read from options in RNFetchBlobRequest.m line 84.

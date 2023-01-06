MarsPhotos - Starter Code
==================================

Starter code for [Android Basics in Kotlin](https://developer.android.com/courses/android-basics-kotlin/unit-4).

Introduction
------------

Using this stater code you will create MarsPhotos is a demo app that shows actual images of Mar's surface. These images are
real-life photos from Mars captured by NASA's Mars rovers. The data is stored on a Web server
as a REST web service.  The solution app will demonstrate the use of [Retrofit](https://square.github.io/retrofit/) to make REST requests to the web service, [Moshi](https://github.com/square/moshi) to
handle the deserialization of the returned JSON to Kotlin data objects, and [Coil](https://coil-kt.github.io/coil/) to load images by URL.

The app also leverages [ViewModel](https://developer.android.com/topic/libraries/architecture/viewmodel),
[LiveData](https://developer.android.com/topic/libraries/architecture/livedata), and
[Data Binding](https://developer.android.com/topic/libraries/data-binding/) with binding 
adapters.

Summary
--------------

### REST web services

- A web service is software-based functionality offered over the internet that enables your app to make requests and get data back.
- Common web services use a REST architecture. Web services that offer REST architecture are known as RESTful services. RESTful web services are built using standard web components and protocols.
- You make a request to a REST web service in a standardized way, via URIs.
- To use a web service, an app must establish a network connection and communicate with the service. Then the app must receive and parse response data into a format the app can use.
- The Retrofit library is a client library that enables your app to make requests to a REST web service.
- Use converters to tell Retrofit what to do with data it sends to the web service and gets back from the web service. For example, the ScalarsConverter converter treats the web service data as a String or other primitive.
- To enable your app to make connections to the internet, add the "android.permission.INTERNET" permission in the Android manifest.

### JSON parsing

- The response from a web service is often formatted in JSON, a common format for representing structured data.
- A JSON object is a collection of key-value pairs.
- A collection of JSON objects is a JSON array. You get a JSON array as a response from a web service.
- The keys in a key-value pair are surrounded by quotes. The values can be numbers or strings.
- The Moshi library is an Android JSON parser that converts a JSON string into Kotlin objects. Retrofit has a converter that works with Moshi.
- Moshi matches the keys in a JSON response with properties in a data object that have the same name.
To use a different property name for a key, annotate that property with the @Json annotation and the JSON key name.

### Load and display images from the Internet
- The Coil library simplifies the process of managing images, such as download, buffer, decode, and cache images in your app.
- Binding adapters are extension methods that sit between a view and that view's bound data. Binding adapters provide custom behavior when the data changes, for example, to call Coil to load an image from a URL into an ImageView.
- Binding adapters are extension methods annotated with the @BindingAdapter annotation.
- To display a grid of images, use a RecyclerView with a GridLayoutManager.
- To update the list of properties when it changes, use a binding adapter between the RecyclerView and the layout.

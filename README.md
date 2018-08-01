# NumbersLight

Min API : 14+

Asumptions :
- I understood the "Each item should be highlighted when user clicks on it" 
as being highlighted only for the duration of the click, and not as being hightlighted permanently (or before being reclicked) after a click.

UI choices :
- As specified "not very important", used basic default components.

Architecture choices:
- As there is almost no user interaction (except clicking on list item) and the whole applciation being quite small, I did not create any Presenter interface. 
A Singleton Network Manager handles the network requests (2 different methods), and is directly called from the Activity.
Some Static Utilities classes and methods are also used by the Activity.

Library choices:
- OKHttp for Http request (fast, asynchronous and easy to use)
- Picasso to load and display the pictures (fast, asynchronous and easy to use)
I did not use RxJava despite the recommandations as I am not familiar at all with it.

Additional requirements:
- Unit test for the Model Class in Kotlin. Unfortunately, can't do much unit test with JSONObject and most of the code use JSONObjects.
- Application written in Java. Unit test class, Item, and ItemUtilities in Kotlin (I reckon they are quite simple, but they're used ;) )
- Logs only in Debug build config

Tested on :
Real device smartphone Honor 7X Android 8 : API 26
Emulator Tablet Nexus 7 : API 16

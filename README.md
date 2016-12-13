Here's the minimal basic project to reproduce the conflict between Robolectric and AppsFlyer. It's a basic generated Android App (via Android Studio), with a single commit to add the AppsFlyer and Robolectric dependencies, as well as the AppsFlyer BroadcastReceiver and the code to change the sample unit test to a Robolectric test. See commit 1039512 for just the code that does this.

To run:
* checkout the project
* run `./gradlew test`
* test should fail. if you look at the generated html report, you'll see the `Expecting a stackmap frame` error.

# Espresso

Use Espresso to write concise, beautiful, and reliable Android UI tests.

The following code snippet shows an example of an Espresso test:

    @Test
    public void greeterSaysHello() {
    onView(withId(R.id.name_field)).perform(typeText("Steve"));
    onView(withId(R.id.greet_button)).perform(click());
    onView(withText("Hello Steve!")).check(matches(isDisplayed()));
    }

**Synchronization capabilities**
Each time your test invokes `onView()`, Espresso waits to perform the corresponding UI action or assertion until the following synchronization conditions are met:

* The message queue is empty.
* There are no instances of `AsyncTask` currently executing a task.
* All developer-defined idling resources are idle.

**Packages**
- espresso-core
- espresso-web 
- espresso-idling-resource
- espresso-contrib
- espresso-intents
- espresso-remote

## Create UI tests with Espresso Test Recorder
The Espresso Test Recorder tool lets you create UI tests for your app without writing any test code. 
**Record an Espresso test**
Espresso tests consist of two primary components:
- UI interactions : include tap and type actions that a person may use to interact with your app.
- assertions on View elements :  verify the existence or contents of visual elements on the screen.

*Record UI interactions*
To start recording a test with Espresso Test Recorder, proceed as follows:

1. Click Run > Record Espresso Test.
2. In the Select Deployment Target window, choose the device on which you want to record the test. Click OK.
3. Espresso Test Recorder triggers a build of your project, and the app must install and launch before Espresso Test Recorder allows you to interact with it. The Record Your Test window appears after the app launches, and since you have not interacted with the device yet, the main panel reads "No events recorded yet." Interact with your device to start logging events such as "tap" and "type" actions.

*Add assertions to verify UI elements*
Assertions verify the existence or contents of a View element through three main types:
1. text is: Checks the text content of the selected View element
2. exists: Checks that the View element is present in the current View hierarchy visible on the screen
3. does not exist: Checks that the View element is not present in the current View hierarchy
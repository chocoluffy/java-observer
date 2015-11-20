### Learn how to use observable and observer in java ###

one thing i want the first mention is that the shortcut key for switching between different tabs. shift + command + []; and the shortcut for run is control + alt + r.

here in this example, the parcel class is a observable and the class company and customer are a observer.

in the main method, we can add observer object into observerable object's list like:

```java
order1.addObserver(store);
order1.updateLocation("Calgary, AB");
```
The basic idea here is that when updated infomation on observeable, key lines in obseverable:

```java
setChanged();
notifyObservers("some info about the updated object");
```

Then, we peek inside different observer class, finding out that they both share a update method:

```java
public void update(Observable o, Object arg) {
	 System.out.println("Company " + this.name +
                " observed a change in " + o);
        System.out.println("   The notification said: " + arg);
}
```

one point for the review purpose is that if we define a toString method for a object, we can do this in string concantenation.






























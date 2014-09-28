Emitting your own events
===================================

 - **emit<a name="emit"></a>**

    _Fire custom event_

    <u>Example:</u>

```xml
  <!-- Fire dummyEvent event of the customEventNotifier -->
    <div data-anijs="if: click, do: fadeIn animated, to: #container, after: emit customEventNotifier.dummyEvent"> </div>
    <!-- Listen and act when the dummyEvent event of the customEventNotifier ocurres -->
    <div data-anijs="if: dummyEvent, on: $customEventNotifier, do: $addClass hidden,  to: $children #container | div"> </div>
```
In order to emit a custom event, the only thing to do is select two names: *notifier name* and *event name*. Then, you will use those names as the above example, in two places: where you are going to fired the event, and in the place you are going to listen for the event occurrence.

    <u>Remember the files to include...</u>
    
```xml
   <!--The core library-->
    <script src="anijs-min.js"></script>

   <!-- Main helpers library -->
    <script src="anijs-helper-dom-min.js"></script>
```

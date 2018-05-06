#  Implementation of listeners and event handlers

## Python

* The Listener class is an “abstract” base class for any objects which wish to register to receive notifications of new messages on the bus.

* A Listener can be used in two ways; the default is to call the Listener with a new message, or by calling the method on_message_received.

* For event handlers, Python has its own events.EventHandler(sender) class, which is a simple event handling class that manages callbacks to be executed.

    ```python
    def on_message_received(self, msg):
        print(msg)
    class MyClass(object):
        def __init__(self):
        self.anevent = EventHandler(self)

    ```

## C#

* An event is a message sent by an object to signal the occurrence of an action. The action could be caused by user interaction, such as a button click, or it could be raised by some other program logic, such as changing a property’s value. The object that raises the event is called the event sender. The event sender doesn't know which object or method will receive (handle) the events it raises. The event is typically a member of the event sender; for example, the Click event is a member of the Button class, and the PropertyChanged event is a member of the class that implements the INotifyPropertyChanged interface.

    ```c#
    class Counter
    {
        public event EventHandler ThresholdReached;

        protected virtual void OnThresholdReached(EventArgs e)
        {
            EventHandler handler = ThresholdReached;
            if (handler != null)
            {
                handler(this, e);
            }
        }

        // provide remaining implementation for the class
    }
    ```

* Delegates 

  A delegate is a type that holds a reference to a method. A delegate is declared with a signature that shows the return type and parameters for the methods it references, and can hold references only to methods that match its signature. A delegate is thus equivalent to a type-safe function pointer or a callback. A delegate declaration is sufficient to define a delegate class.

  ```c#
    public delegate void ThresholdReachedEventHandler(object sender, ThresholdReachedEventArgs e);
  ```

* Event Handlers

  To respond to an event, you define an event handler method in the event receiver. This method must match the signature of the delegate for the event you are handling. In the event handler, you perform the actions that are required when the event is raised, such as collecting user input after the user clicks a button. To receive notifications when the event occurs, your event handler method must subscribe to the event.

    ```c#
    class Program
    {
        static void Main(string[] args)
        {
            Counter c = new Counter();
            c.ThresholdReached += c_ThresholdReached;

            // provide remaining implementation for the class
        }

        static void c_ThresholdReached(object sender, EventArgs e)
        {
            Console.WriteLine("The threshold was reached.");
        }
    }
    ```
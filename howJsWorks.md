

# Call Stack
The call stack is a data structure used by the programming language to keep track of function calls in a program. Whenever a function is called, a new frame (or context) is added to the top of the call stack, representing that function's execution context. When the function completes its execution, its frame is removed from the call stack, and the control returns to the previous function in the stack. This process continues until the call stack becomes empty, indicating that the program has finished executing.


# Callback Queue:
The callback queue (also known as the "task queue" or "message queue") is a queue data structure that holds callback functions waiting to be executed. In asynchronous programming, when certain events or asynchronous operations complete (e.g., network requests, timers, or user interactions), the corresponding callback functions are not executed immediately. Instead, they are pushed into the callback queue.

# Microtask Queue:
The microtask queue (also known as "job queue" or "microtask queue") is another queue data structure used for holding microtasks. Microtasks are tasks that have higher priority than regular tasks (callbacks) in the event loop. They are typically used for handling promises and other microtask-specific functionalities.



# HOW THEY WORK TOGETHER

## Call Stack and Callback Queue:
When synchronous code is executed, function calls are added to the call stack in the order they are encountered. However, when asynchronous operations are encountered, such as setTimeout or AJAX requests, they are removed from the main thread of execution and are handled separately by the browser or runtime environment.

Once an asynchronous operation is completed (e.g., the timer expires, or the AJAX response is received), the corresponding callback function is placed in the callback queue, waiting for the call stack to be empty.

When the call stack becomes empty (i.e., all synchronous code has finished executing), the event loop checks the callback queue. If there are any items in the callback queue, the event loop moves them from the callback queue to the call stack, and the callback functions are executed one by one.

## Callback Queue and Microtask Queue:
The microtask queue has a higher priority than the callback queue in the event loop. It means that microtasks are executed before the next regular task (callback) is taken from the callback queue and executed.

So, after the call stack becomes empty and before any regular callbacks are executed, the event loop checks the microtask queue first. If there are any microtasks in the queue, they are executed one by one until the microtask queue becomes empty. Only then does the event loop proceed to process items from the callback queue.

This priority distinction between microtasks and callbacks is essential for certain tasks, such as ensuring that promise resolutions are handled before any UI updates occur, improving responsiveness and consistency in applications.

In summary, the call stack is responsible for tracking the execution context of functions, the callback queue holds callback functions waiting to be executed, and the microtask queue holds microtasks with higher priority than regular tasks (callbacks) in the event loop. Understanding these components and their relationship is crucial for writing efficient and responsive asynchronous code.
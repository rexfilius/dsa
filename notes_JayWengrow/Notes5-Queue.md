A queue is another data structure designed to process temporary data. It’s like a stack in many ways, except that it processes data in a different order. 

Like a stack, a queue is also an abstract data type.
You can think of a queue as a line of people at the movie theater.
The first one in the line is the first one to leave the line and enter
the theater. 

With queues, the first item added to the queue is the first item to be removed. That’s why computer scientists apply the acronym “FIFO” to queues: First In, First Out.

Like stacks, queues are arrays with three restrictions:
1. Data can be inserted only at the end of a queue.
2. Data can be deleted only from the front of a queue.
3. Only the element at the front of a queue can be read.

Queues are common in many applications, ranging from printing jobs to background workers in web applications.

Queues are also the perfect tool for handling asynchronous requests - they ensure that the requests are processed in the order in which they were received. They are also commonly used to model real-world scenarios where events need to occur in a certain order, such as airplanes waiting for takeoff and patients waiting for their doctor.


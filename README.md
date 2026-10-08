# CSC-122-wk7

## Unique-corn
You want to create a class that represents a Unicorn. A unicorn has a name. However, unicorns are magical, and no two unicorns can have the same name! Your constructor for unicorn should thus print an error message if you try to make a unicorn with a name that's already taken.

In addition, Unicorns lose their magic when they die, and their name can be used by a new unicorn. Thus, you should make a destructor that frees up the name when a unicorn is destroyed.

Hint: Remember that static variables exist! A static variable in a class has a single value that is shared across all objects of this class.

Motivation: While this is a bit of a fantastical context, this is actually a very real pattern. Imagine a more realistic case where we have Tasks and Workers. These probably represent some computing tasks, and the workers are computers that can do a task. When we create a task, we want to give it a worker. However, we don't want to give it a worker who's already busy doing a different task! And when a task is finished, the worker is now free to be used by a different task.

Also answer these TPQs:

1) In this lab, our constructor accepts a name and prints an error if that name is in use. However, in a task/worker context as discussed in the lab description, it would be better to guarantee that we choose a worker that is available, and only throw an error if there are no free workers. Discuss how you might implement a system where creating a Unicorn picks an unused name from a predetermined list of names.

2) Imagine a unicorn also has a fairy companion. When a unicorn is born (constructed), a fairy object is also created, and the fairy has the same name as the unicorn. Now, assume the fairy's lifespan is not tied to its unicorn's. So if a unicorn dies (is destructed), the fairy still exists and has the name. When a unicorn is born, it's name must not match the name of a living unicorn, or a living fairy. Also, unicorns may outlive fairies, and still have the name! Describe at a high level how you would handle implementing this system.

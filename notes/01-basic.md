# Basic Operation

```
# added as a node to the default grpah
hello = tf.constant('Hello, Tensorflow!')

# create a TF session
sess = tf.Session()

# run the operation
print(sess.run(hello))
```

In TF, we do not run the session right away, instead, we create a *computational graph* and add the nodes (Tensor). 

After we finish required nodes, we now can run the session, and nodes will run.

##### computational graph - additon
```
node1 = tf.constant(3.0, tf.float32)
node2 = tf.constant(4.0) # implicitly tf.float32
node3 = tf.add(node1, node2) # or node3 = node1 + node2

print('sees.run(node1, node2): ', sess,run([node1, node2]))
print('sess.run(node3): ', sess.run(node3))
```

## Placeholder
In the previous example, we manually defined the values for node1 and node2. What if we want to throw the values for node1 and node2? 

Here is the example.
```
a = tf.placeholder(tf.float32)
b = tf.placeholder(tf.float32)
adder_node = a + b

print(sess.run(adder_node, feed_dict = {a: 3, b: 4.5}))
print(sess.run(adder_node, feed_dict = {a: [1, 3], b: [2, 4]}))
```

## Ranks, Shapes, and Types

### Rank
Rank is the dimension of the tensor.

* `s = 483 # scalar (rank = 0)`
* `v = [1, 2, 3] # vector(rank = 1)`
* `m = [[1, 2, 3], [4, 5, 6]] # matrix(rank = 2)`
* `t = [[[2], [4], [6]], [[8], [10], [112]]] # 3-tensor`

### Shapes
Shape is the number of elements in the list.

```
t = [[1, 2, 3], [4, 5, 6]] # (2, 3) shape
```

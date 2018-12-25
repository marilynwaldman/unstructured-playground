# Spark RDDs

Transformations

* map
* filter
* flatmap
* union
* distinct
* groupByKey
* reduceByKey
* sortByKey
* join

Actions

* reduce
* collect
* count
* first
* take
* takeOrdered
* saveAsTextFile

  | Meaning |
  | :--- |
  | Aggregate the elements of the dataset using a function func \(which takes two arguments and returns one\). The function should be commutative and associative so that it can be computed correctly in parallel. |
  | Return all the elements of the dataset as an array at the driver program. This is usually useful after a filter or other operation that returns a sufficiently small subset of the data. |
  | Return the number of elements in the dataset. |
  | Return the first element of the dataset \(similar to take\(1\)\). |
  | Return an array with the first n elements of the dataset. |
  | Return an array with a random sample of num elements of the dataset, with or without replacement, optionally pre-specifying a random number generator seed. |
  | Return the first n elements of the RDD using either their natural order or a custom comparator. |
  |  |


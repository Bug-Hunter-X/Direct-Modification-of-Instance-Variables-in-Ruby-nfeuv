# Direct Modification of Instance Variables in Ruby

This example highlights a common, yet subtle, error in Ruby: directly manipulating instance variables using `instance_variable_set` or `instance_variable_get`. While technically possible, this practice can lead to several issues:

- **Maintainability:** Modifying the internal state of an object without using defined methods makes the code harder to understand, maintain, and debug.  It breaks encapsulation.
- **Consistency:** If you have methods that rely on the instance variable's value, direct manipulation might bypass these methods and lead to unexpected behavior or inconsistencies. 
- **Debugging:** Tracking down errors becomes more complex when instance variables are altered outside of the object's methods.

The provided solution shows how to use accessor methods for consistent and predictable object manipulation.
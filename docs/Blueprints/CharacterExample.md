# Character Example

This is an example of a character blueprint, that uses the stamina system. The character blueprint is based on the default third person character blueprint. 

It is recommended to use the `Stamina Component` in the `Character` class, but it can be used in any class that inherits from `Actor`. 

However, the `Sprint Component` has to be on an actor that has both the `Stamina Component` and `Character Movement Component`. This is because it automatically detects these components on it's owning actor. 
# Predicate

Predicate is a functional interface that was introduced in java 8. It is is used to hold a condition. The method test can be used to test that condition.
It is present in the `java.util.function` package.

Example: -
```
Predicate<Integer> isEven = x -> x % 2 == 0;
if(isEven.test(4)) {
  System.out.println("Even");
}
```

The other methods that are available in Predicate are: -

1. and() Returns a composed predicate that represents the logical AND of two predicates
```
Predicate<String> startsWithZ = x -> x.toLowerCase().startsWith("z");
Predicate<String> endsWithN = x -> x.toLowerCase().endsWith("n");
if(startsWithZ.and(endsWithN).test("Zeeshan")){
 System.out.println("Zeeshan");
}
```
2. or() Returns a composed predicate that represents the logical OR of two predicates
```
if(startsWithZ.or(endsWithN).test("zees")){
  System.out.println("Starts with Z Or Ends with N");
}
```
3. negate() Returns a predicate that represents the logical negation of a predicate
```
if(startsWithZ.negate().test("eeshan")){
  System.out.println("Does not starts with Z");
}
```



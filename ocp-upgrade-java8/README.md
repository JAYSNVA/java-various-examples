ocp-upgrade-java8
-----------------

These are preparation materials for the Oracle's "Upgrade to Java SE 8 Programmer" exam \([1Z1-810](http://education.oracle.com/pls/web_prod-plq-dad/db_pages.getpage?page_id=5001&get_params=p_exam_id:1Z0-810)\).

### Exam topics:

#### 1. Lambda Expressions
- 1.1. [Describe Java inner classes and develop the code that uses Java inner classes (such as: nested class, static class, local class and anonymous classes)](http://docs.oracle.com/javase/tutorial/java/javaOO/nested.html): [InnerClassExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic1_1/InnerClassExample.java),   [StaticInnerClassExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic1_1/StaticInnerClassExample.java),     [AnonymousClassExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic1_1/AnonymousClassExample.java),     [LocalMethodClassExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic1_1/LocalMethodClassExample.java)
    
- 1.2. Define and write functional interfaces

  A _functional interface_ is an interface that specifies exactly one abstract method. The signature of the abstract method of a functional interface is called a function descriptor. @FunctionalInterface annotation is used to indicate that the interface is intended to be a functional interface.
  
  [FunctionalInterfaceExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic1_2/FunctionalInterfaceExample.java)
  
- 1.3. [Describe a Lambda expression;](http://en.wikipedia.org/wiki/Anonymous_function#Java) refactor the code that use anonymous inner class to use Lambda expression including [type inference](http://docs.oracle.com/javase/tutorial/java/generics/genTypeInference.html), [target typing](http://docs.oracle.com/javase/tutorial/java/javaOO/lambdaexpressions.html#target-typing):   [RefactoringCodeExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic1_3/RefactoringCodeExample.java),   [TypeInferenceExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic1_3/TypeInferenceExample.java)
      
#### 2. Using Built in Lambda Types
- 2.1. Describe the built in interfaces included in Java 8 – [java.util.function package](http://docs.oracle.com/javase/8/docs/api/java/util/function/package-summary.html)

|Functional interface|Function descriptor|Primitive specializations|
|:--------------------------|:------------------------|:------------------------|
|[Function\<T, R\>](http://docs.oracle.com/javase/8/docs/api/java/util/function/Function.html)|T -> R|IntFunction<R>, IntToDoubleFunction, IntToLongFunction, LongFunction<R>, LongToDoubleFunction, LongToIntFunction, DoubleFunction<R>, ToIntFunction<T>, ToDoubleFunction<T>, ToLongFunction<T>|
|[Consumer\<T\>](http://docs.oracle.com/javase/8/docs/api/java/util/function/Consumer.html)|T -> void|IntConsumer, LongConsumer, DoubleConsumer|
|[Supplier\<T\>](http://docs.oracle.com/javase/8/docs/api/java/util/function/Supplier.html)|() -> T|BooleanSupplier, IntSupplier, LongSupplier, DoubleSupplier|
|[UnaryOperator\<T\>](http://docs.oracle.com/javase/8/docs/api/java/util/function/UnaryOperator.html)|T -> T|IntUnaryOperator, LongUnaryOperator, DoubleUnaryOperator|
|[BinaryOperator\<T\>](http://docs.oracle.com/javase/8/docs/api/java/util/function/BinaryOperator.html)|(T, T) -> T|IntBinaryOperator, LongBinaryOperator, DoubleBinaryOperator|
|[Predicate\<T\>](http://docs.oracle.com/javase/8/docs/api/java/util/function/Predicate.html)|T -> boolean|IntPredicate, LongPredicate, DoublePredicate|
- 2.2. Develop code that uses [Function](http://docs.oracle.com/javase/8/docs/api/java/util/function/Function.html) interface: [FunctionInterfaceExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic2_2/FunctionInterfaceExample.java)
- 2.3. Develop code that uses [Consumer](http://docs.oracle.com/javase/8/docs/api/java/util/function/Consumer.html) interface: [ConsumerInterfaceExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic2_3/ConsumerInterfaceExample.java)
- 2.4. Develop code that uses [Supplier](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic2_4/SupplierInterfaceExample.java) interface: [SupplierInterfaceExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic2_4/SupplierInterfaceExample.java)
- 2.5. Develop code that uses [UnaryOperator](http://docs.oracle.com/javase/8/docs/api/java/util/function/UnaryOperator.html) and [BinaryOperator](http://docs.oracle.com/javase/8/docs/api/java/util/function/BinaryOperator.html) interfaces: [UnaryAndBinaryOperatorInterfacesExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic2_5/UnaryAndBinaryOperatorInterfacesExample.java)
- 2.6. Develop code that uses [Predicate](http://docs.oracle.com/javase/8/docs/api/java/util/function/Predicate.html) interface: [PredicateInterfaceExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic2_6/PredicateInterfaceExample.java)
- 2.7. Develop the code that use primitive and binary variations of base interfaces of java.util.function package: [PrimitiveAndBinaryVariationsExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic2_7/PrimitiveAndBinaryVariationsExample.java)
- 2.8. Develop the code that use method reference; including refactor the code that use Lambda expression to use method references: [MethodReferenceExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic2_8/MethodReferenceExample.java)

#### 3. Filtering Collections with Lambdas
- 3.1. Develop the code that iterates a collection by using forEach; including method chaining: [ForEachExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic3_1/ForEachExample.java)
- 3.2. Describe the [Stream](http://docs.oracle.com/javase/8/docs/api/java/util/stream/Stream.html) interface and [pipelines](http://docs.oracle.com/javase/tutorial/collections/streams/#pipelines): [StreamInterfaceExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic3_2/StreamInterfaceExample.java)
- 3.3. Filter a collection using lambda expressions: [FilterCollectionExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic3_3/FilterCollectionExample.java)
- 3.4. Identify lambda operations that are [lazy](http://docs.oracle.com/javase/tutorial/collections/streams/parallelism.html#laziness)

#### 4. Collection Operations with Lambda
- 4.1. Develop code to [extract data from an object using map](http://www.oracle.com/technetwork/articles/java/ma14-java-se-8-streams-2177646.html): [ExtractDataWithMapExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic4_1/ExtractDataWithMapExample.java)
- 4.2. [Search for data using search methods including: findFirst, findAny, anyMatch, allMatch, noneMatch](http://www.oracle.com/technetwork/articles/java/ma14-java-se-8-streams-2177646.html); [SearchDataExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic4_2/SearchDataExample.java)
- 4.3. Describe the unique characteristics of [Optional](http://docs.oracle.com/javase/8/docs/api/java/util/Optional.html), [OptionalInt](https://docs.oracle.com/javase/8/docs/api/java/util/OptionalInt.html), [OptionalLong](https://docs.oracle.com/javase/8/docs/api/java/util/OptionalLong.html), and [OptionalDouble](https://docs.oracle.com/javase/8/docs/api/java/util/OptionalDouble.html) classes: [OptionalExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic4_3/OptionalExample.java)
- 4.4. Perform calculations by using methods [count](http://docs.oracle.com/javase/8/docs/api/java/util/stream/Stream.html#count--), [max](http://docs.oracle.com/javase/8/docs/api/java/util/stream/Stream.html#max-java.util.Comparator-), [min](http://docs.oracle.com/javase/8/docs/api/java/util/stream/Stream.html#min-java.util.Comparator-), [average](http://docs.oracle.com/javase/8/docs/api/java/util/stream/IntStream.html#average--), and [sum](http://docs.oracle.com/javase/8/docs/api/java/util/stream/IntStream.html#sum--): [CalculationsExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic4_4/CalculationsExample.java)
- 4.5. [Sort a collection using lambda expressions](http://www.oracle.com/technetwork/articles/java/architect-lambdas-part2-2081439.html): [SortCollectionWithLambdas.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic4_5/SortCollectionWithLambdas.java)
- 4.6. Save results to a collection by using the collect method and [Collectors](http://docs.oracle.com/javase/8/docs/api/java/util/stream/Collectors.html) class; including methods such as averagingDouble, groupingBy, joining, partitioningBy: [CollectorsMethodsExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic4_6/CollectorsMethodsExample.java)

#### 5. Parallel Streams
- 5.1. [Develop the code that use parallel streams](http://docs.oracle.com/javase/tutorial/collections/streams/parallelism.html): [ParallelStreamExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic5_1/ParallelStreamExample.java)
- 5.2. Implement decomposition and reduction in paraller streams: [ReductionExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic5_2/ReductionExample.java)

#### 6. Lambda Cookbook
- 6.1. Develop the code that use Java SE 8 collection improvements: [Colleciton.removeIf](http://docs.oracle.com/javase/8/docs/api/java/util/Collection.html#removeIf-java.util.function.Predicate-), [List.replaceAll](http://docs.oracle.com/javase/8/docs/api/java/util/List.html#replaceAll-java.util.function.UnaryOperator-), [Map.computeIfAbsent](http://docs.oracle.com/javase/8/docs/api/java/util/Map.html#computeIfAbsent-K-java.util.function.Function-), [Map.computeIfPresent](http://docs.oracle.com/javase/8/docs/api/java/util/Map.html#computeIfPresent-K-java.util.function.BiFunction-), [Map.forEach](http://docs.oracle.com/javase/8/docs/api/java/util/Map.html#forEach-java.util.function.BiConsumer-): [CollectionImprovmentsExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic6_1/CollectionImprovementsExample.java)
- 6.2. Read files using lambda improvements in Files API including [find()](http://docs.oracle.com/javase/8/docs/api/java/nio/file/Files.html#find-java.nio.file.Path-int-java.util.function.BiPredicate-java.nio.file.FileVisitOption...-), [lines()](http://docs.oracle.com/javase/8/docs/api/java/nio/file/Files.html#find-java.nio.file.Path-int-java.util.function.BiPredicate-java.nio.file.FileVisitOption...-), and [walk()](http://docs.oracle.com/javase/8/docs/api/java/nio/file/Files.html#find-java.nio.file.Path-int-java.util.function.BiPredicate-java.nio.file.FileVisitOption...-) methods: [FilesApiImprovementsExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic6_2/FilesApiImprovementsExample.java)
- 6.3. Use [merge](http://docs.oracle.com/javase/8/docs/api/java/util/Map.html#merge-K-V-java.util.function.BiFunction-) and [flatMap](http://docs.oracle.com/javase/8/docs/api/java/util/stream/Stream.html#flatMap-java.util.function.Function-) methods on a collection: [MergeAndFlatMapExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic6_3/MergeAndFlatMapExample.java)
- 6.4. Describe other stream sources  [Arrays.stream()](http://docs.oracle.com/javase/8/docs/api/java/util/Arrays.html) and [IntStream.range()](http://docs.oracle.com/javase/8/docs/api/java/util/stream/IntStream.html#range-int-int-): [OtherStreamSourcesExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic6_4/OtherStreamSourcesExample.java)

#### 7. Method Enhancements
- 7.1. Adding [static methods](http://docs.oracle.com/javase/tutorial/java/IandI/defaultmethods.html) to interfaces: [StaticMethodsExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic7_1/StaticMethodsExample.java)
- 7.2. Define and use a [default method](http://docs.oracle.com/javase/tutorial/java/IandI/defaultmethods.html) of a interface and describe the inheritance rules for a default method: [DefaultMethodsExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic7_2/DefaultMethodsExample.java)

#### 8. Use Java SE 8 Date/Time API - 10%
- 8.1. [Create and manage date-based and time-based events](http://www.oracle.com/technetwork/articles/java/jf14-date-time-2125367.html); including combination of date and time into a single object using  LocalDate, LocalTime, LocalDateTime, Instant, Period, Duration: [CreateAndManageDateTimeExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic8_1/CreateAndManageDateTimeExample.java)
- 8.2. Work with dates and times across time-zones and manage changes resulting from daylight savings: [TimeZonesExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic8_2/TimeZonesExample.java)
- 8.3. Define and create timestamps, periods and durations; apply formatting to local and zoned dates and times: [DateTimeFormattingExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic8_3/DateTimeFormattingExample.java)

#### 9.JavaScript on Java with Nashorn
- 9.1. [Develop](http://www.oracle.com/technetwork/articles/java/jf14-nashorn-2126515.html) Javascript code that creates and uses Java members such as Java objects, methods, JavaBeans, Arrays, Collections, Interfaces: [JavasriptUsesJavaExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic9_1/JavascriptUsesJavaExample.java), [characters-list.js](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic9_1/characters-list.js)
- 9.2. [Develop](http://www.oracle.com/technetwork/articles/java/jf14-nashorn-2126515.html) code that  evaluates JavaScript in java, passes Java object to Javascript, invokes Javascript function and calls methods on Javascript objects: [JavaEvaluatesJavascriptExample.java](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic9_2/JavaEvaluatesJavascriptExample.java), [quebec-gst-tax-calculator.js](/ocp-upgrade-java8/src/main/java/com/kiroule/ocpupgradejava8/topic9_2/quebec-gst-tax-calculator.js)

#### Other resources:
- [Java 8 in Action](http://www.amazon.com/Java-Action-Lambdas-functional-style-programming/dp/1617291994/ref=pd_bxgy_b_img_y)

##### Futurama and Futurama characters are the trademarks of Twentieth Century Fox Film Corporation. 


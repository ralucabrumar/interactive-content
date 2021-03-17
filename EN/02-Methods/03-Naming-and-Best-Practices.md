# Naming and Best Practices

[slide hideTitle]
# Naming Methods

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Methods-And-Arrays/03.Java-Fundamentals-Methods/EN/interactive-java-fundamentals-methods-11-12-13-Naming-methods-and-parameters-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

Always use verbs when naming methods.

A method represents an action and its name should clearly state what it is.

Method names can be a single word or a mixture of words.

## Examples of Good Names

Method names should answer the question: *What does this method do?*

Good method names are **findStudent**, **getReportByName**, **getBrowserId**.


## Examples of Bad Method Names

If you cannot find a good name for a method, think about what its purpose is first.

Bad method names: **Method1**, **DoSomething**, **HandleStuff**, **SampleMethod**.

Perhaps your method does too many things making it difficult to decide on a name.

This should be an indicator that you should split its functions into two or more methods.

## Naming Method Parameters

Method parameter names should be composed of a \[Noun\] or an \[Adjective\] + \[Noun\]. 

Always use **camelCase**:

- **firstName**, **report**, **speedKmH**, **getListOfUsers**, **calculateFontSizeInPixels**


[/slide]

[slide hideTitle]
# Best Practices

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Methods-And-Arrays/03.Java-Fundamentals-Methods/EN/interactive-java-fundamentals-methods-14-Methods-Best-Practices-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

Each method should perform a **single**, well-defined task.

A method's name should **describe that task** in a precise and non-ambiguous way.

**Avoid** creating methods **that cannot fit on your screen**, split them into several shorter ones.

Here are some self-documenting method names:

```Java
public static void printReceipt() {
    printHeader();
    printBody();
    printFooter();
}
```

You can understand what each of the above methods does by reading their names, even without checking their implementation.

[/slide]

[slide hideTitle]
# Code Structure and Formatting

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Methods-And-Arrays/03.Java-Fundamentals-Methods/EN/interactive-java-fundamentals-methods-15-Code-Structure-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

Make sure to use correct **indentation**.

Leave a **blank line** in **method mbodies** - after **loops** and after **if** statements.

**Avoid long lines** and **complex expressions**.

```Java
public static void performAction() {
    // some code…
    // some more code…
}
```
[/slide]

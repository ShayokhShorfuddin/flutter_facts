# facts

A Flutter package that provides various types of facts and also allows you to filter only Safe or Unsafe facts.

## Screenshot

<img src="https://raw.githubusercontent.com/ShayokhShorfuddin/facts/master/fact.png" />


## How to use

### Functions

There are 2 functions that you can use to get facts. They are -

* ```getFact()```
* ```getFacts()```


```getFact()``` will give you 1 fact depending on the parameters you gave it. It may return Safe/ Unsafe/ Mixed.
```getFacts()``` will give you a "List" of facts depending on the parameters you gave it. It may return Safe/ Unsafe/ Mixed.

**NOTE**: If you are going to use ```getFacts```, make sure to pass the ```amount``` parameter to tell the package "How many facts do you wanna get in the List". Also, make sure that the ```amount``` you pass is "At least 1 or equal to the amount of available facts". For example - 

Suppose you did this..

```dart
Center(
  child: Column(
     mainAxisSize: MainAxisSize.min,
     children: [
        for (var item in Facts().getFacts(amount: 112, isNotSafe: true))
        Text(item)
     ]
   )
)
```
The code above will throw an error. As you did ```isNotSafe: true```, the package will get all the available "Unsafe" facts and then try to get random "112" Unsafe facts for you. But 112 Unsafe facts are not available yet. There are currently 108 Unsafe facts available. So, the minimum amount is 1 and maximum is the the amount of available facts. :]


### Available Facts

* **Safe Facts** : 6671
* **Unsafe Facts** : 108
* **Mixed Facts** : 6779

### Fact Types

You can get 3 types of facts from this package. 

* Safe facts
* Unsafe facts
* Mixed facts (Might be Safe or Unsafe. Its random.)

### Mixed Facts

If you want to get a mixed fact that can be `Safe or Unsafe`, simply do -

* ```Facts().getFact()  // For 1 mixed fact```
* ```Facts().getFacts(amount: 7) // For getting a list of mixed fact. Currently it will give you a List with 7 random mixed facts.```

**NOTE**: Make sure you don't pass `isSafe` or `isNotSafe` in order to get mixed fact. 


### Safe Facts

To get only Safe facts, do -

* ```Facts().getFact(isSafe: true)  // For 1 safe fact```
* ```Facts().getFacts(amount: 5, isSafe: true)  // For getting a list of safe fact. Currently it will give you a List with 5 random safe facts.```

**NOTE**: You can also get Safe facts using ```isNotSafe: false```. That's because both ```isSafe: true``` and ```isNotSafe: false``` indicate to Safe facts :]


### Unsafe Facts

To get only Unsafe facts, do -

* ```Facts().getFact(isNotSafe: true)  // For 1 unsafe fact```
* ```Facts().getFacts(amount: 5, isNotSafe: true)  // For getting a list of unsafe fact. Currently it will give you a List with 5 random unsafe facts.```

**NOTE**: You can also get Unsafe facts using ```isSafe: false```. That's because both ```isSafe: false``` and ```isNotSafe: true``` indicate to Unsafe facts.


## Usage

To use this package :

* add the dependency to your `pubspec.yaml` file.

```yaml
  dependencies:
    flutter:
      sdk: flutter
    facts:
```


# License
MIT License

Copyright (c) 2022 Shayokh Shuvro

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.


## Getting Started

For help getting started with Flutter, view our online [documentation](https://flutter.io/).

For help on editing package code, view the [documentation](https://flutter.io/developing-packages/).

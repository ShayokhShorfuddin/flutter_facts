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

**NOTE**: If you are going to use ```getfacts```, make sure to pass the ```amount``` parameter to tell the package "How many facts do you wanna get in the List". Also, make sure that the ```amount``` you pass is "At least 1 or equal to the amount of available facts". For example - 

Suppose you did this..

```dart
Center(
  child: Column(
     mainAxisSize: MainAxisSize.min,
     children: [
        for (var item in Facts().get_facts(amount: 112, isNotSafe: true))
        Text(item)
     ]
   )
)
```
The code above will throw an error. As you did ```isNotSafe: true```, the package will get all the available "Unsafe" facts and then try to get random "112" Unsafe facts for you. But 112 safe facts are not available yet. There are currently 108 Unsafe facts available. So, the minimum amount is 1 and maximum is the the amount of available facts. :]

Safe facts : 6671
UnSafe facts : 108
Mixed facts : 6779


### Available Facts

soon

### Fact Types

You can get 3 types of facts from this package. 

* Safe facts
* Unsafe facts
* Mixed facts (Might be Safe or Unsafe. Its random.)

### Mixed facts

If you want to get a mixed fact that can `Safe or Unsafe`

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

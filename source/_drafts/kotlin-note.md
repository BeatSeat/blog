---
title: Kotlin学习笔记
date: 2024-06-10 17:42:00
tags: kotlin language_notes
---
Kotlin虽然来自于Java，但是整体来讲现代很多，有点类似于现代C++、Golang这些，虽然是强类型但是有类型推断。
例如赋值语句如*var*(variable)和*val*(value)。 类型的话就和Java差不多。

在Kotlin中和Java一样有若干基本的Collection，我比较喜欢和C++一样叫容器，分别是List、Set和Map。Kotlin是一个引入了一些函数式风格的语言，所以默认下这些的构造都是Immutable的。
```
val immutableList = listOf("apple", "pear")

var mutableList : MutableList<String> = mutableListOf
```
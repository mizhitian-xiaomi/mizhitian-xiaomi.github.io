---
layout: post
title: ThinkinginJava-第二章练习
description: 练习记录及笔记
tags: Java
---

<hr>

### 练习5



```java

import static net.mindview.util.Print.print;

public class TestObject_5 {

    static void showMsg(Dog dog){
        print(dog.name+" is shouting "+dog.says);
    }

    public static void main(String[] args) {
        Dog spot  = new Dog();
        Dog ruff = new Dog();
        spot.name = "Spot";
        spot.says = "Ruff!";
        ruff.name = "scruffy";
        ruff.says = "Wurf!";
        showMsg(spot);
        showMsg(ruff);
    }
}
```

<br>

### 练习6

equals() 用于除基本类型外的对象

> 八大基本类型：
>
> char  /  boolean  /  byte  /  short  /  int  /  long  /  float  /  double

<br>

```Java

import static net.mindview.util.Print.print;

public class TestObject_6 {

    static void showMsg(Dog dog) {
        print(dog.name + " is shouting " + dog.says);
    }

    public static void main(String[] args) {
        Dog spot = new Dog();
        spot.name = "Spot";
        spot.says = "Ruff!";

        Dog doggy = new Dog();
        doggy = spot;

        print("------- == -------");
        print(doggy == spot);

        print("------- equals -------");
        print(doggy.equals(spot));
        
        print()
        showMsg(doggy);
        showMsg(spot);

    }
}

```

<br>

### 练习7

* **与或非**操作只能用于**布尔值**
* 如果在应用string类型的地方使用了布尔值，布尔值会自动转换成适当的文本形式

```Java

import java.util.Random;

public class ThrowCoins {

    public static void main(String[] args) {
        Random random = new Random();
        int coin = random.nextInt();
        if (coin % 2 == 1)
            System.out.println("HEAD");
        else
            System.out.println("FLOWER");
    }
}

```

<br>

### 练习8

* 16进制前缀 0x
* 8进制前缀 0

```java

public class LongValues {

    public static void main(String[] args) {
        long hexadecimal = 0xffff;
        long octal = 07777L;
        System.out.println(hexadecimal);
        System.out.println(octal);
        
        System.out.println("--------Long.toBinaryString()-------");
        System.out.println("hexadecimal = " + Long.toBinaryString(hexadecimal));
        System.out.println("otcal = " + Long.toBinaryString(octal));
    }
}

```

<br>

### 练习9

```java

import static net.mindview.util.Print.print;

public class MinMax {

    public static void main(String[] args) {
        print("--------Float--------");
        print("Min = " + Float.MIN_VALUE);
        print("Max = " + Float.MAX_VALUE);

        print("--------Double-------");
        print("Min = " + Double.MIN_VALUE);
        print("Max = " + Double.MAX_VALUE);

    }
}
```

<br>






```java

public class Test_i {

    static void compare(int n){
        System.out.println("----- Count:"+n+" -----");
        long t1 = System.currentTimeMillis();
        for (int i = 0; i < n; i++) {
//            System.out.println(i);
        }
        System.out.println("i++耗时: "+(System.currentTimeMillis()-t1));
        long t2 = System.currentTimeMillis();
        for (int i = 0; i < n; ++i) {
//            System.out.println(i);
        }
        System.out.println("++i耗时: "+(System.currentTimeMillis()-t2));
    }

    public static void main(String[] args) {
        compare(10);
        compare(10000);
        compare(Integer.MAX_VALUE);
    }

}

```



![1573008392452](C:%5CUsers%5Cmizhitian%5CDesktop%5C1573008392452.png)
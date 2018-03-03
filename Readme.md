### Java 设计模式


#### 单例模式 (DLC双锁检查机制，线程安全)
```java
public class Singleton {
    public static Singleton instance = null;

    public static Singleton getInstance() {
        if (instance == null) {
            synchronized (Singleton.class){
                if(instance==null){
                    instance=new Singleton();
                }
            }
        }
        return instance;

    }

    private Singleton() {
    }
}
```




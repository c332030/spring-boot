
# spring 环境配置

application-{profile}.yml

@Profile注解可以实现不同环境下配置参数的切换

自定义注解
```java
@Target({ElementType.TYPE, ElementType.METHOD})
@Retention(RetentionPolicy.RUNTIME)
@Profile("dev")
public @interface Dev {
// ...    
}
```

```java
@Configuration
@Profile("dev")
public class DevConfiguration {
    // ...
}
```

```java
@Configuration
@Profile("test")
public class TestConfiguration {
    // ...
}
```

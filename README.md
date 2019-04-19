构造器拷贝支持非静态内部类

## Getting Started
Check out the [Getting Started Guide](https://dozermapper.github.io/gitbook/documentation/gettingstarted.html), [Full User Guide](https://dozermapper.github.io/user-guide.pdf) or [GitBook](https://dozermapper.github.io/gitbook/) for advanced information.

## Getting the Distribution
If you are using Maven, simply copy-paste this dependency to your project.

```XML
<dependency>
    <groupId>com.github.dozermapper</groupId>
    <artifactId>dozer-core</artifactId>
    <version>6.4.1</version>
</dependency>
```

## Simple Example
```XML
<mapping>
  <class-a>yourpackage.SourceClassName</class-a>
  <class-b>yourpackage.DestinationClassName</class-b>
    <field>
      <a>yourSourceFieldName</a>
      <b>yourDestinationFieldName</b>
    </field>
</mapping>
```

```Java
SourceClassName sourceObject = new SourceClassName();
sourceObject.setYourSourceFieldName("Dozer");

Mapper mapper = DozerBeanMapperBuilder.buildDefault();
DestinationObject destObject = mapper.map(sourceObject, DestinationClassName.class);

assertTrue(destObject.getYourDestinationFieldName().equals(sourceObject.getYourSourceFieldName()));
```

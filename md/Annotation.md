# π’ μ΄λΈνμ΄μ(@Annotation)μ΄λ?
> μ¬μ μ  μλ―Έλ‘λ μ£Όμμ΄λΌλ λ»μ΄λ€. μλ°μμ μ¬μ©λ  λμ μ΄λΈνμ΄μμ μ½λ μ¬μ΄μ 
> μ£Όμμ²λΌ μ°μ¬μ νΉλ³ν μλ―Έ, κΈ°λ₯μ μννλλ‘ νλ κΈ°μ 

## `μ΄λΈνμ΄μ` μ μ©λ

> -μ»΄νμΌλ¬μκ² μ½λ μμ± **λ¬Έλ² μλ¬λ₯Ό μ²΄ν¬**νλλ‘ μ λ³΄λ₯Ό μ κ³΅ </br>
-μννΈμ¨μ΄ κ°λ°ν΄μ΄ **λΉλλ λ°°μΉμ μ½λλ₯Ό μλμΌλ‘ μμ±**ν  μ μλλ‘ μ λ³΄ μ κ³΅ </br>
-**μ€νμ(λ°νμμ)νΉμ  κΈ°λ₯μ μ€ν**νλλ‘ μ λ³΄λ₯Ό μ κ³΅ </br>

## `μ΄λΈνμ΄μ`μ μ¬μ©νλ μμ
> 1.μ΄λΈνμ΄μ(@***)μ μ μνλ€. <br/>
2.ν΄λμ€μ μ΄λΈνμ΄μμ λ°°μΉνλ€.  <br/>
3.μ½λκ° μ€νλλ μ€μ Reflectionμ μ΄μ©νμ¬ μΆκ° μ λ³΄λ₯Ό νλνμ¬ κΈ°λ₯μ μ€μνλ€.

## `μ΄λΈνμ΄μ`μ μ’λ₯
## π @Annotation
- μ¬μ μ  μλ―Έλ‘λ 'μ£Όμ', μλ°μ½λμ μ£Όμμ λ¬μ νΉλ³ν μλ―Έλ₯Ό λΆμ¬ν κ²
- μ¦, μλ°μ½λμ μ£Όμμ²λΌ λ¬μ νλ‘κ·Έλ¨μκ² μΆκ°μ μΈ μ λ³΄λ₯Ό μ κ³΅ν΄μ£Όλ
'λ©νλ°μ΄ν°' <br/>
μλ°λ μ€νλ§μ΄ μ κ³΅ν΄μ£Όλ κ²λ μκ³ , μ¬μ©μκ° μ§μ  λ§λ€ μλ μμ

### π @ComponentScan
- λΉμΌλ‘ λ±λ‘ λ  μ€λΉλ₯Ό λ§μΉ ν΄λμ€λ€μ μ€μΊνμ¬, λΉμΌλ‘ λ±λ‘ν΄μ£Όλ κ²
  λΉμΌλ‘ λ±λ‘ λ  μ€λΉλ₯Ό νλ κ²μ΄λ? <br/>
@Component, @Service, @Repository, @Controller, @Configurationμ΄ λΆμ λΉλ€μ μ°Ύμμ
Contextμ λΉμΌλ‘ λ±λ‘ λ  μ€λΉλ₯Ό ν κ² <br/>
= ν΄λΉ μ΄λΈνμ΄μμ΄ μμ±λ ν¨ν€μ§ μ΄νμ 
ν΄λμ€λ€μ μννλ©° λΉμΌλ‘ λ±λ‘λ  κ°μ²΄λ€μ νμ

#### π component-scan μ¬μ©λ°©λ²
- component-scan μ μ¬μ©νλ λ°©λ²μ
xml νμΌμ μ€μ νλ λ°©λ²κ³Ό μλ°νμΌ μμμ μ€μ νλ λ°©λ²μ΄ μλ€. <br/>

- AppCtx μ€μ  ν΄λμ€μ @ComponentScan μ΄λΈνμ΄μμ λΆμΈ μμ (μλ°νμΌ)
``` 
@Configuration
// @Component μ λΈνμ΄μμ λΆμΈ ν΄λμ€λ₯Ό μ€μΊν΄μ λΉμΌλ‘ λ±λ‘νλλ‘ νλ€.
// basePackages μμ±μ μ€μΊ λμ ν¨ν€μ§ λͺ©λ‘μ μ§μ νλ€. ν΄λΉ ν¨ν€μ§μ κ·Έ νμ ν¨ν€μ§μ μν ν΄λμ€λ₯Ό μ€μΊ λμμΌλ‘ μ€μ νλ€.
// μ€μΊ λμ μ€ @Component μ λΈνμ΄μμ΄ λΆμ ν΄λμ€μ κ°μ²΄λ₯Ό μμ±ν΄μ λΉμΌλ‘ λ±λ‘νλ€.
@ComponentScan(basePackages= {"spring"})
public class AppCtx {
  @Bean
  @Qualifier("example")
  public ExService exService(){
    return new ExService();
  }
  @Bean
  public SampleService sampleService(){
    return new SampleService ();
  }
}
```

### π @Component
- κ°λ°μκ° μ§μ  μμ±ν Classλ₯Ό BeanμΌλ‘ λ±λ‘νκΈ° μν μ΄λΈνμ΄μ

@ComponentScan μ μΈμ μν΄ νΉμ  ν¨ν€μ§ μμ ν΄λμ€λ€μ μλ μ€μΊνμ¬<br/>
@ComponentScan μ΄λΈνμ΄μμ΄ μλ ν΄λμ€λ€μ λνμ¬ λΉ μΈμ€ν΄μ€λ₯Ό μμ±νλ€.<br/>
@Component μ΄λΈνμ΄μμ Controller, Service, DAO μΈκ°μ§ μ΄μΈμ ν΄λμ€μλ§ μ¬μ© κΆμ₯
<br/>
@Component -> (κ΅¬μ²΄ν) -> @Controller, @Service, @Repository
<br/>

[ μ¬μ©ν  μ μλ μμΉ ] <br/>
μ€μ  μμΉ: ν΄λμ€ μ μΈλΆ μ
<context:component-scan> νκ·Έλ₯Ό μ€μ νμΌμ μΆκ°νλ©΄ ν΄λΉ μ΄λΈνμ΄μμ΄ μ μ©λ ν΄λμ€λ₯Ό λΉμΌλ‘ λ±λ‘νκ² λλ€. 
λ²μλ λν΄νΈλ‘ singletonμ΄λ©° @Scopeλ₯Ό μ¬μ©νμ¬ μ§μ ν  μ μλ€.
μ¬μ©νλ €λ©΄ XML μ€μ νμΌμ <context:component-scan>μ μ μνκ³  μ μ©ν  
κΈ°λ³Έ ν¨ν€μ§λ₯Ό base-package μμ±μΌλ‘ λ±λ‘νλ€.


### π @Bean
- κ°λ°μκ° μ§μ  μ μ΄κ° λΆκ°λ₯ν μΈλΆλΌμ΄λΈλ¬λ¦¬ λ±μ BeanμΌλ‘ λ±λ‘ν  λ μ¬μ©<br/>
- ex) ArrayListκ°μ λΌμ΄λΈλ¬λ¦¬ λ±μ BeanμΌλ‘ λ±λ‘νκΈ° μν΄μλ<br/>
λ³λλ‘ ν΄λΉ λΌμ΄λΈλ¬λ¦¬ κ°μ²΄λ₯Ό λ°ννλ Methodλ₯Ό λ§λ€κ³  @Beanμ μ¬μ©νλ©΄ λ¨<br/>
- ex)  DB μ°λμ μ¬μ©ν  DataSourceλ₯Ό μ€νλ§ λΉμΌλ‘ λ±λ‘ν ν, 
DB μ°λ κΈ°λ₯μ κ΅¬νν λΉ κ°μ²΄λ DataSourceλ₯Ό μ£Όμλ°μ μ¬μ©
- μλ°νμΌver
```  
@Configuration
public class DBSet {
    @Bean
    public DriverManagerDataSource getConnection() throws SQLException {
        DriverManagerDataSource driverManagerDataSource = new DriverManagerDataSource();
        driverManagerDataSource.setDriverClassName();
        driverManagerDataSource.setUrl();
        driverManagerDataSource.setUsername();
        driverManagerDataSource.setPassword();

        return driverManagerDataSource;
    }
} 
```
- xml ver
```  
<!-- mybatis setting -->
   <beans:bean name="dataSource"
      class="org.springframework.jdbc.datasource.DriverManagerDataSource">
      <beans:property name="driverClassName" value="oracle.jdbc.driver.OracleDriver" />
      <beans:property name="url"
         value="jdbc:oracle:thin:@localhost:1521:xe" />
      <beans:property name="username" value="hr" />
      <beans:property name="password" value="123456" />
   </beans:bean>
```


### π @Autowired
- νμν μμ‘΄ κ°μ²΄μ "νμ"μ ν΄λΉνλ λΉμ μ°Ύμ μ£Όμ

[ @Autowired ]
- required : κΈ°λ³Έκ° : true
(λͺ» μ°ΎμΌλ©΄ κ΅¬λ μ€ν¨ )

[ μ¬μ©ν  μ μλ μμΉ ]
- μμ±μ (μ€νλ§ 4.3λΆν°λ μλ΅ κ°λ₯) <br/>
- setter <br/>
- νλ <br/>

### π @Qualifier("alias")
- νΉμ ν κ°μ²΄λ₯Ό μ°ΎκΈ°μν μ΄λ¦μ μ§μ  <br/>
- ex) WebClinetλ₯Ό BeanμΌλ‘ λ±λ‘νλλ° μμ²­ν΄μΌ ν  urlμ΄ λ§μμ μ¬λ¬κ°μ WebClientλ₯Ό λ±λ‘νλ©΄μ λ¬Έμ κ° λ°μνμλ€.
λ¬Όλ‘  κ·Έλκ·Έλ μμ±ν΄μ μ°λ©΄λμ§λ§ ν¨μ¨μ μ΄μ§ λͺ»νλ€.<br/>
μ΄λ¬ν λ¬Έμ λ₯Ό ν΄κ²°νκΈ° μν΄μ μμ£Ό μ¬μ©νκ³  μ¬μ¬μ©μ΄ κ°λ₯νλ€λ©΄ 
@Quailiferλ₯Ό μ¬μ©νλ©΄ λλ€. <br/>

[μ¬μ©ν  μ μλ μμΉ ]
- @Autowired λ°λ‘ μλ μ°μΈλ€.(@Autowired μ΄λΈνμ΄μκ³Ό ν¨κ» μ¬μ©)
- @Autowiredμ λͺ©μ μμ λμΌ νμμ λΉκ°μ²΄κ° μ‘΄μ¬μ νΉμ λΉμ 
μ½μν  μ μκ² μ€μ νλ€. 
@Qualifier("mainBean")μ ννλ‘ @Autowiredμ κ°μ΄ μ¬μ©νλ©° 
ν΄λΉ <bean>νκ·Έμ <qualifire value="mainBean" /> 
νκ·Έλ₯Ό μ μΈν΄μ£Όμ΄μΌ νλ€. λ©μλμμ λκ°μ΄μμ νλΌλ―Έν°λ₯Ό μ¬μ©ν  κ²½μ°λ
νλΌλ―Έν° μμ μ μΈν΄μΌνλ€.

μ¬μ©νλ €λ©΄ λμΌνμμ λΉκ°μ²΄ μ€μ μμ <qualifier value="[aliasλͺ]" />λ₯Ό μΆκ°ν΄ μ€λ€.
```  
<bean id="user2" class="com.sp4.UserImpl"> 
    <property name="name" value="μ€νλ§"/> 
    <property name="age" value="20"/> 
    <property name="tel" value="000-0000-0000"/>
</bean> 
<bean id="userService1" class="com.sp4.UserService"/>
```
```  
public class UserService { 
    @Autowired 
    @Qualifier("user2") 
    private User user; 
    
    public String result() { 
        return user.getData(); 
    } 
}

```


### π @Required
- νμ νλ‘νΌν°μμ λͺμνλ κ²μΌλ‘ νμ νλ‘νΌν°λ₯Ό μ€μ νμ§ μμ κ²½μ° 
λΉ μμ±μ μμΈλ₯Ό λ°μμν΄ <br/>

[μ¬μ©ν  μ μλ μμΉ ]
- setter λ©μλ μ

```  
import org.springframework.beans.factory.annotation.Required 
public class TestBean { 
    @Required 
    private TestDao testDao; 
  
    public void setTestDao(TestDao testDao) { 
        this.testDao = testDao; 
    } 
}
```

```  
<bean class="org.springframework.beans.factory.annotation.RequiredAnnotationBeanpostProcessor"/> 
<bean name="testBean" class="han.test.TestBean"> 
    <property name="testDao" ref="testDao"/> 
    <!-- @Required μ΄λΈνμ΄μμ μ μ©νμμΌλ―λ‘ μ€μ νμ§ μμΌλ©΄ μμΈλ₯Ό λ°μμν¨λ€. --> 
</bean>
```
RequiredAnnotationBeanPostProcessor ν΄λμ€λ 
μ€νλ§ μ»¨νμ΄λμ λ±λ‘λ bean κ°μ²΄λ₯Ό μ‘°μ¬νμ¬
@Required μ΄λΈνμ΄μμΌλ‘ μ€μ λμ΄ μλ νλ‘νΌν°μ κ°μ΄ μ€μ λμ΄ μλμ§ 
κ²μ¬ <br/>
μ¬μ©νλ €λ©΄ <bean class="org.springframework.beans.factory.annotation.RequiredAnnotationBeanPostProcessor" /> 
ν΄λμ€λ₯Ό λΉμΌλ‘ λ±λ‘μμΌμ€μΌ ν¨

### π @Controller
(μ£Όμ©λ view λ¦¬ν΄)ν΄λμ€μ λ¦¬ν΄νμμ΄ Stringμ΄λ©΄ λ¦¬ν΄κ°μ΄ jspνμΌλͺμ μλ―Έ <br/>
-> @Controllerμ κ²½μ° λ©μλμ @ResponseBodyλ₯Ό μ¬μ©νμ¬ κ°μ²΄λ₯Ό λ¦¬ν΄ν  μ μμ<br/>
<table>
@Controllerμ μ€ν νλ¦
<tr>
Client -> Request -> Dispatcher Servlet -> Handler Mapping 
-> Controller -> View -> Dispatcher Servlet -> Response -> Client
</tr>
@ResponseBodyμ μ€ν νλ¦
<tr>
Client -> Request -> Dispatcher Servlet -> Handler Mapping -> Controller (ResponseBody) -> Response -> Client
</tr>
</table>

### π @RestController
- **(@Controller + @ResponseBody)** κ²°ν© ννμ μ΄λΈνμ΄μμΌλ‘, <br/>
μ£Ό μ©λλ ν΄λΉ ν΄λμ€κ° ajax μμ²­μ λ°μ Json/Xml ννλ‘ κ°μ²΄ 
λ°μ΄ν°λ₯Ό λ°ν
- (μ£Όμ©λ λ°μ΄ν° λ¦¬ν΄)ν΄λμ€μ λ¦¬ν΄νμμ΄ Stringμ΄λ©΄ λ¬Έμμ΄ λ°μ΄ν° μλ―Έ(jspνμΌ μ¬μ© X)
<table>
@RestControllerμ μ€ν νλ¦
<tr>
Client -> HTTP Request -> Dispatcher Servlet -> Handler Mapping 
-> RestController (μλ ResponseBody μΆκ°)-> HTTP Response -> Client
</tr>
</table>

### π @ResponseBody
- μλ° κ°μ²΄λ₯Ό HTTP μμ²­μ body λ΄μ©μΌλ‘ λ³ν/λ§€ννλ μ΄λΈνμ΄μ

### π @RequestBody
- HTTP μμ²­μ body λ΄μ©μ μ λ¬λ°μ μλ° κ°μ²΄λ‘ λ³ν/λ§€ννλ μ΄λΈνμ΄μ
  (POST/PUT)

### π @Service
- @Serviceλ κ³μΈ΅ κ΅¬μ‘°μ μ£Όλ‘ λΉμ¦λμ€ μμ­μ λ΄λΉνλ κ°μ²΄μμ νμνκΈ° μν΄ μ¬μ©<br/>
  @Service, @Repository, @Controllerλͺ¨λ @Componentμ μ­ν μ μν(μ¦ iocμ»¨νμ΄λμ beanκ°μ²΄λ₯Ό μμ±ν΄μ£Όλ μ­ν ) νμ§λ§ κ° μ΄λΈνμ΄μλ§λ€ νΉνλ κ³μΈ΅μ΄ λ€λ₯΄λ€.

### π @Repository
- DAOλ₯Ό μΈμμμΌμ£ΌκΈ° μν μ€μ 
- ν΄λΉ ν΄λμ€κ° DAOλΌλ κ²μ μλ¦¬κΈ° μν΄μ @RepositoryλΌκ³  κΈ°μ¬<br/>
  @Service, @Repository, @Controllerλͺ¨λ @Componentμ μ­ν μ μν(μ¦ iocμ»¨νμ΄λμ beanκ°μ²΄λ₯Ό μμ±ν΄μ£Όλ μ­ν ) νμ§λ§ κ° μ΄λΈνμ΄μλ§λ€ νΉνλ κ³μΈ΅μ΄ λ€λ₯΄λ€.

### π @RequestMapping
- νΉμ  uriλ‘ μμ²­μ λ³΄λ΄λ©΄ Controllerμμ μ΄λ ν λ°©μμΌλ‘ μ²λ¦¬ν μ§ μ μ ν¨. 
- μ΄λ λ€μ΄μ¨ μμ²­μ νΉμ  λ©μλμ λ§€ννκΈ° μν΄ μ¬μ©νλ κ²
- @RequestMappingμμ κ°μ₯ λ§μ΄μ¬μ©νλ λΆλΆμ valueμ methodμ΄λ€.
  - valueλ μμ²­λ°μ urlμ μ€μ νκ² λλ€. 
  - methodλ μ΄λ€ μμ²­μΌλ‘ λ°μμ§ μ μνκ² λλ€.(GET, POST, PUT, DELETE λ±)
```  
@RestController
public class HelloController {

    @RequestMapping(value = "/hello", method = RequestMethod.GET)
    public String helloGet(...) {
        ...
    }

    @RequestMapping(value = "/hello", method = RequestMethod.POST)
    public String helloPost(...) {
        ...
    }

    @RequestMapping(value = "/hello", method = RequestMethod.PUT)
    public String helloPut(...) {
        ...
    }

    @RequestMapping(value = "/hello", method = RequestMethod.DELETE)
    public String helloDelete(...) {
        ...
    }
}
```
μ½λλ₯Ό κ°κ²°νκ² νκΈ° μν΄μλ
```  
@RestController
@RequestMapping(value = "/hello")
public class HelloController {

    @GetMapping()
    public String helloGet(...) {
        ...
    }

    @PostMapping()
    public String helloPost(...) {
        ...
    }

    @PutMapping()
    public String helloPut(...) {
        ...
    }

    @DeleteMapping()
    public String helloDelete(...) {
        ...
    }
}
```
κ³΅ν΅μ μΈ urlμ classμ @RequestMappingμΌλ‘ μ€μ μ ν΄μ£Όμλ€.
κ·Έλ¦¬κ³  @GetMapping, @PostMapping, @PutMapping, @DeleteMappingμΌλ‘ 
κ°λ¨νκ² μλ΅μ΄ κ°λ₯νλ€. <br/>
λ€μ μΆκ°μ μΌλ‘ urlμ λΆμ΄κ³  μΆλ€λ©΄ 
@GetMapping, @PostMapping, @PutMapping, @DeleteMapping μ 
μΆκ°μ μΈ urlμ μμ±νλ©΄ λλ€.
```  
@RestController
@RequestMapping(value = "/hello")
public class HelloController {    
    @GetMapping("/hi")
    public String helloGetHi(...) {
        ...
    }
}
```
μμ μλ helloGetHiμ λ€μ΄κ°κΈ° μν΄μλ /hello/hiλ‘ λ€μ΄κ°μΌ νλ€.
μΆκ°μ μΈ λ΄μ©μΌλ‘ @RequestMappingμ Classμ Methodμ λΆμΌ μ μκ³  
@GetMapping, @PostMapping, @PutMapping, @DeleteMappingλ€μ 
Methodμλ§ λΆμΌ μ μλ€.

### π @ModelAttribute
- ν΄λΌμ΄μΈνΈκ° μ μ‘νλ μ¬λ¬κ°μ νλΌλ―Έν°λ€μ **1:1λ‘ κ°μ²΄μ λ°μΈλ©** νμ¬ λ€μ Viewλ‘ λκ²¨μ μΆλ ₯νκΈ° μν΄ μ¬μ©λλ Object<br/>
λ§€νμν€λ νλΌλ―Έν°μ νμμ΄ κ°μ²΄μ **typeκ³Ό μΌμΉνλμ§**λ₯Ό ν¬ν¨ν λ€μν κ²μ¦μ§ν <br/>
ex) κ²μλ¬Ό λ²νΈλ₯Ό μ μ₯νλ intν index λ³μμ "1"μ΄λΌλ String κ°μ λ£μΌλ©΄ BindException λ°μ 
- @RequestBodyμ κ²½μ° Jsonμ΄λ XMLμ Jacksonκ³Ό κ°μ MessageConverterλ₯Ό μ¬μ©νλ©΄ λ³ννμ§λ§,
μ΄ μ΄λΈνμ΄μμ μ¬λ¬ κ°μ νλΌλ―Έν°λ₯Ό λ°λ‘ java bean κ°μ²΄λ‘ mapping μν΄
μ¦, JSPμμ form νκ·Έλ₯Ό ν΅νμ¬ μ λ¬λ°μ νλΌλ―Έν°λ€μ κ°μ²΄λ‘ λ°μΈλ© μν€λ κ²½μ°μ μ¬μ©κ°λ₯

π  @ModelAttributeμ @RequestBodyμ μ°¨μ΄μ 
@ModelAttributeλ λ°μΈλ© μν€λ μ΄λ€ λ°μ΄ν°λ₯Ό set ν΄μ£Όλ Setter ν¨μκ° μλ€λ©΄ λ§€νμ΄ λμ§ μλλ€.
νμ§λ§ @RequestBodyλ μμ²­λ°μ λ°μ΄ν°λ₯Ό λ³νμν€λ κ²μ΄κΈ° λλ¬Έμ, Setter ν¨μκ° μμ΄λ λ§€νμ΄λλ€.

### π @RequestParam
- μμ²­ νλΌλ―Έν°λ₯Ό λ©μλμμ 1:1λ‘ λ°κΈ° μν΄ μ¬μ©<br/>
@RequestParamμ μ¬μ©νλ©΄ κΈ°λ³Έμ μΌλ‘ λ°λμ ν΄λΉ νλΌλ―Έν°κ° μ μ‘λμ΄μΌ ν¨
- μ¬μ©μκ° μνλ λ§€κ°λ³μμ mapping νκΈ° μν΄μ μ¬μ©

### π @Data
- @Getter, @Setter, @RequiredArgsConstructor, @ToString, @EqualsAndHashCodeμ νκΊΌλ²μ μ€μ κ°λ₯
- λͺ¨λ  νλλ₯Ό λμμΌλ‘ μ κ·Όμμ μ€μ μκ° μλμΌλ‘ μμ±
1. @Getter @Setter <br/>
ex)
```  
@Getter @Setter
private String name;
```

2. @RequiredArgsConstructor (μμ±μ μλ μμ±)  <br/>
- @NoArgsConstructor: νλΌλ―Έν°κ° μλ κΈ°λ³Έ μμ±μλ₯Ό μμ± <br/> 
- @AllArgsConstructor: λͺ¨λ  νλ κ°μ νλΌλ―Έν°λ‘ λ°λ μμ±μ μμ± <br/>
- @RequiredArgsConstructor: finalμ΄λ @NonNullμΈ νλ κ°λ§ νλΌλ―Έν°λ‘ λ°λ μμ±μ μμ±<br/>

ex)
```  
@NoArgsConstructor
@RequiredArgsConstructor
@AllArgsConstructor
public class User {
  private Long id;
  @NonNull
  private String username;
  @NonNull
  private String password;
  private int[] scores;
}
```
κ²°κ³Ό
```  
User user1 = new User(); //@NoArgs
User user2 = new User("dale", "1234"); //@Required
User user3 = new User(1L, "dale", "1234", null); //@AllArgs
```

3. @ToString
- @ToStringμ ν΄λμ€μ λΆμ¬μ£Όλ©΄ toString() μλμΌλ‘ μμ±
- exclude μμ±μ μ¬μ©νλ©΄, νΉμ  νλλ₯Ό toString() κ²°κ³Όμμ μ μΈμν¬ μλ μμ

ex)
```  
@ToString(exclude = "password")
public class User {
  private Long id;
  private String username;
  private String password; //passwordλ string μ μ© μ λ¨
  private int[] scores;
}
```

νλ μν
```  
User user = new User();
user.setId(1L);
user.setUsername("dale");
user.setPassword(1234);
user.setScores(new int[]{80, 70, 100});
System.out.println(user);
```

κ²°κ³Ό
```  
User(id=1, username=dale, password=1234, scores=[80, 70, 100])
```

# 工厂模式

```java
 public class ReadFactory {
     public <E> JcsvReader<E> csvBuild (final Class<E> classE){
         JcsvReader<E> reader =new JcsvReader<>();
         //you can set reader class need propertys.
         //reader.setEnterclz("classE");
         return reader;
     }
     
      public <E> poiReader<E> poiBuild (final Class<E> classE){
         poiReader<E> reader =new poiReader<>();
         //you can set reader class need propertys.
         //reader.setEnterclz("classE");
         return reader;
     }

 }

 public class JcsvReader<E> {
     @Setter
     private Class<E> enterClz;
     
     //no args constructor method
     public JcsvReader(){ 
     }
     
     //do you real process
     public void read(){
         //csv read
     }
 }

 public class poiReader<E> {
     @Setter
     private Class<E> enterClz;
     
     //no args constructor method
     public poiReader(){ 
     }
     
     //do you real process
     public void read(){
         //poi read
     }
 }

```



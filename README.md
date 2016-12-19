# AutoMapped
配對有相同Property Name的二個模型



#Model A
```ruby
public class AModel{

  public int id {get;set;}
  
  public string Name {get;set;}

  public int age {get;set;}

}


```


#Model B
```ruby
public class BModel
{
  
  public int id {get;set;}
  
  public string Name {get;set;}
 
}


```

#Mapper
```ruby
  var b = new BModel();
  
  b.id = 10;
  
  b.Name = "John";

  b.Age = 30;
  
  var newModel = new AutoMapped().Mapper<AModel>(b);
 
```

#結果
```ruby
	結果會回傳 AMode
 

	因為AModel 跟傳入的 BModel 模型都有相同名稱的Property
  
	就會賦值
  
	newModel.id == 10;

	newModel.Name == 'John'
  
	newModel.Age = null //因為BModel沒有這個Property
```


  
 

# AutoMapped
�t�靈�ۦPProperty Name���G�Ӽҫ�



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

#���G
```ruby
	���G�|�^�� AMode
 

	�]��AModel ��ǤJ�� BModel �ҫ������ۦP�W�٪�Property
  
	�N�|���
  
	newModel.id == 10;

	newModel.Name == 'John'
  
	newModel.Age = null //�]��BModel�S���o��Property
```


  
 

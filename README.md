# AutoMapped
�t�靈�ۦPProperty Name���G�Ӽҫ�



using AIEZ;

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
  
  var newModel = AutoMapper.Mapper<AModel>(b);
 
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



#MapperList
```ruby
   var c = new List<BClass>();
   c.Add(new BClass { Address = "aa", Age = 10, id = 1, Name = "Hello" });
   c.Add(new BClass { Address = "cc", Age = 15, id = 2, Name = "World" }); 
   var newModel = AutoMapper.MapperList<AModel>(b);
 
```

#���G
```ruby
�^�� �@�ӷs��List
```

#Ignores
```ruby
   �ҥ~�ѼơA�ư����Q�i���ഫ���ѼơA�åH�r���j�}
   var newModel = AutoMapper.Mapper<AModel>(b,"ID,Name");
 
```
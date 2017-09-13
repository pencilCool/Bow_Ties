# Bow_Ties

## how to create subclass of  NSManagedObject 

- uicolor init 
- uiimage save 
- 设置数据范围
- 图片数据类型
- transformable


## 错误处理

```
   do {
      try managedContext.save()
      populate(bowtie: currentBowtie)
    } catch let error as NSError {
      print("Could not fetch \(error), \(error.userInfo)")
    }
    
```    

## 保存数据

```
   let entity = NSEntityDescription.entity(forEntityName: "Bowtie", in: managedContext)!
   let bowite = Bowtie(entity: entity, insertInto: managedContext)

   bowite.name = btDict["name"] as? String

   try! managedContext.save()

```

Data 和 NSData 桥接了直接用  

<h1 align="center">[ 对象映射器 ] Mapster</h1>
<p align="center">
</p><br/><br/><br/>



>[!WARNING|style: flat|label: 简要说明 ]
>
>- (`Mapperly`) 是一个高性能对象映射(`Object Mapping`)
>
>  <span style='color:red'>[ 它通过源生成器`Source Generator`在编译时自动生成类型之间的映射代码，避免了运行时的反射开销，从而提升了性能和类型安全性 ]</span>
>
>  [<span style='color:#008B00'>[👓 GitHub - Riok.Mapperly ]</span>](https://github.com/riok/mapperly ':target=_blank') [<span style='color:#008B00'>[👓 官方文档 ]</span>](https://mapperly.riok.app/docs/intro/ ':target=_blank')
>
><br/>

```csharp
# [ 源类型 ]
public class T1(string Description);
public record class T2(int Id, string Name);
public enum CarColor { Black = 1, Blue = 2, White = 3 }

public class T1Class
{
     public string Name { get; set; } = string.Empty;
     public int Age { get; set; }
     public CarColor Color { get; set; }
     public T1? T1 { get; set; }
     public List<T2> T2s { get; } = [];
}
    
# [ 目标类型 ]
public class T1Dto(string Description);
public record class T2Dto(int Id, string Name);
public enum CarColorDto { Black = 1, Blue = 2, White = 3 }

public class T3ClassDto
{
     public string Name { get; set; } = string.Empty;
     public int Age { get; set; }
     public CarColor Color { get; set; }
     public T1? T1 { get; set; }
     public List<T2> T2s { get; } = [];
}


```

```csharp
# [ 类型映射器 ]
[Mapper]
public static partial class MapperConfiguration
{

     public static partial T3ClassDto Map(T3Class @class);
}


```



>```csharp
>T3Class t3Class = new()
>{
>     Name = "Test",
>     Age = 30,
>     Color = CarColor.Blue,
>     T1 = new("Description"),
>     T2s = [new(1, "Name1"), new(2, "Name2")]
>};
>
>T3ClassDto t3ClassDto = MapperConfiguration.Map(t3Class);
>Console.WriteLine($"Name: {t3ClassDto.Name}, Age: {t3ClassDto.Age}, Color: {t3ClassDto.Color}");
>
>```
>
>
>
>

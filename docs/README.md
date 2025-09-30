<h1 align="center">[ 对象映射器 ] Mapster</h1>
<p align="center">
</p><br/><br/><br/>



>[!WARNING|style: flat|label: 简要说明 ]
>
>- (`Mapperly`) 是一个高性能对象映射(`Object Mapping`)
>
>   <span style='color:red'>[ 它通过源生成器`Source Generator`在编译时自动生成类型之间的映射代码，避免了运行时的反射开销，从而提升了性能和类型安全性 ]</span>
>
>   [<span style='color:#008B00'>[👓 GitHub - Riok.Mapperly ]</span>](https://github.com/riok/mapperly ':target=_blank') [<span style='color:#008B00'>[👓 官方文档 ]</span>](https://mapperly.riok.app/docs/intro/ ':target=_blank')
>
>
><br/>
>
><span style='color:Blue'>[`Mapperly`在创建目标`target`对象时，遵循以下原则，自动选则目标类型的构造函数 ]：</span>
>
>- <span style='color:red'>[`A`] 优先使用标记`[MapperConstructor]`的构造函数</span>
>
>- [`B.1`] 配置`PreferParameterlessConstructors = true`<span style='color:Blue'>[ 系统默认 ]</span>
>
>   <span style='color:red'>优先使用 [ 默认构造函数 ]</span>
>
>   <span style='color:red'>如果没有无参构造函数，则查找所有可访问的构造函数 [ 优先选择参数最多 + 且能全部映射的构造函数 ]</span>
>
>- [`B.2`] 配置`PreferParameterlessConstructors = false`<span style='color:red'>[ 跟`B`相反，最后考虑默认构造函数 ]</span>
>
>⚠ <span style='color:red'>[ 框架依然会对：目标类型中未通过构造函数参数赋值的 - 可写属性进行赋值 ]</span>
>
><br/>


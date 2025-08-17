<h1 align="center">C#</h1>
<p align="center">基础语法, 经验总结</p>
<p align="center">
<img src="https://img.shields.io/badge/version-v1.0.0-brightgre?style=plastic" title="文档版本" />
<img src="https://img.shields.io/badge/Internet-v11+-orange?style=plastic&labelColor=0076D6&logo=Internet-Explorer" title="IE" />
<img src="https://img.shields.io/badge/Microsoft%20Edge-0076D6?style=plastic&logo=Internet-Explorer" title="Microsoft Edge" />
<img src="https://img.shields.io/badge/Google-0076D6?style=plastic&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAACvklEQVQ4T42TeUjTYRjHv+/Puc2Wu8wj7zIxh61DZaWBdBDuj1qaJeERSZL1RzJISMygtBChCVkI0vGHmBYhSIKZurRDLQ2TTbJmHuGm5oW62nTHLzbbllLR89f7XJ/34X2+L8Eam664ec5iMJ5ZHvsaZhod5tEWC9x4/CWGQDjh7u1b7lNQrCAA7WgjjgOt0bC+1T1U6t+0xa2F/u67BwYNc7mcaH5JxZwtbgfQCrnH+DxDZ+jt4f+r2ZFjBm/SBy4zhKSy0mQHmGamSsdys/OsC/P/02+v4ezZq/TLLzpAbqueJoXxAp7E9Y9R0xVl9iRbtA38YyfBjhCB8uT+DWoGICZn2++o+mZGol4euYGJ3GxQbA/4l9xC7TsazSozTBYaKRImZNEE+CQHvqtdQH78B5JQn68fWpjkFEanIsPiCxCCuvlI1HSYVt1cIGNhd8gkoE53xVkBiySy9jytNxnBYbDRlVwKHpMDeZURg5PWVYBwPwqKdDbQnw4s6VZyDK6ViB9dsMwt6ymbfypiP4pi05BzzwDtnHPV9todIRSKjrOAvqOAZXEF4O5tJtKGq9PquVEvm08RgtbDxWh6K0Rjn+2NVowiwPUTbERxO4Evha7J1ou1JFNZ1v1Cq4pxREM9fVCz7woev3bD+xEzAgQU0uKZEAdTwEAO8OOzCyBIaCbyjruJdUOdjVbaNXKM9xZkbT2IWJ9w+Hr80tbsc2CkxNVMrQN8knbZhZTRqmhr06kT/rRwkSAIz6SXgP4Mm+JcJb6pD0hgTpYdcKjpIodDC7U9U4O8tZD6xALsXG4HJqpcKS+pDiF5gYQQ2vmZNLSGpXjVomwY7XZ+JlmoBOWSZECdBtAmgCEA/DOrsUF2mhBiF4oT4MDfH2hJ6Z0Zyu8aHxDVSy8bNs5Ws2DU6uGx+SN4268RT4ny9yl/Aofh87ClWli7AAAAAElFTkSuQmCC" title="Google" />
<img src="https://img.shields.io/badge/Firefox-0076D6?style=plastic&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAADMElEQVQ4T22Ta2gUVxTH/3ceO7vZPCYGQ5P4mk3ERKVgtNhGqG801CpEYygi1KaWRqpJRKIfCi0iWqz4wAcaUXwkNYKk2gqK4iMWRBSsWaGxNtmspJtk1+gk2c3Mzs7MvWUHdvHRy/1yzj3/3znn3nMJ3llyw7Upk3KFnZbNloRHjYLksZwhBnmO3IrE6K7hg5XBNyUkaahfTpHlLEGfk3/820gssU8zmUA4HiDJTcAYA7USqM+5A0U2/6jsaqsZ3zw0kNQ6gL5vSn48m7ly6QEsruBEF3Z4ziFqe3HMXJNORuMGsvQIWqdegs25X5ZqzxvHf/+01QE82TgrIJimMpbhQaakwVfcg+K+dljElQbYr1XY0Sh+n/0ryhUNar8VZoEehTCA+Dd+SMdxmhPMiRYyC4Zxs7sCL203fijcBGbbAKUgoohZtAvtFVcAaiH+fGQnObut9qdF0Y7tqVScYCFXUfGaVqFjSEQjtxbmQBhM1yAUFTlN/12+DxmSimAo7x/S3rA6/JHemZ8CCO4E8ktD+Dm0FfutZWCUwh6Ngo6MOpXUTu5C04w/kSd2ozukWOTiljV6hfHEnQQkxVL2GNroEpyhnyHICh2R2fsifRdNvoeonxuANNYJf3AaI/c2fWopdj/v9O82oA9n4MLEBThqVYGCR7HVj25LRuLfQefJDs+8jeqyLkgxP+7+9QkjLfVfqPPjj2QnBaOglINH1qHlcbB0EV4tjgvSYuyO1cAaDKNv2V64zX7wJIZzjz43yaEttdeqjI7lqRoZBUyDR4STYVOC0zmVuOqdB5pIYMXIbzha+gskrwZTd+HrZ9sekj11X/mq6f0eCdZbQ90pKGiWVuCBawa8TMe62A3UeK6j5IMQpBwdj5+V4YVatMoZpJbvqp7ON/0z3/0XaZswSFk6sgpUiG4DiZgbp3pWhjafaJvgANjmEukGU15NN3u9/wcRPAayC1VEB2QQArRoC6Nbj5/PIQBzAA6kGnxz4Xr/8viD6RzYe5xX1IObxjT4suO9q49c9aUC0oCUo6mu7mPFFT9ZmgiUTaKDfITLZb1CkW3wngC02PYNzZcvv0n/D7WEXciKJwIhAAAAAElFTkSuQmCC" title="Firefox" />
<img src="https://img.shields.io/badge/360-0076D6?style=plastic&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAACtUlEQVQ4T4WTW0iTYRjH/++3TeeWiYd0HvMws2JZmhA6MDNP4FXeCZLrohNEmKXMAv0gxUq6iMAg6UBCCel0F3UhLKtZIuU0naZmOjPnKd3WTu34hYM+JBX/d+/z/v+/53l4eQm2EMMwXADJACQA4j0ez3SntpnRel/7MYw3liLop9O61SBgyP95u91+ws3982LS1BehNbyDh3HD6FiEybWC/fwcq93ovKsL6NVQoKLptO5mFkDTNFVTU9PYb1BUqfRPNoHXGwm4QciNLPdYtMI2VWB9e32Gqos12my2a6pfLU1jxl44PFZf5+2UIyrD/Jy+s+yYvMQHWFtbk0x5egctLgN31jICnWUYfI4QmeElEAWI8dP6Ff0rSji9dpaZGyFzcnV7c3wAs/X3w3Hb+7M/LFoMG96AgMLFAw8Qzo9nA3PWMTyavMKeEwPTUBxcdZ/QNM2VX6/+1LfaceTtQqvPIN6dgbKkhk0btExcxrxtgq1fSnk8RRQKRWhusXT53qiM8sKz7d5bXcjETSBKpTLCJhlcHDd9ZD2BvBCE+EfvCMsVyUDk6rxEfyH1faM7JSgTpYn0jgCz2TxFagcL6oRUULU/RyAwOBd8IS7hoTz5DmKFB1mIi3Hg5XQDHF6brxYpSEY671QzqdPkv9rDTZg5Hlt6oX2mkfMvwSE85EWdQaRADLNrFSr9UxidSyzwdNIt6+yAUUpqB/KHKZCKq/s6stTGZzfX33snFUWfRwIjPScSiVpIraagCwSdlDKrVS6XN/WuPq9UL7VtyfCjAnAyqtwbaT96Oy4u7gYhhCF1A4ViEKaRIdBQXowcEhSlpgqLKo386VC9/RtMzmXs4gUjzD8Gh0MKdV/6Ryuys7PZMbf8ND09PfywsLB0iUQS43a7E4aGhpwOh+OzVCr9QAjxbhzvL+lJFkzfHSclAAAAAElFTkSuQmCC" title="360" />
</p><br/><br/><br/>


>[!WARNING|style: flat|label: 编程规范]
>
>- [`命名空间 | 类型`]名称单词的<span style='color:red'>[ 首字母大写 & 接口首字母以`I`开头 ]</span>
>- [`常量`]单词的<span style='color:Blue'>[ 首字母大写 ]</span>
>- [`私有字段`] 前缀<span style='color:Blue'>[ _下划线开头 + 小写字母 ]</span>
>- [`属性名称`]单词的<span style='color:Blue'>[ 首字母大写 ]</span>
>- [`方法名称`]单词的<span style='color:Blue'>[ 首字母大写 ]</span>
>
>---
>
>在实际[`Review`]代码过程中，可以根据<span style='color:red'>[ 自身的经验，从各个角度提出优化的意见 ]</span>一般需要重点着重
>
>- 你看不懂或疑惑的地方
>
>- 打破你常规的地方
>
>- 复杂的地方
>
><br/>



>[!WARNING|style: flat|label: 代码可读性]
>
><span style='color:red'>[ 代码是写给人看的 - 没有不需要维护的代码 ]</span>无论是`Author`自己后续维护代码，还是他人接手代码<span style='color:red'>[ 是否能快速地理解代码逻辑 ]</span>
>
>- 变量、方法的[`命名是否合适`]是否[ 真实反映了他们的目的 ]
>
>- 实现的逻辑[`是否已有现成的库可以替代`]尽量不要自己去实现<span style='color:Red'>( 因为可能会引入不必要的`BUG`)</span>
>
>- <span style='color:red'>[ 关于注释 ]</span>代码注释不求多<span style='color:red'>[ 而在于有效 ]</span>
>
>---
>
>- <span style='color:red'>[ 不好理解的地方 ]</span>要有恰当的注释，代码中如果有[`特殊处理、特殊的常量、或者不符合一般用法的逻辑`]需要特别注释说明一下
>
>- <span style='color:red'>[ 代码的组织 ]</span>良好的代码应该有<span style='color:red'>[ 较好的封装 & 模式设计 ]</span>使得代码看起来[`清晰明了`]
>
>```csharp
>/// <summary>
>/// [ 创 建 人 ] 桑云龙
>/// [ 创建日期 ] 2020-01-01
>///
>/// 类型简要描述
>/// - 条目说明
>///
>/// </summary>
>public class AClass
>{
>    
>      /// <summary>
>      /// 姓名
>      /// </summary>
>      public string Name { get; set; }
>
>	  #region Print() - 打印信息
>
>      /// <summary>
>      /// 描述说明
>      /// </summary>
>      /// <param name="index">参数说明</param>
>      /// <returns>返回结果</returns>
>      public string Print(int index)
>      {
>            /*
>             * [ 描 述  人 ] 桑云龙
>             * [ 创建日期 ] 2020-01-01
>             *
>             * 不好理解的内容描述...
>             * -
>             *
>             * */
>             return default;
>      }
>
>      #endregion Print() - 打印信息
>
>}
>
>```
>
><br/>

>[!WARNING|style: flat|label: 代码健壮性]
>
><span style='color:red'>[ 代码的变动 - 是否会影响其他功能 ]</span>&nbsp;<span style='color:red'>[ 用户参数 - 是否做细致的校验 ]</span>&nbsp;<span style='color:red'>[ 是否会破坏`API`的兼容性 ]</span>
>
>- 当前的实现方式 - 是否能兼容以后类似的扩展需求
>
>  比如在[`新增接口、API 或者调整参数`]以解决某一问题上，可以考虑是否<span style='color:red'>[ 后续会有其他类似情况发生 ]</span>
>
>  &nbsp;&nbsp;\- 假设我们需要定义一个[`API - 接口`]去获取一个`用户的某些信息, 例如联系方式等`我们定义的 API 就不能只返回这些信息<span style='color:red'>[ 而是应该把用户相关的信息都返回 ]</span>
>
>  &nbsp;&nbsp;\- 假设我要定义一个参数，虽然当前定义成单个元素即可满足，(`例如: string, int`)但是以后是否会涉及到多个元素的场景，是否定义成 `stirng[], int[]`是更优的
>
>  <br/>


# Tensority 矿机 相关文档整理

+ tensority
  + input: `block_header_hash` & `seed`
    + `block_header_hash`
      + [区块头hash流程](https://github.com/Bytom/B3-Mimic/blob/master/docs/blhr_hash_V3.go)
    + `seed`
      + 从 `seed` 生成矩阵需要花费一定时间，`seed` 256个区块改变一次，故 seed 生成的矩阵数组可以做个 cache 以复用
  + output: `tensority_hash`
+ 代码实现
  + [cpp openBLAS](https://github.com/Bytom/CppTensority)
    + 最慢
    + 但方便参考改成 gpu 版本，其下亦提出了关于如何修改成 gpu 版本的建议
  + [go](https://github.com/Bytom/bytom/tree/master/mining/tensority)
    + 目前用户普遍使用的版本，并且是目前兼容性最好，环境最容易搭建的版本
  + [SIMD](https://github.com/Bytom/bytom/tree/dev-ts-simd/mining/tensority)
    + Intel SIMD 指令集版本, 也是目前cpu上最快的版本
+ 算法解释
  + [Tensority Paper](https://github.com/Bytom/bytom/wiki/download/tensority-v1.2.pdf)
  + [procedure](https://github.com/HAOYUatHZ/tensorityMinerDocs/blob/master/tensority-mining-algo.pdf)
  + [图解比原链Tensority算法：如何让POW做到人工智能友好](https://mp.weixin.qq.com/s?__biz=MzUyNDE0NTI4Mw==&mid=2247484535&idx=1&sn=e251a62eaa04b074bfd8dcff46d113ce&chksm=fa30839bcd470a8d8f7fa76af5f576351efd8015945cb90f654aed81942ca71e833ff8a28d3b&mpshare=1&scene=1&srcid=05242TRDoWpKreNF9DVbUZXL&pass_ticket=V2pRSyMpC9ab2InnlR1w4tUO8L%2FaDRK3fmUsMWcx3xF5eZCgI6ZwkIyAsFwcz0UF#rd)
+ [与 stratumn 协议矿池通信模拟 B3](https://github.com/Bytom/B3-Mimic)
  + [通信格式](https://github.com/Bytom/B3-Mimic/blob/master/docs/STRATUM-BTM.md)
  

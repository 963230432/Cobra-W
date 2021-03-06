## 更新日志
- 2017-9-7
    - Cobra 2.0完成
    - 改写grep以及find，提供更好的底层支持
- 2017-9-7
    - Cobra-W 0.1完成
    - 去除相关冗余代码
- 2017-9-8
    - Cobra-W 0.1.1完成
    - 去除api以及cve部分代码
- 2017-9-18
    - Cobra-W 0.2完成
    - 新的rule规则
    - 重构完成
- 2017-9-27
    - Cobra-W 0.3完成
    - 重写rule分类，新增自定义处理配合初步ast
- 2017-10-12
    - Cobra-W 0.31完成
    - 深度AST分析第一部分完成，可递归遍历变量
- 2017-10-17
    - Cobra-W 0.32完成
    - 深度AST分析第一部分完善，递归自定义函数接近完成
- 2017-10-25
    - Cobra-W 0.33
    - 修复了一个issue，在处理if，else时候的bug
    - 更新了开发文档
- 2017-10-27
    - Cobra-W 0.4
    - 修复了CVI-1004的一部分致命bug
    - 更新了vustomize-match的多文件支持
- 2017-11-3
    - Cobra-W 0.5
    - 修复了issue#5
    - 更新了在递归变量时对数组的回溯
- 2017-11-22
    - Cobra-W 0.6
    - 修复了敏感语句在函数声明中回溯不正确的问题
    - 更新了全新的机制应用于敏感语句被封装于新函数的情况
- 2017-11-23
    - Cobra-W 0.6.1
    - 修复了生成新规则机制应用于function-param-regex
    - 更新了新的测试文件应对类变量回溯
- 2017-11-27
    - Cobra-W 0.7
    - 更新了全新的机制应用于类变量回溯，已完成大部分支持
- 2017-12-1
    - Cobra-W 0.7.1
    - 修复类变量回溯的多个bug，对类变量回溯已经有比较完整的支持
- 2017-12-7
    - Cobra-W 0.7.2
    - 修复处理BinaryOp节点时无法正确处理的bug
    - 部分修复了issue#9
    - 修复了对for节点以及if\else节点的支持
- 2017-12-22
    - Cobra-W 0.7.3
    - 修复了部分处理ast的bug
    - 完善了cvi-1009
- 2017-12-27
    - Cobra-W 0.8
    - 全新的secret机制，自定义解决不同cms的过滤不一，导致的扫描误差大问题
    - 更新修复了判断是否被修复的问题
- 2017-12-28
    - Cobra-W 0.8.1
    - 修复了secret机制对auto rule的支持
- 2018-01-09
    - Cobra-W 0.8.2
    - 修复了部分bug
    - 添加部分debug log用于调试
- 2018-01-12
    - Cobra-W 0.8.3
    - 修复了python3支持
- 2018-01-17
    - Cobra-W 1.0.0-beta.1
    - 添加单元测试
    - 添加更完善的开发文档
- 2018-08-01
    - Cobra-W 1.0.1
    - 更新了solidity中only-regex-match模式的支持
- 2018-08-31
    - Cobra-W 1.1.0
    - 更新了新的regex-return-regex模式
- 2019-04-16
    - Cobra-W 1.2.0
    - 修复了include节点中出现变量，无法正确回溯的问题
    - 花大代价尝试重构关于ast处理部分，把ast处理整体提出
    - 解决了之前无法检索define全局变量的问题
- 2019-04-19
    - Cobra-W 1.3.0
    - 添加了调用链展示功能
    - 试探性的加入了疑似漏洞在漏洞表内
    - 修复了上版本中如果路径错误会导致获取node失败的问题
    - 修复了针对function节点递归检测异常的问题
    - 修复了针对function-regex模式即使匹配到敏感函数之后还会继续匹配的问题
- 2019-04-23
    - Cobra-W 1.4.0
    - tamper中更新加入了关于输入函数的tamper部分，现在可以通过设置输入函数来定制扫描
    - 修复了对于list参数为空时仍会进入分析的bug
    - 修复了关于function_flag设置的bug
    - 添加了父类在递归中以解决部分无限递归的问题
- 2019-04-23
    - Cobra-W 1.4.1
    - 修复新生成函数正则表达式过于宽松导致的递归问题
    - 修复list变量的bug
    - 修复了深层递归的bug
    - 添加了指定语言功能以避免语言判断出问题的时候
- 2019-05-15
    - Cobra-W 1.4.2
    - 添加了内置函数列表以标记避免无意义的搜索
    - 优化递归逻辑以减少无意义的搜索
- 2019-05-16
    - Cobra-W 1.5.0
    - 添加了-b参数以设置扫描时的黑名单，可以用来避免扫描第三方模块，造成无意义的搜索
    - 修复了tamper中无法设置函数名为输入的问题
- 2019-06-10
    - Cobra-W 1.6.0
    - 修复了部分在is_repair的判断错误问题
    - 重构了关于语言设置的问题，现在可以同时对多种语言扫描，并留下了各种语言的拓展位
    - 添加了关于简单的js的支持，现在可以进行正则匹配扫描
- 2019-06-17
    - Cobra-W 1.6.1
    - 修复了多语言同时扫描时遇到的bug
    - 修复了引入多语言扫描之后导致的无用扫描
- 2019-06-19
    - Cobra-W 1.7.0 
    - 引入了special-crx-keyword-match的新型匹配方法
    - 添加了关于chrome ext的审计模式并引入了
    - 修复了新python3.8中废弃的相关属性
- 2019-07-05
    - Cobra-W 1.7.1
    - 重构了关于语法解析的部分代码逻辑
    - 删除了python2.7的支持，舒服了~
- 2019-09-29
    - Cobra-W 1.8.0
    - 历时接近3个月，完成了关于javascript的语义分析
    - 测试并通过了jsprime其中大多测试样例
    - 重构Cobra底层关于多语言区分的支持，现在可以自由的添加新语言分析
- 2019-10-08
    - Cobra-W 1.8.1
    - 修复了不知道什么版本导致的无法针对单个文件的扫描bug
    - 现在支持-t后跟随单个文件进行分析
- 2019-10-23
    - Cobra-W 1.8.2
    - 修复了针对chrome 插件扫描时无法扫描js的bug
    - 添加了js美化代码模块以便于更好的扫描以及人工确认
- 2019-11-04
    - Cobra-W 1.9.0
    - 将Python版本限制升级到3.6并添加多处异步优化
    - 现在工具整体扫描效率优化了3倍左右
- 2019-12-13
    - Cobra-W 1.9.1
    - 修复了针对Chrome Ext的多个扫描bug
    - 添加了-u模式用于设定是否需要展示疑似漏洞
- 2020-01-26
    - Cobra-W 1.9.2
    - 修复了在单独文件扫描时的bug
    - 将逐行扫描的方式修改为逐5行扫描，并引入了新的方式去修复line number错误的问题
    - 修复了在php的if/else中变量错误传递的问题 #63
    - 修复了在php的array check中的错误逻辑 #65
- 2020-04-24
    - Cobra-W 1.9.3
    - 修复了因为每5行扫描而导致的无法定位参数问题 #68
    - 修复了在if/else递归逻辑中错误的逻辑关
    - 我必须要承认，由于对php结构的不熟悉，对于大多出后加的语法接口，基本都是出现问题之后才写的，相互割裂太严重，导致引入了过多的递归跳出逻辑，严重影响到了对作用域的控制
- 2020-04-26
    - Cobra-W 1.9.4
    - 修复了全局变量扫描的时候遇到的语法错误 #69
    - 修复了if/else中不正确的进出逻辑
    - 添加了新恶意函数列表的展示，并优化其逻辑
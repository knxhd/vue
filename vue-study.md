### vue学习项目

#### 样式使用
- vue样式
    - 使用class绑定样式
         - 直接使用数组，需要用v-bind进行数据绑定，需要用单引号或者双引号
         - 在class绑定中，还可以使用三元表达式来设置样式
              ###### 即 :class="[flag?'className':''] ，如果flag式true，则className将绑定在元素中
         - [demo：/demo/vue-style-class.html]()
     - 使用style行内样式，如果类型名包含-，则需要使用单引号或者双引号括起来
          ######  :style="{类型名:'类型值'}" 
          ######  :style="{'类型-名':'类型值'}" 
        - [demo：/demo/vue-style-style.html]()
 - v-for使用
    ###### 复习一下数组的操作push、pop、unshift、shift的用法
        - push：在数组尾部插入一条数据
        - pop：移除数组尾部的一条数据
        - unshift：在数组首部插入一条数据
        - shift：移除数组首部的一条数据
    - [demo：/demo/v-for.html]()
    - 在组件中使用，key是必须使用的
    - 循环数组
        ###### v-for="(item,i) in list" 
        ###### 或
        ###### v-for="item in list"
    - 循环对象
        ###### v-for="item in object" 
        或(对象，键)
        ###### v-for="(item,key) in object"
        或(对象、键、索引)
        ###### v-for="(item,key,index) in object"
    - 循环数组
        ###### v-for="item in number"
        ###### 例如：v-for="item in 50"，循环50个数
     - 演示key值得使用，如果不指定key，可能会出现bug，参见 v-for-key.html
    
        

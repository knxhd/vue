### vue学习项目

#### 样式使用
- vue样式
    - 使用class绑定样式
         - 直接使用数组，需要用v-bind进行数据绑定，需要用单引号或者双引号
         - 在class绑定中，还可以使用三元表达式来设置样式
              ###### 即 :class="[flag?'className':''] ，如果flag式true，则className将绑定在元素中
         - [demo：demo/vue-style-class.html](demo/vue-style-class.html)
     - 使用style行内样式，如果类型名包含-，则需要使用单引号或者双引号括起来
          ######  :style="{类型名:'类型值'}" 
          ######  :style="{'类型-名':'类型值'}" 
        - [demo：demo/vue-style-style.html](demo/vue-style-style.html)
 - v-for使用
    ###### 复习一下数组的操作push、pop、unshift、shift的用法
        - push：在数组尾部插入一条数据
        - pop：移除数组尾部的一条数据
        - unshift：在数组首部插入一条数据
        - shift：移除数组首部的一条数据
    - [demo：demo/v-for.html](demo/v-for.html)
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
     - 演示key值得使用，如果不指定key，可能会出现bug，参见 [v-for-key.html](demo/v-for-key.html)
     
     
    
        
- 品牌列表的练习 [goodDemo.html](day2/goodDemo.html)
    - 复习知识点，在list中过滤数据
      - 使用find函数

        - this.list.find((item,index)=>{ 
        
             //过滤条件
            
            return  item.id====1;       
          })
     
       - 使用findIndex函数，此函数获得的是筛选的值的索引
            - this.list.find((item,index)=>{ 
                         
                 //过滤条件
                
                 return  item.id====1;       
              })
       - 使用filter函数进行筛选，方法和上面的类似
- 过滤器
    - 过滤器的命名和调用格式
        - Vue.filter("过滤器名称",function(data){});
        - {{name | 过滤器名称}}
     - 例子见 [vue-filter.html](day2/vue-filter.html)
     - ES6新方法，padStart(maxLength,fillString)和padEnd(maxLength,fillString)，
        - 作用：如果字符串不足maxLength长度，使用fillString补充
        - 注意，该方法是字符串特有的方法
- 指令，感觉不太常用，以后用到了，可以看官网进行运用。官网文档[自定义指令](https://cn.vuejs.org/v2/guide/custom-directive.html)
    - 指令的定义和调用格式
        - Vue.directive("指令名称",{
             bind:function(el){
             
             },
             inserted:function(el){
             
             },
             update: function(el){
             
             },
           });
        - 注意，指令定义不需要加前缀，但是使用时，必须使用前缀v，即v-自定义指令名字

     
       
        

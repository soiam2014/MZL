* 引用的三种方式：赋值，深拷贝，浅拷贝  
  python中统一都是引用传递，类型是属于对象的，而不是变量。
  对象有两种，“可更改”和“不可更改”对象。
  https://www.jianshu.com/p/e93b6131a5cb
* python 中的 == 判断的到底是什么？
  https://blog.csdn.net/kobebryantlin0/article/details/73391584
* 小整数对象池：  
  python为了优化速度，会把【-5,256】之间的数据提前存放在小整数对象池中，程序中只要用的【-5，256】之间的数据不会再重新创建一份，都是指向对象池中的同一份数据，除了这个区间之外的数据，每次使用时系统都会重新申请一块内存，用来存储数据。
* py基本数据类型：  
  不可更改：数值、元组、字符串  
  可更改：列表、集合、字典
* a = '123A' b = '123A' a is b True  
  a = '12@'  b = '12@'  a is b False  
  只包含字母、数字、下划线的字符串会在编译时驻留，和解释器的具体实现有关。
* 正则表达式：  
  1）反向引用：  
        \1代表引用第一次匹配到的()括起来的部分<br>
        \2代表引用第二次匹配到的()括起来的部分<br>
        python中写成\\1  \\2  <br>
  2）findall 匹配的是**（）里的内容**，如果不加括号，则默认匹配全字符（最大括号）<br>
  3）search 之后结果的group方法返回匹配的**整个表达式的字符串**，且返回的是匹配到的第一个<br>
  4）正则匹配的两种写法，一个先编译pattern，再pattern匹配；另外一个直接匹配，不编译pattern。<br>
 * 多线程：  
   使用threading 模块创建线程： <br> 
      直接从threading.Thread继承创建一个新的子类，  <br>
      并**实例化**后调用**strat()方法**启动新线程，他实际上调用了线程的run()方法。<br>
 * 函数装饰器： 就是增强函数或类的功能的一个函数。<br>
   1）使用场景：授权验证、登陆验证、日志记录  <br>
   2）作用：原函数不需要做任何修改，只需在定义的地方加上装饰器。提高了程序的可重复利用性，并增加了程序的可读性。  <br>
   3）why？装饰器在 Python 使用如此方便都要归因于 Python 的函数能像普通的对象一样能作为参数传递给其他函数，可以被赋值给其他变量，可以作为返回值，可以被定义在另外一个函数内<br>
  * 参数：  
    *args 用来将参数打包成tuple给函数体调用<br>
    **kwargs 打包关键字参数成dict给函数体调用 <br>
    参数arg、*args、**kwargs三个参数的位置必须是一定的。必须是(arg,*args,**kwargs)这个顺序，否则程序会报错。 <br>

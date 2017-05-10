***Illuminate\Http\Request;***

# 获取请求
 
 1. 简单：
            public function store(Request $request);
 2. 路由中有参数，将路由参数置于其后：
            Route::put('user/{id}', 'UserController@update');
            public function store($request $request, $id);

# 基本请求信息
1. path()     获取请求的uri
    http://domain.com/foo/bar   => /foo/bar
2. is()         判断接收到的uri与指定的uri是否匹配
3. url()         获取请求的url，？之前的部分
4.fullUrl()    获取完整的url， 加上？后的部分
    http://domain.com/foo/bar?name=zhangsan&age=12

# 获取输入值

1. input("name", "张三") 获取值，如果没有，第二个参数为默认值
2. 可以使用访问属性的方法访问
3. 如果输入值为数组可以使用.的方式获取
4. has()  判断值是否出现，出现且不为空时返回true
5. all()  获取所有输入数据
6. only() 传入数组
7. except()

# 基础语法

## 1.迭代器

```text
def foo():
    print("starting...")
    a = 1
    while True:
        print("hello")
        yield a    #使用yield代表这是一个生成器，功能类似于一个return
        a += 1

g = foo()         #生成一个生成器
print(next(g))    #第一次运行，运行到yield处返回,此时打印了a的值并将其返回
print("*"*20)
print(next(g))    #再次运行，从a+=1开始再次运行到yield处，此时a的值+1
print("*"*20)
print(next(g))    #同上


#运行结果
starting...
hello
1
********************
hello
2
********************
hello
3
```

 


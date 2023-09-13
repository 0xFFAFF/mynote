# python 线程操作

- import threading(导入多线程的包)
- threading.active_count()  # 返回当前线程数
- threading.enumerate()  # 返回当前线程列表
- threading.current_thread()  # 返回当前线程
- threading.Thread().start()  # 启动线程
- threading.Thread().join()  # 等待线程结束, 当前线程阻塞
- l = threading.Lock() # 创建一把锁
- l.acquire() # 上锁
- l.release() # 解锁


Python中创建多线程的方法
```python
import threading
def run(n):
    print('task',n)
    return
newThread = threading.Thread(target=func, args=(), kwargs={})
newThread.start()

```


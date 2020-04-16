《程序员修炼之道》第二版中译反馈
======

如果在阅读过程中发现了任何错误，可以在 Issues 里提出来。争取能在下次印刷中改过来。

已知勘误：
========

* 121/122页 代码中注释排版有问题。应该是这样的：
```ruby
def update_customer(transaction_amount)
	File.open(@name + ".rec", "r+") do |file|             # >--
		read_customer(file)                           #    |
		@balance = @balance.add(transaction_amount,2) #    |
		write_customer(file)                          #    |
	end                                                   # <--
end
```
* 302页 答案9 “我们不考虑~~迸~~(进)出存储设备的信息所需的传输时间”

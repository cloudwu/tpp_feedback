《程序员修炼之道》第二版中译反馈
======

如果在阅读过程中发现了任何错误，可以在 Issues 里提出。争取能在下次印刷中修正。

已知勘误：
========

* 19 页 就去读一本讲设计和~~构架~~架构的书。

* 37 页代码 `calculate_length` 应统一为 calculateLength , 且 setStart 及 setEnd 函数最后缺少分号，应该是这样的：
```java
class Line {
	private double length;
	private Point start;
	private Point end;

	public Line(Point start, Point end) {
		this.start = start;
		this.end = end;
		calculateLength();
	}

	// public
	void setStart(Point p) { this.start = p; calculateLength(); }
	void setEnd(Point p) { this.end = p; calculateLength(); }

	Point getStart(void) { return start; }
	Point getEnd(void) { return end; }

	double getLength() { return length; }

	private void calculateLength() {
		this.length = start.distanceTo(end);
	}
};
```	
* 63 页 单独的一个 "/" 请求会交给 Page~~w~~Controller 模块的 `index` 函数处理。
* 81 页中间，命令补全之上的代码应为：  alias rm='rm -iv'
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
* 166 页下方代码，缺少一个 ) 和一个 } 。应该是：
```java
void printLocation(Locatable item) {
	if (item.locationIsValid()) {
		print(item.getLocation().asString());
	}
}
// ...
```
* 215页 原文：
> 如果你想更深入了解比塞奇威克介绍的东西，......

应改为：
> 如果你想了解比塞奇威克介绍的更深入的东西，......
* 302页 答案9 “我们不考虑~~迸~~(进)出存储设备的信息所需的传输时间”

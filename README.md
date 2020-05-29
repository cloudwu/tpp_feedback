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
* 77 页 即使 ~~其时~~ 产生数据的应用程序可能已失效很久。
* 81 页中间，命令补全之上的代码应为：  alias rm='rm -iv'
* 119 页 地海巫 ~~師~~ 师
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
* 142 页的图中，ch == * 应为 ch == " ，参见：https://github.com/cloudwu/tpp_feedback/issues/14
* 166 页下方代码，缺少一个 ) 和一个 } 。应该是：
```java
void printLocation(Locatable item) {
	if (item.locationIsValid()) {
		print(item.getLocation().asString());
	}
}
// ...
```
* 215 页 如果你想更深入了解 ~~比~~ 塞奇威克介绍的东西，......
* 225 页 诺 ~~米~~ 维格 （Peter Norvig）
* 278 页 但再 ~~仔细一些盘问~~ 盘问仔细一些之后会知道 
* 302页 答案9 “我们不考虑~~迸~~(进)出存储设备的信息所需的传输时间”

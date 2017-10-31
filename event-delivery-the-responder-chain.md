# Event Delivery: The Responder Chain

事件开始时，UIKit生成event并添加到app的事件队列，事件可能是touch事件也可能是motion事件

事件处理过程是，UIApplication单例从事件队列取出事件并分发给key window。对于touch事件，key window将事件传递给hit-test view。对于其他事件，将传递给第一响应者


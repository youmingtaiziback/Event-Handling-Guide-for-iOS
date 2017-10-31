# Event Delivery: The Responder Chain

事件开始时，UIKit生成event并添加到app的事件队列，事件可能是touch事件也可能是motion事件

事件处理过程是，UIApplication单例从事件队列取出事件并分发给key window。对于touch事件，key window将事件传递给hit-test view。对于其他事件，将传递给第一响应者

## Hit-Testing Returns the View Where a Touch Occurred

hit-test过程，调用hitTest:withEvent:，该方法内部还会调用pointInside:withEvent:

> 在生命周期内，touch一直与hit-test view关联，即使touch移出了view

## The Responder Chain Is Made Up of Responder Objects

UIApplication、APPDelegate、UIView、UIViewController都是UIResponder的直接子类

一个对象成为第一响应者的方法：

* `canBecomeFirstResponder`
* `becomeFirstResponder`

## The Responder Chain Follows a Specific Delivery Path




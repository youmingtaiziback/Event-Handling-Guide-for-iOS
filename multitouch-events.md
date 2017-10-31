# Multitouch Events

## Create a Subclass of UIResponder

创建UIResponder的子类，UIView、UIViewcontroller、UIControl、UIApplication、UIWindow

实现UIResponder的事件处理方法

## Implementing the Touch-Event Handling Methods in Your Subclass

UIResponder和UIGestureRecognizer有相同签名的事件处理方法

当触控事件结束或者取消后，应该清理掉之前保留的事件

## Tracking the Phase and Location of a Touch Event

## Receiving and Querying Touch Objects

`multiTouchEnabled`默认为NO，此时事件处理方法每次被调用时touches里面只包含一个touch。如果设置为YES，包含多个

`touchesForWindow:`、`touchesForView:`

## Handling Tap Gestures

## Handling Swipe and Drag Gestures

## Handling a Complex Multitouch Sequence

如果需要保存touch，需要用CFDictionaryRef而不能用NSDictionary，因为后者需要对象实现NSCopying协议

如何判断最后一个手指离开了界面：`[touches count] == [[event touchesForView:self] count]`

## Specifying Custom Touch Event Behavior

影响事件流的方法

* multipleTouchEnabled
* exclusiveTouch
* hitTest:withEvent:

永久禁止接收事件：userInteractionEnabled

临时就是接收事件：beginIgnoringInteractionEvents、endIgnoringInteractionEvents

## InterCepting Touches by Overriding Hit-Testing

覆盖hitTest:withEvent:

## Forwarding Touch Events

分析事件的方法

* 加一层superview
* 覆盖UIWindow的sendEvent:方法，一定要调用\[super sendEvent:\]

## Best Practices for Handling Multitouch Events

实现取消方法

如果在UIView、UIViewController、UIResponder的子类处理事件：实现所有方法、不调用super的实现

如果在UIKit的其他Responder的子类处理了事件：无需实现所有方法、必须调用super的实现

不要向自己定义的UIView子类以外的Responder转发事件

不显示调用nextResponder，调用superclass的实现

不使用近似取整

## 




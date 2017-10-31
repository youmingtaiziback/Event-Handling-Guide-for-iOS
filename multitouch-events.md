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

## Specifying Custom Touch Event Behavior

## InterCepting Touches by Overriding Hit-Testing

## Forwarding Touch Events

## Best Practices for Handling Multitouch Events

## 




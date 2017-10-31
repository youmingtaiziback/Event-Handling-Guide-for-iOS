# Gesture Recognizers

## Use Gesture Recognizers to Simplify Event Handling

尽量使用系统提供的gesture recognizer，如果不能满足可以自定义

#### Built-in Gesture Recognizers Recognize Common Gestures

_iOS Human Interface Guidelines_

#### Gesture Recognizers Are Attached to a View

view和gesture recognizer是1对N的关系

gesture recognizer处理事件的优先级高于event handling

#### Gestures Trigger Action Messages

离散手势、连续手势

## Responding Events with Gesture Recognizers

#### Using Interface Builder to Add a Gesture Recognizer to Your App

#### Adding a Gesture Recognizer Programmatically

#### Responding to Discrete Gestures

#### Responding to Continuous Gestures

## Defining How Gesture Recognizers Interact

#### Gesture Recognizers Operate in a Finite State Machine

![](/assets/import.png)

#### Interacting with Other Gesture Recognizers

默认条件下，同一个view上面的多个gesture recognizer哪一个现接受事件是不确定的

影响多个gesture recognizer接受事件顺序的方式有

* UIGestureRecognizer类方法
  * 两个gesture recognizer之间指定顺序：\[a requireGestureRecognizerToFail:b\]，a一直等待，直到b失败a才开始接受事件
* 代理方法
  * 禁止gesture recognizer处理事件
    * gestureRecognizer:shouldReceiveTouch:，只要有新的touch事件就会被调用。UIView和UIGestureRecognizer都有该方法
    * gestureRecognizerShouldBegin:，gesture recognizer尝试从Possible状态转移出去的时候调用
  * 支持同时识别手势
    * gestureRecognizer:shouldRecognizeSimultaneouslyWithGestureRecognizer:该方法只会在一个手势试图阻止另一个手势时被调用，两个手势中只需要一个代理方法返回YES
* 覆盖子类方法

#### Interacting with Other User Interface Controls

## Gesture Recognizers Interpret Raw Touch Events

## Regulating the Delivery of Touches to Views

## Create a Custom Gesture Recognizer




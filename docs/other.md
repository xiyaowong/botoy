# 其他

- 简单测试了下，效率先不确定，但基本不会漏消息

- bot 端的内置队列貌似还不太稳定，必要时请自行设置延时，但又由于接收函数之间和每次接收到新消息后，运行都是同时进行的,
  由此导致的频率和数据安全问题，请自行解决

- botoy.collection
  模块封装了已知的消息类型(MsgTypes)和事件类型(EventNames)以及部分表情代码(Emoticons)

- 消息上下文的字段命名与原数据完全一致

- 私聊消息比较难处理，如果好友消息 ctx 的 TempUin 不为 None，说明是私聊消息,
  这个字段是私聊入口群号, 可以用 `ensure_tempMsg`接收函数装饰器确保是私聊消息
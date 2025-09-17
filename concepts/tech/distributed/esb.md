Enterprise Service Bus


# classic
- 所有服务通过一个总线通信
- message routing
  - 根据消息内容或元数据决定发送到哪个服务，例如基于订单类型发送到不同系统。
  - [business logic]
  - modern alternative: message topic
- Protocol Bridging
  - 在不同通信协议之间转换，如 HTTP <--> JMS、SOAP <--> REST。
  - including *message transformation*, XML --> JSON
- orchestration
  - [business logic]
  - modern alternative: low-code app integration
- eventing
  - 根据特定事件触发(Trigger)通知或调用(Invoke)其他服务，如库存不足时自动通知采购系统。
  - [business logic]
- security
  - authN, authR, encryption, ACL
- error handling
  - logging, catch-exception, auto-retry
- Auditing

# modern ESB
rebranded as [App Integration](https://github.com/davidkhala/app-integration)

[wso2 ESB](https://wso2.com/enterprise-service-bus/)
- provided by [WSO2 Micro Integrator](https://wso2.com/integration/micro-integrator/)


[Mulesoft ESB]
- provided by Anypoint Platform

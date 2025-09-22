---
layout:      post
title:       ""
subtitle:    ""
description: ""
excerpt:     ""
date:        2018-05-23
author:      "XiangdiWu"
image: "https://www.lfasiallc.com/wp-content/uploads/2023/05/KubeCon_OSS_China_23_DigitalAssets_web-homepage-1920x606.jpg"
tags:
    - Microservice
    - Security
URL:         "/2018/05/23/external_system_auth/"
categories:  [ "Tech" ]

draft: true
showtoc: false
---

```plantuml
@startuml
SlotAllocator <|-- Instance
TypedSlot o-- Slot

Slot : bool currentThreadRegistered()
Slot : void set(InitializeCb cb)
Slot : ThreadLocalObjectSharedPtr get()

TypedSlot : bool currentThreadRegistered()
TypedSlot : void set(InitializeCb cb)
TypedSlot : ThreadLocalObjectSharedPtr get()
TypedSlot : void runOnAllThreads(const UpdateCb& cb)

SlotAllocator : SlotPtr allocateSlot()

Instance : void registerThread(Event::Dispatcher& dispatcher, bool main_thread)
Instance : void shutdownGlobalThreading()
Instance : void shutdownThread()
Instance : Event::Dispatcher& dispatcher()
Instance : bool isShutdown()
@enduml
```
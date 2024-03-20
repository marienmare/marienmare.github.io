---
layout: post
title: Swift 언어의 호출 규약
categories: [macOS, Swift]
---

64비트 아키텍처에서 Swift로 작성된 바이너리의 함수 호출 및 인자 전달 매커니즘을 이해하기 위해서는 Swift의 호출 규약(Calling Convention)에 대해 알 필요가 있다. 호출 규약은 함수가 어떻게 인자를 받고, 반환값을 어떻게 처리하는지 정의한다.

Swift는 기본적으로 System V AMD64 ABI(Application Binary Interface)를 따르는데, 이는 대부분의 UNIX 기반 시스템(ex: Linux)에서 사용되는 표준이다. Swift는 함수 호출 시 레지스터를 사용해 인자를 전달한다. 일반적으로 첫번째 인자부터 RDI, RSI, RDX, RCX(또는 R10), R8, R9 레지스터를 차례대로 사용한다.



## References

- [https://en.wikipedia.org/wiki/X86_calling_conventions](https://en.wikipedia.org/wiki/X86_calling_conventions)
- 
---

date: 2020-12-10

title: "1차시 Intro (1~2강)"

categories: os

tags: os cs os-lecture

toc: true

toc_sticky: true

---

## 1강 Intro

>  인트로



## 2강 Introduction to Operating Systems

> 운영체제 개요

### 운영 체제란?

- 협의의 운영체제
  - 운영체제의 핵심 부분으로 메모리에 상주하는 부분 (커널)
- 광의의 운영체제
  - 커널 + 각종 주변 유틸리티(ex. 파일 다운로더)



### 운영 체제의 목적

1. 컴퓨터를 편리하게 사용할 수 있는 환경을 제공
2. 프로세서, 기억장치, 입출력 장치 등 각종 :star:**자원을 효율적으로 관리** + :star:**형평성(자원이 소외되지 않도록)**



### 운영 체제의 분류

#### 동시 작업 가능 여부

- 단일 작업
  - MS-DOS
- 다중 작업
  - UNIX, MS Windows

#### 사용자 수

- 단일 사용자
  -  MS-DOS, MS Windows
- 다중 사용자
  - UNIX, NT server

#### 처리 방식

- 일괄 처리 (batch processing)
  - 예전 컴퓨터
  - 작업카드로 구멍 뚫어서 프로그래밍
- 시분할(time sharing)
  - 현재 컴퓨터
  - 여러 작업을 컴퓨터가 일정한 시간 단위로 분할하여 사용
  - Interactive한 방식
  - 사용자가 많아지면 느려짐 => 정확한 시간을 지키거나 하지는 않음
- 실시간(Realtime OS)
  - 정해진 시간 안에 반드시 종료가 보장됨
  - Hard realtime system (경성 실시간 시스템)
    - 특수 목적 시스템 (ex. 원자로/공장 제어, 미사일 제어, 반도체 장비, 로보트 제어)
  - Soft realtime system (연성 실시간 시스템)
    - 영화 프레임 등 - 하지만 실서비스는 사용 X, 시분할로 해결 (시간 지났다고 멈추면 안되니까)

우리가 사용하는 운영체제

- 다중 작업
- 다중 사용자
- 시분할

\* 헷갈리는 용어 정리

Multitasking, Multiprogramming(메모리 강조), Time sharing(CPU 강조), Multiprocess : CPU가 1개여도 동시에 task 수행 가능

Multoprocessor : CPU(processor)가 여러 개



### 운영 체제의 예

| 분류      | 유닉스(UNIX)                                        | Windows     |
| --------- | --------------------------------------------------- | ----------- |
| 초기 목적 | 대형 컴퓨터                                         | 개인 컴퓨터 |
| 사용자    | 다중 사용자                                         | 단일 사용자 |
| 소스코드  | 공개                                                | 비공개      |
| 이식성    | 높음(C언어라서 다른 컴퓨터로 옮겨서 컴파일 하면 됨) |             |
| 커널 크기 | 작음(핵심만, 확장성 높음)                           |             |
| GUI       | X                                                   | O           |



### 운영 체제의 구조

CPU(속도 빠름) -> memory(속도 중간) -> Disk, I/O device(속도 느림)

CPU 스케줄링 -> 메모리 관리 -> 파일 관리(disk 스케줄링), 입출력 관리

프로세스 관리

그 외(보호 시스템, 네트워킹, 명령어 해석기)


출처 : http://www.kocw.or.kr/home/cview.do?mty=p&kemId=1046323
---
title: "Day 1: 텍스트 RPG 관리자 모드"
date: 2025-05-24 14:30:00 +0900
tags: [RPG, C++]
categories: [TextRPG]
layout: post
---

#프로젝트명: 텍스트 RPG 실습 프로젝트

목적: 매일 하나씩 기능을 추가하며 C/C++ 파일 입출력, 자료구조, 제어문 등을 연습


[2025.05.24 Day 1 – 텍스트 RPG 관리자 모드 구현]

오늘 목표 : 텍스트 기반 RPG의 “관리자 모드” 기능 구현

-----------------------------------------------------------------------

구현 내용

1) 직업별 스테이터스 입력 및 저장

struct JobInfo 형태로 직업명, 체력·공격력·방어력 등 입력

fwrite를 이용해 바이너리 파일(JobInformation.jit)에 저장

저장된 정보 수정 기능

fopen("rb") 모드로 파일 열기

정보 출력 기능

fread로 파일에서 불러와 printf로 개별 직업 스테이터스 출력

--------------------------------------------------------------------------

문제 해결 & 배운 점

최대한 extern을 사용하고 싶지않아서 구조체 포인터 변수로 해결하였습니다.
switch문을 활용해 수정시에도 전체 수정이 아닌 부분수정이 가능하도록 구현했습니다.
1개의 함수에 1가지의 기능만 들어갈 수 있게 최대한 작게 쪼개어 구현하려고 노력하고 있습니다.
fopen, fread, fclose 등 파일과 관련된 함수들을 이용하게되면서 어떤식으로 사용할 수 있는지 알게됐습니다.

--------------------------------------------------------------------------
다음에 추가할 기능
1) 직업 정보 삭제
2) 몬스터 정보 입력
3) 아이템 정보 구현

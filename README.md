# 심화실습-1 보고서

<!-- 
👨🏻‍💻 작성요령
아래 양식에 맞춰 내용을 채워주세요.

⚠️ 주의 ⚠️
단, 해시테그(`#`)로 시작하는 줄은 수정하지 마세요.
제출 내용에서 해시테그로 시작하는 줄이 없어진 경우, 항목 누락으로 간주되어 감점이 있을 수 있습니다.

👀 참고자료
[1] GitHub, GitHub에서 쓰기 위한 빠른 시작, https://docs.github.com/ko/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/quickstart-for-writing-on-github
[2] GitHub, Markdown 기본 문법, https://docs.github.com/ko/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax
-->

## 1. 제출 정보

| 구분 | 내용 |
| --- | --- |
| 학년학기 | 2026학년도 1학기 |
| 과목명(학수번호) | 프로그래밍기초와실습 (DASF004-00) |
| 학번 | 2026314916 |
| 이름 | 프기실 |
| 과제명 | 심화실습-1 |

## 2. 현재 상태

### 2.1 배운적 있는 언어 및 현재 수준

- Python - 중
- C - 하
    - `상, 중, 하` 혹은 `해당없음`
        - 상: 어떤 요구사항을 받아도 어떻게든 구현할 수 있다.
        - 중: 기본적으로 어느정도 수준의 구현은 가능하지만 해당 언어의 고급기술 활용은 어렵다.
        - 하: 가볍게 배워본 정도이다.

### 2.2 실습 환경

| 사용한AI 도구 | 개발환경 |
| --- | --- |
| ChatGPT | VSCode + GCC |

## 3. 코드 리뷰 결과

### 3.1 AI가 생성한 코드를 얼마나 이해할 수 있었는지?

- 이해도: **6 / 10**점 (0점: 전혀 이해하지 못함, 10점: 완전히 이해함)

- AI가 생성한 코드는 일정 관리 프로그램을 구현한 C 언어 코드였다.구조체(`struct`)를 이용하여 일정 정보를 저장하고, 동적 메모리(`malloc`, `realloc`)를 이용하여 일정의 개수를 유동적으로 관리하는 방식으로 작성되어 있었다.  

- 프로그램은 메뉴 기반으로 동작하며 다음과 같은 기능을 수행한다.

  - 일정 추가
  - 일정 조회
  - 일정 수정
  - 일정 삭제
  - 프로그램 종료

- 각 기능은 함수 단위로 분리되어 있으며, `main()` 함수에서는 메뉴를 출력하고 사용자의 선택에 따라 해당 기능을 호출하도록 구성되어 있다.

### 3.2 최초에 입력한 프롬프트와 그 결과물에 대한 평가

#### 최초 프롬프트

```
다음 조건을 모두 만족하는 C 언어 콘솔 프로그램을 한 개의 .c 파일에 구현해줘
1. 기본 요구 기능 
1-1. 일정 추가 - 사용자가 제목, 날짜(YYYY‑MM‑DD), 시간(HH:MM), 설명을 입력하면 일정이 저장된다.
1-2. 일정 조회 - 현재 저장된 모든 일정을 번호와 함께 리스트 형태로 출력합니다. - 일정이 없을 경우 “저장된 일정이 없습니다.” 라는 메시지를 보여준다
1-3. 일정 수정 - 조회 시 표시된 번호를 입력하면 해당 일정의 모든 필드(제목, 날짜, 시간, 설명)를 새 값으로 교체할 수 있다. 
1-4. 일정 삭제 - 조회 시 표시된 번호를 입력하면 해당 일정을 목록에서 제거한다. 
1-5. 프로그램 종료 - 메뉴에서 “0” 혹은 “종료”를 선택하면 프로그램이 정상적으로 종료됩니다.
2. 구현 제약 - 모든 코드는 하나의 .c 파일에 들어가야 하며, gcc 로 컴파일했을 때 오류 없이 동작해야 한다
- 표준 C 라이브러리(stdio.h, stdlib.h, string.h, time.h 등)만 사용하고, 외부 라이브러리는 사용하지 않는다. 
- 구조체(struct Schedule)를 이용해 일정 데이터를 관리하고, 동적 메모리(malloc, realloc)를 사용해 일정 개수를 자유롭게 늘릴 수 있게 한다. 
3. 코드 스타일 & 주석 - 함수 단위로 코드를 작성하고, 주요 함수·변수·구조체에 대한 설명을 주석으로 포함시켜 줘. 
- 각 라인·각 블록에 대한 별도 해설을 코드 뒤에 // 설명: 형태로 달아 주고, 코드 끝에 “코드 라인‑별 해설”이라는 섹션을 추가해, 각 라인의 역할을 한글로 정리해 줘. 
4. 최종 출력물 예시 
4-1. 전체 코드 (schedule_manager.c) 
```

#### 최종 코드 및 실행 결과

> 본 문서 가장 아래 `부록` 섹션에서 `최종 결과물 코드`와 `실행 결과`에 각각 코드 및 실행 결과를 복사 & 붙여넣기로 첨부합니다.

### 3.3 최종 결과물을 얻기까지의 경험

이번 과제에서는 AI 도구를 활용하여 C 언어 일정 관리 프로그램을 구현하였다. 처음에는 요구사항을 정리하여 AI에게 프롬프트를 입력하고 기본적인 프로그램 코드를 생성하였다.

하지만 처음 생성된 코드는 실제로 실행해 보았을 때 정상적으로 동작하지 않는 부분이 있었다. 예를 들어 입력 처리 과정에서 오류가 발생하거나 프로그램이 예상과 다른 방식으로 동작하는 문제가 있었다.

이러한 문제를 해결하기 위해 실행 결과와 오류 메시지를 다시 AI에게 전달하고, 어떤 부분에서 문제가 발생하는지 질문하였다. AI는 해당 문제의 원인을 설명하고 수정된 코드를 다시 제시해 주었다.

이 과정은 한 번에 끝난 것이 아니라 프롬프트 입력 > 코드 생성 > 실행 테스트 > 오류 확인 > 수정 요청의 과정을 반복하면서 진행되었다. 프로그램을 실제로 실행하면서 발생한 문제들을 하나씩 수정해 나가면서 최종적으로 정상 동작하는 일정 관리 프로그램을 완성할 수 있었다.

## 4. 결론

위 과정을 통해 단순히 AI가 생성한 코드를 그대로 사용하는 것이 아니라, 직접 실행해 보고 문제점을 확인 하면서 코드를 수정하는 과정이 중요하다는 것을 경험할 수 있었다. 또한, AI를 활용하면 프로그램의 기본 구조를 빠르게 만들 수 있지만, 프로그램의 동작을 이해하고 검증하는 과정은 개발자가 직접 수행해야 한다는 점을 느낄 수 있었다.

## 참고문헌

- 사용한 AI 도구, 참고한 자료 등

  - OpenAI ChatGPT
  - C언어 표준 라이브러리 문서
  - GitHub Markdown 문서

## 부록

### 실행 결과

- 프로그램의 주요 기능 실행 화면을 터미널에서 텍스트를 복사&붙여넣기로 작성
- 프로그램 실행에 실패했다면, 실패와 관련된 내용을 담아도 좋음

```
==============================
      일정 관리 프로그램      
==============================
1. 일정 추가
2. 일정 조회
3. 일정 수정
4. 일정 삭제
0. 종료
==============================
메뉴를 선택하세요: 1

[일정 추가]
제목: 팀 프로젝트 회의
날짜(YYYY-MM-DD): 2026-03-15
시간(HH:MM): 14:30
설명: 발표 자료 점검
일정이 저장되었습니다.

==============================
      일정 관리 프로그램      
==============================
1. 일정 추가
2. 일정 조회
3. 일정 수정
4. 일정 삭제
0. 종료
==============================
메뉴를 선택하세요: 2

[일정 조회]
1. 제목: 팀 프로젝트 회의
   날짜: 2026-03-15
   시간: 14:30
   설명: 발표 자료 점검
------------------------------

==============================
      일정 관리 프로그램      
==============================
1. 일정 추가
2. 일정 조회
3. 일정 수정
4. 일정 삭제
0. 종료
==============================
메뉴를 선택하세요: 3

[일정 수정]

[일정 조회]
1. 제목: 팀 프로젝트 회의
   날짜: 2026-03-15
   시간: 14:30
   설명: 발표 자료 점검
------------------------------
수정할 일정 번호를 입력하세요: 1
새로운 일정 정보를 입력하세요.
제목: 팀 프로젝트 최종 회의
날짜(YYYY-MM-DD): 2026-03-16
시간(HH:MM): 16:00
설명: 최종 리허설
일정이 수정되었습니다.

==============================
      일정 관리 프로그램      
==============================
1. 일정 추가
2. 일정 조회
3. 일정 수정
4. 일정 삭제
0. 종료
==============================
메뉴를 선택하세요: 4

[일정 삭제]

[일정 조회]
1. 제목: 팀 프로젝트 최종 회의
   날짜: 2026-03-16
   시간: 16:00
   설명: 최종 리허설
------------------------------
삭제할 일정 번호를 입력하세요: 1
일정이 삭제되었습니다.

==============================
      일정 관리 프로그램      
==============================
1. 일정 추가
2. 일정 조회
3. 일정 수정
4. 일정 삭제
0. 종료
==============================
메뉴를 선택하세요: 2

[일정 조회]
저장된 일정이 없습니다.

==============================
      일정 관리 프로그램      
==============================
1. 일정 추가
2. 일정 조회
3. 일정 수정
4. 일정 삭제
0. 종료
==============================
메뉴를 선택하세요: 0
프로그램을 종료합니다.

```

### 최종 결과물 코드

- AI가 생성한 전체 코드 첨부

```
#include <stdio.h>   // 설명: 표준 입출력 함수 printf, fgets 등을 사용하기 위해 포함
#include <stdlib.h>  // 설명: malloc, realloc, free, strtol 등을 사용하기 위해 포함
#include <string.h>  // 설명: strlen, sscanf 등 문자열 처리 함수를 사용하기 위해 포함

#define TITLE_LEN 100   // 설명: 제목 문자열의 최대 길이
#define DATE_LEN 12     // 설명: 날짜 문자열 길이(YYYY-MM-DD + 널 문자)
#define TIME_LEN 7      // 설명: 시간 문자열 길이(HH:MM + 널 문자)
#define DESC_LEN 256    // 설명: 설명 문자열의 최대 길이
#define INPUT_LEN 512   // 설명: 일반 입력을 받을 임시 버퍼의 크기

/* 일정 한 건을 저장하는 구조체 */
typedef struct {
    char title[TITLE_LEN];         // 설명: 일정 제목
    char date[DATE_LEN];           // 설명: 일정 날짜
    char time[TIME_LEN];           // 설명: 일정 시간
    char description[DESC_LEN];    // 설명: 일정 설명
} Schedule;                        // 설명: 일정 데이터 형식 이름을 Schedule로 정의

/* 메뉴 표시 함수 */
void printMenu(void);  // 설명: 프로그램 메뉴를 화면에 출력하는 함수 선언
/* 문자열 입력 함수(개행 제거 포함) */
void readLine(const char *prompt, char *buffer, size_t size);  // 설명: 안전하게 한 줄 문자열을 입력받는 함수 선언
/* 정수 입력 함수(잘못된 입력 방지) */
int readInt(const char *prompt);  // 설명: 숫자만 입력받도록 검증하는 함수 선언
/* 날짜 형식 검증 함수(YYYY-MM-DD) */
int isValidDate(const char *date);  // 설명: 날짜 문자열 형식을 검사하는 함수 선언
/* 시간 형식 검증 함수(HH:MM) */
int isValidTime(const char *time);  // 설명: 시간 문자열 형식을 검사하는 함수 선언
/* 일정 정보 입력 함수 */
void inputSchedule(Schedule *schedule);  // 설명: 제목/날짜/시간/설명을 사용자에게 입력받는 함수 선언
/* 일정 추가 함수 */
void addSchedule(Schedule **schedules, int *count);  // 설명: 동적 배열에 일정을 추가하는 함수 선언
/* 일정 목록 출력 함수 */
void listSchedules(const Schedule *schedules, int count);  // 설명: 저장된 모든 일정을 출력하는 함수 선언
/* 일정 수정 함수 */
void editSchedule(Schedule *schedules, int count);  // 설명: 선택한 일정을 수정하는 함수 선언
/* 일정 삭제 함수 */
void deleteSchedule(Schedule **schedules, int *count);  // 설명: 선택한 일정을 삭제하는 함수 선언

int main(void) {  // 설명: 프로그램 시작점
    Schedule *schedules = NULL;  // 설명: 일정들을 저장할 동적 배열 포인터, 처음에는 비어 있음
    int count = 0;               // 설명: 현재 저장된 일정 개수
    int choice;                  // 설명: 사용자가 선택한 메뉴 번호

    while (1) {  // 설명: 사용자가 종료를 선택할 때까지 계속 반복
        printMenu();  // 설명: 메뉴 화면 출력
        choice = readInt("메뉴를 선택하세요: ");  // 설명: 사용자로부터 메뉴 번호 입력받기

        switch (choice) {  // 설명: 입력한 메뉴 번호에 따라 기능 분기
            case 1:  // 설명: 일정 추가 메뉴
                addSchedule(&schedules, &count);  // 설명: 일정 추가 함수 호출
                break;  // 설명: switch 문 종료
            case 2:  // 설명: 일정 조회 메뉴
                listSchedules(schedules, count);  // 설명: 일정 목록 출력 함수 호출
                break;  // 설명: switch 문 종료
            case 3:  // 설명: 일정 수정 메뉴
                editSchedule(schedules, count);  // 설명: 일정 수정 함수 호출
                break;  // 설명: switch 문 종료
            case 4:  // 설명: 일정 삭제 메뉴
                deleteSchedule(&schedules, &count);  // 설명: 일정 삭제 함수 호출
                break;  // 설명: switch 문 종료
            case 0:  // 설명: 종료 메뉴
                free(schedules);  // 설명: 동적으로 할당된 일정 배열 메모리 해제
                printf("프로그램을 종료합니다.\n");  // 설명: 종료 메시지 출력
                return 0;  // 설명: 프로그램 정상 종료
            default:  // 설명: 정의되지 않은 메뉴 번호 입력 시
                printf("올바른 메뉴 번호를 입력하세요.\n");  // 설명: 오류 메시지 출력
                break;  // 설명: switch 문 종료
        }
    }
}

void printMenu(void) {  // 설명: 메뉴를 출력하는 함수 정의
    printf("\n==============================\n");  // 설명: 메뉴 상단 구분선 출력
    printf("      일정 관리 프로그램      \n");   // 설명: 프로그램 제목 출력
    printf("==============================\n");  // 설명: 메뉴 구분선 출력
    printf("1. 일정 추가\n");  // 설명: 메뉴 1 안내
    printf("2. 일정 조회\n");  // 설명: 메뉴 2 안내
    printf("3. 일정 수정\n");  // 설명: 메뉴 3 안내
    printf("4. 일정 삭제\n");  // 설명: 메뉴 4 안내
    printf("0. 종료\n");      // 설명: 메뉴 0 안내
    printf("==============================\n");  // 설명: 메뉴 하단 구분선 출력
}

void readLine(const char *prompt, char *buffer, size_t size) {  // 설명: 문자열 입력 함수 정의
    size_t len;  // 설명: 입력 문자열 길이를 저장할 변수

    while (1) {  // 설명: 올바른 입력이 들어올 때까지 반복
        printf("%s", prompt);  // 설명: 입력 안내 문구 출력

        if (fgets(buffer, (int)size, stdin) == NULL) {  // 설명: 한 줄 입력 받기
            buffer[0] = '\0';  // 설명: 입력 실패 시 빈 문자열로 처리
            return;  // 설명: 함수 종료
        }

        len = strlen(buffer);  // 설명: 입력된 문자열 길이 계산

        if (len > 0 && buffer[len - 1] == '\n') {  // 설명: 개행 문자가 포함된 정상 입력인지 확인
            buffer[len - 1] = '\0';  // 설명: 마지막 개행 문자를 널 문자로 바꿈
            return;  // 설명: 정상 입력이므로 함수 종료
        }

        /* 입력 버퍼가 넘친 경우 남은 문자를 비움 */
        {
            int ch;  // 설명: 남은 입력을 하나씩 받을 임시 변수
            while ((ch = getchar()) != '\n' && ch != EOF) {  // 설명: 줄 끝까지 남은 문자 제거
                /* 버퍼 비우기 */  // 설명: 반복문 본문은 비워 두고 버퍼만 정리
            }
        }

        printf("입력이 너무 깁니다. 다시 입력하세요.\n");  // 설명: 너무 긴 입력에 대한 안내 메시지
    }
}

int readInt(const char *prompt) {  // 설명: 정수 입력 함수 정의
    char buffer[INPUT_LEN];  // 설명: 입력 문자열을 저장할 버퍼
    char *endPtr;            // 설명: strtol 변환 후 남은 문자열 위치를 가리킬 포인터
    long value;              // 설명: 변환된 숫자를 임시 저장할 변수

    while (1) {  // 설명: 올바른 숫자를 입력할 때까지 반복
        readLine(prompt, buffer, sizeof(buffer));  // 설명: 한 줄 문자열 입력받기

        if (buffer[0] == '\0') {  // 설명: 빈 입력인지 검사
            printf("입력이 비어 있습니다. 다시 입력하세요.\n");  // 설명: 빈 입력 안내
            continue;  // 설명: 다시 입력 받기
        }

        value = strtol(buffer, &endPtr, 10);  // 설명: 문자열을 10진수 정수로 변환

        if (*endPtr == '\0') {  // 설명: 숫자 뒤에 다른 문자가 없는지 확인
            return (int)value;  // 설명: 정상 숫자이면 int로 변환해 반환
        }

        printf("숫자를 입력하세요.\n");  // 설명: 숫자가 아닌 입력에 대한 안내
    }
}

int isValidDate(const char *date) {  // 설명: 날짜 형식을 검사하는 함수 정의
    int year, month, day;  // 설명: 연도, 월, 일을 저장할 변수

    if (strlen(date) != 10) {  // 설명: YYYY-MM-DD 형식 길이인지 확인
        return 0;  // 설명: 길이가 다르면 유효하지 않음
    }

    if (date[4] != '-' || date[7] != '-') {  // 설명: 하이픈 위치가 올바른지 확인
        return 0;  // 설명: 형식이 다르면 유효하지 않음
    }

    if (sscanf(date, "%4d-%2d-%2d", &year, &month, &day) != 3) {  // 설명: 연, 월, 일 파싱
        return 0;  // 설명: 파싱 실패 시 유효하지 않음
    }

    if (year < 1 || month < 1 || month > 12 || day < 1 || day > 31) {  // 설명: 기본 범위 검사
        return 0;  // 설명: 범위를 벗어나면 유효하지 않음
    }

    return 1;  // 설명: 모든 검사를 통과했으므로 유효한 날짜로 판단
}

int isValidTime(const char *time) {  // 설명: 시간 형식을 검사하는 함수 정의
    int hour, minute;  // 설명: 시, 분 값을 저장할 변수

    if (strlen(time) != 5) {  // 설명: HH:MM 형식 길이인지 확인
        return 0;  // 설명: 길이가 다르면 유효하지 않음
    }

    if (time[2] != ':') {  // 설명: 콜론 위치가 올바른지 확인
        return 0;  // 설명: 형식이 다르면 유효하지 않음
    }

    if (sscanf(time, "%2d:%2d", &hour, &minute) != 2) {  // 설명: 시와 분 파싱
        return 0;  // 설명: 파싱 실패 시 유효하지 않음
    }

    if (hour < 0 || hour > 23 || minute < 0 || minute > 59) {  // 설명: 시간 범위 검사
        return 0;  // 설명: 범위를 벗어나면 유효하지 않음
    }

    return 1;  // 설명: 모든 검사를 통과했으므로 유효한 시간으로 판단
}

void inputSchedule(Schedule *schedule) {  // 설명: 일정의 모든 필드를 입력받는 함수 정의
    do {  // 설명: 제목이 비어 있지 않을 때까지 반복
        readLine("제목: ", schedule->title, sizeof(schedule->title));  // 설명: 제목 입력
        if (schedule->title[0] == '\0') {  // 설명: 제목이 빈 문자열인지 확인
            printf("제목은 비울 수 없습니다.\n");  // 설명: 빈 제목 안내
        }
    } while (schedule->title[0] == '\0');  // 설명: 제목이 비어 있으면 다시 입력

    do {  // 설명: 유효한 날짜를 입력할 때까지 반복
        readLine("날짜(YYYY-MM-DD): ", schedule->date, sizeof(schedule->date));  // 설명: 날짜 입력
        if (!isValidDate(schedule->date)) {  // 설명: 날짜 형식 검사
            printf("올바른 날짜 형식이 아닙니다. 예: 2026-03-12\n");  // 설명: 잘못된 날짜 형식 안내
        }
    } while (!isValidDate(schedule->date));  // 설명: 날짜가 유효하지 않으면 다시 입력

    do {  // 설명: 유효한 시간을 입력할 때까지 반복
        readLine("시간(HH:MM): ", schedule->time, sizeof(schedule->time));  // 설명: 시간 입력
        if (!isValidTime(schedule->time)) {  // 설명: 시간 형식 검사
            printf("올바른 시간 형식이 아닙니다. 예: 14:30\n");  // 설명: 잘못된 시간 형식 안내
        }
    } while (!isValidTime(schedule->time));  // 설명: 시간이 유효하지 않으면 다시 입력

    readLine("설명: ", schedule->description, sizeof(schedule->description));  // 설명: 설명 입력
}

void addSchedule(Schedule **schedules, int *count) {  // 설명: 일정을 추가하는 함수 정의
    Schedule *temp;  // 설명: realloc 결과를 임시 저장할 포인터

    temp = (Schedule *)realloc(*schedules, (size_t)(*count + 1) * sizeof(Schedule));  // 설명: 일정 배열 크기를 1개 늘림
    if (temp == NULL) {  // 설명: 메모리 재할당 실패 여부 확인
        printf("메모리 할당에 실패했습니다.\n");  // 설명: 실패 메시지 출력
        return;  // 설명: 함수 종료
    }

    *schedules = temp;  // 설명: 재할당된 새 메모리 주소를 원본 포인터에 반영

    printf("\n[일정 추가]\n");  // 설명: 일정 추가 시작 안내
    inputSchedule(&((*schedules)[*count]));  // 설명: 새로 생긴 마지막 칸에 일정 입력
    (*count)++;  // 설명: 일정 개수 1 증가

    printf("일정이 저장되었습니다.\n");  // 설명: 저장 완료 메시지 출력
}

void listSchedules(const Schedule *schedules, int count) {  // 설명: 저장된 일정을 출력하는 함수 정의
    int i;  // 설명: 반복문 인덱스 변수

    printf("\n[일정 조회]\n");  // 설명: 조회 시작 안내

    if (count == 0) {  // 설명: 저장된 일정이 없는지 검사
        printf("저장된 일정이 없습니다.\n");  // 설명: 일정 없음 메시지 출력
        return;  // 설명: 함수 종료
    }

    for (i = 0; i < count; i++) {  // 설명: 모든 일정 순회
        printf("%d. 제목: %s\n", i + 1, schedules[i].title);  // 설명: 번호와 제목 출력
        printf("   날짜: %s\n", schedules[i].date);           // 설명: 날짜 출력
        printf("   시간: %s\n", schedules[i].time);           // 설명: 시간 출력
        printf("   설명: %s\n", schedules[i].description);    // 설명: 설명 출력
        printf("------------------------------\n");          // 설명: 일정 간 구분선 출력
    }
}

void editSchedule(Schedule *schedules, int count) {  // 설명: 기존 일정을 수정하는 함수 정의
    int index;  // 설명: 수정할 일정 번호를 저장할 변수

    printf("\n[일정 수정]\n");  // 설명: 수정 시작 안내

    if (count == 0) {  // 설명: 저장된 일정이 없는지 검사
        printf("저장된 일정이 없습니다.\n");  // 설명: 일정 없음 메시지 출력
        return;  // 설명: 함수 종료
    }

    listSchedules(schedules, count);  // 설명: 현재 일정 목록을 먼저 보여 줌
    index = readInt("수정할 일정 번호를 입력하세요: ");  // 설명: 수정할 일정 번호 입력받기

    if (index < 1 || index > count) {  // 설명: 번호가 유효 범위인지 검사
        printf("유효하지 않은 번호입니다.\n");  // 설명: 잘못된 번호 안내
        return;  // 설명: 함수 종료
    }

    printf("새로운 일정 정보를 입력하세요.\n");  // 설명: 새 값 입력 안내
    inputSchedule(&schedules[index - 1]);  // 설명: 선택한 일정의 내용을 새 값으로 덮어씀
    printf("일정이 수정되었습니다.\n");  // 설명: 수정 완료 메시지 출력
}

void deleteSchedule(Schedule **schedules, int *count) {  // 설명: 일정을 삭제하는 함수 정의
    int index;       // 설명: 삭제할 일정 번호
    int i;           // 설명: 배열 이동용 반복 변수
    Schedule *temp;  // 설명: realloc 결과를 임시 저장할 포인터

    printf("\n[일정 삭제]\n");  // 설명: 삭제 시작 안내

    if (*count == 0) {  // 설명: 저장된 일정이 없는지 검사
        printf("저장된 일정이 없습니다.\n");  // 설명: 일정 없음 메시지 출력
        return;  // 설명: 함수 종료
    }

    listSchedules(*schedules, *count);  // 설명: 현재 일정 목록을 먼저 보여 줌
    index = readInt("삭제할 일정 번호를 입력하세요: ");  // 설명: 삭제할 번호 입력받기

    if (index < 1 || index > *count) {  // 설명: 번호가 유효한 범위인지 검사
        printf("유효하지 않은 번호입니다.\n");  // 설명: 잘못된 번호 안내
        return;  // 설명: 함수 종료
    }

    for (i = index - 1; i < *count - 1; i++) {  // 설명: 삭제 위치 뒤의 요소들을 앞으로 한 칸씩 당김
        (*schedules)[i] = (*schedules)[i + 1];   // 설명: 다음 일정을 현재 위치로 복사
    }

    if (*count - 1 == 0) {  // 설명: 삭제 후 일정이 0개가 되는 경우 처리
        free(*schedules);   // 설명: 배열 메모리 해제
        *schedules = NULL;  // 설명: 포인터를 NULL로 초기화
        *count = 0;         // 설명: 일정 개수를 0으로 갱신
        printf("일정이 삭제되었습니다.\n");  // 설명: 삭제 완료 메시지 출력
        return;  // 설명: 함수 종료
    }

    temp = (Schedule *)realloc(*schedules, (size_t)(*count - 1) * sizeof(Schedule));  // 설명: 배열 크기를 1개 줄임
    if (temp != NULL) {  // 설명: 재할당 성공 시에만 포인터 갱신
        *schedules = temp;  // 설명: 새 메모리 주소 반영
    }

    (*count)--;  // 설명: 일정 개수 1 감소
    printf("일정이 삭제되었습니다.\n");  // 설명: 삭제 완료 메시지 출력
}

```

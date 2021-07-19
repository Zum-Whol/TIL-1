# CLI 기본 명령어

***

## CLI와 GUI

- CLI(Command-Line Interface)
  - 명령어를 입력해 컴퓨터를 조작하는 방식
  - 리눅스 터미널은 키보드와 모니터 만으로 모든 작업 가능

- GUI(Graphical User Interface)
  - 화면을 통해 컴퓨터를 조작하는 방식
  - 여러가지 I/O 소스를 필요로 함

- 기타 용어
  - 입력(Input) : 컴퓨터를 조작하기 위해 필요한 동작
  - 입력소스(Input Source) : 입력을 담당하는 마우스와 키보드 등
  - 출력(Output) : 입력소스나 프로그램에 의한 결과를 사용자가 인식할 수 있도록 하는 일
  - 출력소스(Output Source) : 출력을 담당하는 모니터와 스피커 등
  - 아이오(I/O) : 컴퓨터를 조작하기 위한 입력과 출력
  - 프롬프트(prompt) : 키보드 입력을 확인하고 편집할 수 있는 한 줄의 공간

***

## 기본적인 CLI 명령어
- pwd: 현재 위치를 확인하는 명령어
- ls: 폴더나 파일의 목록을 출력하는 명령어 (옵션 : -l, -a, -la)
- open (macOS), nautilus (Ubuntu) : 현재 폴더를 파일 탐색기로 여는 명령어
- cd: 폴더에 진입하는 명령어
- mkdir: 새로운 폴더를 생성하는 명령어
- touch : 새로운 파일을 생성하는 명령어
- cat : 파일의 내용을 터미널에 출력하는 명령어
- rm : 폴더나 파일을 삭제하는 명령어 (폴더의 경우 옵션 : -rf)
- cp : 폴더나 파일을 복사하는 명령어 (폴더의 경우 옵션 : -rf)
- mv : 폴더나 파일의 위치를 이동하거나, 이름을 변경하는 명령어
- sudo: 관리자 권한
- clear : 터미널 지우기
- code . : VS Code 실행됨 (.은 현재 폴더에서 VS Code 실행)
- exit : 터미널 종료 (창을 닫는 것과 달리, 브라우저로 치면 탭을 닫는 개념)

- 띄어쓰기는 백슬래시로 표시
- 탭(tab) : 자동완성 기능 활용 가능

### 1. 경로 정보
- / : 루트 디렉토리 (절대 경로의 시작)
- . : 현재 디렉토리 (상대 경로의 시작)
- ~ : 홈 디렉토리

### 2. 조회와 이동 명령어
- pwd (print working directory)
  - 기능 : 현재 위치 확인
  - 문법 : ```pwd```

- ls (list)
  - 기능 : 특정 폴더에 포함된 파일이나 폴더 확인하기
  - 문법 : ```ls```

- ls의 명령어 옵션 l과 a
  - ```ls -a``` : 숨어있는 폴더와 파일을 모두 출력
  - ```ls -l``` : 파일의 포맷 전부 표현
  - ```ls -al``` 또는 ```ls -la``` : 두 가지 옵션을 모두 활용

- open
  - 기능 : 명령어를 이용해 폴더를 GUI의 탐색기로 실행하기 
  - 문법 : ```open .``` - 현재 위치를 GUI로 실행

- cd (change directory)
  - 기능 : 폴더에 진입하기 (프롬프트상으로 사용하는 폴더를 다른 폴더로 변경)
  - 문법 : ```cd 폴더명```
  - 상위폴더 이동 : ```cd ..```

### 3. 파일/폴더의 생성, 삭제, 복사, 이동 명령어
- mkdir (make directories)
  - 기능 : 새로운 폴더 생성
  - 문법 : ```mkdir 폴더명```

- touch
  - 기능 : 새로운 파일 생성하기
  - 문법 : ```touch 파일명```

- cat
  - 기능 : 파일의 전체 내용을 터미널에 출력
  - 문법 : ```cat 파일명```

- cat 대신 사용하는 명령어
  - 기능 : 파일의 전체가 아닌 부분만 열랍할 때 사용
  - 문법 : ```head/tail/more/less 파일명```

- rm (remove)
  - 기능 : 파일 삭제
  - 문법 : ```rm 파일명```

- rm의 명령어 옵션 r과 f
  - 기능 : 폴더 삭제
  - 문법 : ```rm -rf 파일명```
  - 설명 : rf 옵션을 사용해여 폴더 삭제가 가능 (r:recursive, f:force)

- cp (copy)
  - 기능 : 파일을 복사
  - 문법 : ```cp 원본파일 변경할파일명```

- cp의 명령어 옵션 r과 f
  - 기능 : 폴더를 복사
  - 문법 : ```cp -rf 원본폴더명 변경할폴더명```

- mv (move)
  - 기능1 : 폴더 또는 파일 이동
  - 문법 : ```mv 파일명/폴더명 도착폴더명```

  - 기능2 : 폴더명 또는 파일명 변경
  - 문법 : ```mv 파일명/폴더명 변경할이름```


### 4. 기타 링크
- 리눅스 기본 명령어 링크 : http://www.incodom.kr/Linux/%EA%B8%B0%EB%B3%B8%EB%AA%85%EB%A0%B9%EC%96%B4
- 파일, 디렉토리 조작을 위한 기본 명령어 링크 : https://www.44bits.io/ko/post/linux-and-mac-command-line-survival-guide-for-beginner#%ED%8C%8C%EC%9D%BC-%EB%94%94%EB%A0%89%ED%84%B0%EB%A6%AC-%EC%A1%B0%EC%9E%91%EC%9D%84-%EC%9C%84%ED%95%9C-%EA%B8%B0%EB%B3%B8-%EB%AA%85%EB%A0%B9%EC%96%B4%EB%93%A4
- 각 명령어에 포함된 옵션 관련 링크 : https://www.44bits.io/ko/post/linux-and-mac-command-line-survival-guide-for-beginner#%ED%97%AC%ED%94%84-%EC%98%B5%EC%85%98-h-help%EC%9C%BC%EB%A1%9C-%EC%82%AC%EC%9A%A9%EB%B2%95-%EC%B6%9C%EB%A0%A5%ED%95%98%EA%B8%B0



### 관리자 권한과 경로
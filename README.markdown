# 01 Foundation

### Introduction
![001.png](https://github.com/BaeMinCheon/game-engine-architecture-preview-kor/blob/master/image/001.png)
1. 게임 팀에서의 각 역할군이 수행하는 업무 내용
    - 프로그래머 아티스트 기획자 등
2. 게임 장르와 종류에 대한 소개
    - 리얼타임 프로그램으로서의 게임이 가지는 특징
3. 게임엔진이라는 개념과 그 역할
    - 게임 구성요소들을 분할하는 이유와 장점
    - 여러 게임들이 코드 재사용을 위해 도입
4. 게임 장르마다의 게임엔진 차이점
    - FPS 격투게임 레이싱게임 RTS MMORPG 등에서의 차이점
5. 게임엔진들에 대한 조사
    - Unreal Source Frostbite 등 엔진들의 특징
6. 게임엔진의 구조와 고려사항들
    - 하드웨어 드라이버 운영체제 등과의 관계
    - Core Resource Rendering 등 게임엔진을 나누는 기준
    - 이후에 배우게 될 내용들에 대한 간략한 소개 느낌
7. 게임애셋을 만드는 도구와 애셋을 사용하는 파이프라인
    - Maya 3DSMAX Photoshop 등의 애셋도구들에 대한 소개
    - 게임에 이러한 애셋을 어떻게 적용하는지에 대한 소개

### Tools of the Trade
![002.png](https://github.com/BaeMinCheon/game-engine-architecture-preview-kor/blob/master/image/002.png)
![003.png](https://github.com/BaeMinCheon/game-engine-architecture-preview-kor/blob/master/image/003.png)
1. 버전 컨트롤을 하는 이유와 버전 컨트롤 시스템의 종류들
    - SVN Git Perforce 등의 시스템에 대한 소개
    - SVN을 자신의 프로젝트에 적용하는 방법
2. 개발에 사용할 IDE에 대한 소개
    - 비주얼스튜디오를 IDE로 사용할 것이며, 이는 컴파일러와 링커를 포함함
    - 소스파일 헤더파일 DLL파일 등에 대한 소개
    - 프로젝트파일과 솔루션파일 설정법에 대한 소개
    - 여러 가지 디버깅 방법에 대한 소개
3. 코드를 최적화하기 위해 프로파일러를 사용
    - 크게 두 종류의 프로파일러로 분류됨
4. 메모리 누수와 이를 감지하기 위한 도구
    - 자신의 프로그램에서 메모리 누수를 `Purify` 등의 프로그램으로 분석할 수 있음
5. 배워두면 좋을 만한 프로그램들
    - `difference tool`
    - `3-way merge tool`
    - `hex editor`

### Fundamentals of Software Engineering for Games
![004.png](https://github.com/BaeMinCheon/game-engine-architecture-preview-kor/blob/master/image/004.png)
1. CPP와 OOP에 대한 개념을 짚고 넘어가기
    - 클래스와 객체 그리고 다형성 등의 개념에 대한 설명
    - 싱글톤을 비롯한 게임프로그래밍에서 사용되는 디자인패턴에 대한 소개
    - CPP의 각 표준마다의 특징과 CPP 공부에 추천하는 도서들
2. 에러의 종류와 이를 어떻게 다뤄야하는가
    - 에러를 어떤 방식으로 처리하는 것이 좋은가에 대한 철학(?) 설명
    - 에러 감지와 이를 처리하는 방법에 대한 예시
    - `std::except` 와 `assert()` 등을 사용하는 방법
3. 데이터 또는 자료형을 코드로 다룰 때 주의점
    - 정수와 소수를 컴퓨터에서 어떻게 표현하는지에 대한 설명
    - 멀티바이트 자료형을 처리하는 방법과 엔디언 변환법
    - CPP에서 자료형을 선언하고 정의할 때의 주의점
    - CPP의 메모리 레이아웃과 프로그램 스택의 구조
    - 클래스를 사용할 때의 CPP 메모리 레이아웃
4. 컴퓨터 구조 기초
    - 컴퓨터 구조에 대한 간단한 설명
    - CPU를 비롯한 컴퓨터 구성요소에 대한 설명
    - 기계어와 어셈블리어에 대한 설명
5. 메모리와 캐시의 구조와 어드레싱 방법
    - 메모리 매핑 방법과 비디오 램 및 가상 메모리에 대한 설명
    - 페이징 방법과 `Page Fault` 및 `TLB` 에 대한 설명
    - 캐시 지역성과 계층성 그리고 어드레싱 방법에 대한 설명

### Parallelism and Concurrent Programming
![005.png](https://github.com/BaeMinCheon/game-engine-architecture-preview-kor/blob/master/image/005.png)
1. 동시성과 병렬성에 대한 정의
    - 동시성은 복수 개의 연산이 동시에 실행되는 것
    - 병렬성은 복수 개의 하드웨어가 동시에 작동하는 것
    - 명시적이냐 암묵적이냐에 따른 병렬성
    - 태스크 단위냐 데이터 단위냐에 따른 병렬성
    - `SIMD` 를 비롯한 병렬성의 분류들에 대한 설명
2. 암묵적 병렬성을 CPU가 구현하는 방법
    - CPU의 파이프라이닝에 대한 자세한 설명
    - 파이프라이닝 과정에서 분기문이 주는 영향 및 해결책
    - CPU의 슈퍼스칼라에 대한 설명
    - 길이가 긴 명령어 `VLIW` 의 병렬처리
3. 명시적 병렬성을 CPU가 구현하는 방법
    - 멀티코어 CPU와 하이퍼스레딩에 대한 소개
    - CPU 자체를 묶어 병렬성을 달성하는 방법들
4. 스레드 조작을 위한 운영체제 배경지식
    - 운영체제 계층 및 커널에 대한 소개
    - 인터럽트와 커널함수에 대한 소개
    - 프로세스와 프로세스 실행되는 과정을 설명
    - 스레드와 CPP에서의 스레드 사용법에 대한 설명
5. 동시성을 구현하기 위한 배경지식
    - `Race Condition` 문제점에 대한 소개와 그 예시
    - 원자성을 갖는 연산을 사용한 해결책
6. 스레드를 동기화하는 방법
    - 스레드를 동기화하는 기법 `Mutex` 와 `POSIX` 에 대한 소개
    - 윈도우즈 내 CPP에서의 `Mutex` 및 `POSIX` 사용법
    - CPP에서 세마포어를 구현하고 사용하는 방법
7. 락 사용시의 문제점과 해결책
    - 교착상태에 대한 설명과 그 예시
    - 교착상태 해결책과 기아상태에 대한 소개
    - 철학자의 저녁식사 문제를 통한 교착상태 해결예시
8. 동시성 유지를 위한 조언들
    - 동시성 구현 도중 직면하는 문제들을 해결하기 위한 기법들
9. 락 없이 동시성 구현하기
    - 와 ;; 이건 뭔소린지 모르겠음 ㅋㅋ
10. SIMD
    - ???
11. GPGPU에 대한 소개
    - CUDA 프로그래밍으로 데이터 병렬처리를 수행하는 예시
    - GPU의 스레드와 스레드를 묶은 단위인 `warp` 에 대한 소개
    - SIMD에서 SIMT로 변환하는 과정에 대한 소개

### 3D Math for Games
![006.png](https://github.com/BaeMinCheon/game-engine-architecture-preview-kor/blob/master/image/006.png)
1. 2D에서의 해결책 중 일부는 3D에서도 유효함
2. 벡터와 기하학에 대한 설명
3. 행렬과 행렬을 사용한 3D 위상변화
    - SRT에 대한 행렬 연산 소개
    - 물체좌표계와 월드좌표계에 대한 소개
    - 뷰스페이스로 화면에 표현하는 방법 설명
4. 사원수를 활용한 회전
    - 사원수를 사용하는 이유와 그 개념
    - 사원수를 사용하는 방법과 그 구현
5. 회전을 표현하는 데에 사용되는 여러 방법들
    - 오일러 회전의 한계점과 해결책으로 사원수를 사용
    - SRT 행렬을 만들어 한 번의 행렬곱으로 크기회전이동을 적용
6. 그 외 기하학 구조체들
    - `line` `plane` `sphere`
    - `cude : OBB, AABB` `frustum` ...etc
7. 난수 생성에 사용하는 알고리듬

---

# 02 Low Level Engine Systems

### Engine Support Systems
![007.png](https://github.com/BaeMinCheon/game-engine-architecture-preview-kor/blob/master/image/007.png)
1. 시스템의 생성과 소멸 및 그 설계
    - 엔진시스템간의 관계에 따른 생성자과 소멸자 구성
    - 싱글톤 패턴에 대한 소개 및 그 구현
2. 메모리를 관리하는 방법
    - 메모리 동적할당의 비용 강조
    - 메모리 사용을 최적화하여 이 비용들을 감소시키는 기법들
    - 메모리 할당과정에서 발생하는 파편화에 대한 소개와 해결책
3. 자료구조에 대한 전반적인 요약
    - `array` `list` `stack` 등의 일반적인 자료구조 소개
    - 일반적인 자료구조들이 가지는 함수들을 소개
    - CPP의 `iterator` 에 대한 소개와 사용법
    - 알고리듬 복잡도 표기 `O(n)` 에 대한 소개
    - 사용자정의 컨테이너 만들시의 주의점과 STL 소개
    - 해시테이블에 대한 설명과 그 구현
4. `std::string`
    - `std::string` 의 한계점과 해결책들
    - 현지화를 위해 알아야할 유니코드에 대한 설명
    - 여러 상황에서 유니코드를 사용할 때 알아야할 것들
5. 설정값 관리
    - 게임 또는 엔진에 필요한 설정값들을 읽고 쓰는 방법 소개
    - 글로벌 설정값과 유저별 설정값을 구분하는 개념

### Resources and the File System
![008.png](https://github.com/BaeMinCheon/game-engine-architecture-preview-kor/blob/master/image/008.png)
1. 다양한 종류의 파일을 다루는 게임 특성을 기반으로 하는 파일시스템
    - 플랫폼마다의 파일 주소 저장법의 차이점
    - 파일입출력을 위해 사용하는 함수들에 대한 소개
    - 파일입출력에서의 동기 또는 비동기
2. 다양한 종류의 파일들을 조작하기 위한 리소스매니저
    - 게임의 규모가 커짐에 따라 애셋들을 체계적으로 관리해야함
    - 애셋들에 대한 버전컨트롤시스템도 일종의 리소스매니저로 봄
    - 애셋들을 구조화하기 위한 데이터베이스 사용 예시
    - 빌드과정에서 애셋에 의존하는 경우에 대한 소개
    - 런타임리소스매니저의 역할과 그 구성에 대한 소개

### The Game Loop and Real Time Simulation
![009.png](https://github.com/BaeMinCheon/game-engine-architecture-preview-kor/blob/master/image/009.png)
1. 렌더링 과정에 대한 소개
    - 과거 2D 그래픽이 주류였던 시기의 GUI 출력 방법
    - 3D 그래픽이 구성되는 간략한 과정과 대표적인 구조
2. 게임의 전체적인 과정에 대한 소개
    - 렌더링루프와 동기화하는 요소와 그렇지않은 요소들
    - 게임루프는 게임을 구성하는 하위시스템들의 총합
    - `Pong` 을 예시로 하는 게임루프에 대한 설명
3. 게임루프 구조를 어떤 방식으로 만들지에 대해서
    - 윈도우메시지 스타일 외 게임루프 스타일들
4. 타임라인을 어떻게 결정할 것인가에 대해서
    - CPU를 기반으로 할 것인지 또는 게임세계 기반인지
    - 글로벌타임라인과 로컬타임라인의 구분
5. 시간을 측정하는 법과 사용하는 법
    - 프레임레이트와 타임델타 개념에 대한 소개
    - 왜 타임델타를 사용해야하는지에 대한 소개
    - 스크린테어링과 수직동기화에 대한 소개
    - 고해상도 타이머를 사용한 보다 더 정확한 시간측정
    - CPU기반 타이머 사용시 디버깅에서 주의할 점
6. 게임루프가 멀티프로세싱이 가능하도록 만들기
    - 게임루프에서 처리할 작업을 어떻게 분할할 것인가
    - 게임의 하위시스템마다 스레드를 할당하기
    - `Scatter & Gather` 방식으로 분할하기
    - `Job Systems` 방식으로 분할하기

### Human Interface Devices
![010.png](https://github.com/BaeMinCheon/game-engine-architecture-preview-kor/blob/master/image/010.png)
1. 인터페이스 기기들의 역사와 그 종류
    - 조이스틱을 비롯한 여러 가지 컨트롤러에 대한 소개
2. 인터페이스 기기들을 처리하는 방법
    - 폴링과 인터럽트에 대한 소개
    - 무선 인터페이스 기기의 특징
3. 입력에 따른 인터페이스 기기의 특징
    - 입력의 가짓수에 따른 기기 분류
    - 이산적이냐 연속적이냐 상대적이냐 가속적이냐 등
4. 인터페이스 기기의 출력 분류
    - 단발성 진동이냐 아니냐 또는 음성으로 출력되느냐 등
5. 게임엔진이 인터페이스 기기를 처리하는 방법
    - 대부분의 경우 입력을 그대로 처리하지 않는다
    - `dead zone` 을 걸러내기 위한 전처리 등을 수행
    - 동시에 여러 개의 입력들 또는 기기들을 처리하는 방법
    - 멀티플랫폼을 지원하는 인터페이스 시스템 만들기
6. 인터페이스 기기 처리의 실제
    - 하드웨어에 의존적이라 이론만으로는 힘들다
    - 플레이어를 만족시키는 공학이기 때문에 실험이 많이 요구된다

### Tools for Debugging and Development
![011.png](https://github.com/BaeMinCheon/game-engine-architecture-preview-kor/blob/master/image/011.png)
![012.png](https://github.com/BaeMinCheon/game-engine-architecture-preview-kor/blob/master/image/012.png)
1. 로깅이 필요한 이유와 이를 사용한 디버깅
    - 게임에서 `printf()` 방식 디버깅이 효과적인 이유
    - 지나치게 많은 로깅을 방지하기 위한 단계별 조절
    - 로깅 또는 크래쉬 내용을 파일로 출력하기
2. 디버깅을 위해 화면에 출력하는 기법
    - 디버깅을 위해 선 또는 면 등의 도형을 출력하는 개념
    - `last of us` 의 디버깅 API를 통한 예시 설명
    - 디버깅 API를 만들기 위한 설계 및 고려사항
3. 디버깅을 위한 인게임 메뉴
    - 소스코드 수정 등의 별도 작업 없이 게임설정 변경가능
    - 디버깅 및 생산성을 위한 인게임 메뉴 사용예시
4. 디버깅을 위한 인게임 콘솔
    - 좀 더 다양한 설정들을 조정할 수 있다
    - 이와 관련된 내용은 `16.9` 에서 이어진다
5. 디버깅을 위한 캠 기법
    - 메뉴 또는 콘솔로 게임이 중지되었을 때 캠을 움직일 필요 있음
    - 게임이 느린 속도로 진행되도록 하는 것도 디버깅에 효과적
6. 디버깅을 위한 꼼수들
    - 캐릭터를 무적으로 만드는 등의 극한조건을 만들기
7. 디버깅을 위한 캡쳐
    - 디버깅을 위한 요소를 포함하여 스크린샷을 찍을 수 있다
    - 이 경우 나중에 해제할 수 있도록 만들어야한다
    - PS4의 실시간 영상캡쳐에 대한 소개 및 디버깅으로의 활용
8. 성능향상을 위한 프로파일링
    - 게임의 프레임수를 늘리기 위한 부하 측정 필요성
    - 프로파일링을 구현하는 여러 가지 방법들
    - 엑셀 등의 테이블로 출력하는 것도 좋다
9. 성능향상을 위한 메모리검사
    - 하드웨어 자원을 많이 사용하는 게임 특성상 메모리 관리가 중요
    - 게임 같은 대규모 프로젝트에서의 메모리 관리 어려움
    - 메모리관리를 위해 시도하는 방법에 대한 소개

---

# 03 Graphics, Motion and Sound

### The Rendering Engine
![013.png](https://github.com/BaeMinCheon/game-engine-architecture-preview-kor/blob/master/image/013.png)
1. d
    - d
2. d
    - d
3. d
    - d
4. d
    - d
5. d
    - d

### Animation Systems
![014.png](https://github.com/BaeMinCheon/game-engine-architecture-preview-kor/blob/master/image/014.png)
1. d
    - d
2. d
    - d
3. d
    - d
4. d
    - d
5. d
    - d
6. d
    - d
7. d
    - d
8. d
    - d
9. d
    - d
10. d
    - d
11. d
    - d

### Collision and Rigid Body Dynamics
![015.png](https://github.com/BaeMinCheon/game-engine-architecture-preview-kor/blob/master/image/015.png)
1. d
    - d
2. d
    - d
3. d
    - d
4. d
    - d
5. d
    - d
6. d
    - d

### Audio
![016.png](https://github.com/BaeMinCheon/game-engine-architecture-preview-kor/blob/master/image/016.png)
1. d
    - d
2. d
    - d
3. d
    - d
4. d
    - d
5. d
    - d
6. d
    - d

---

# 04 Gameplay

### Introduction to Gameplay Systems
![017.png](https://github.com/BaeMinCheon/game-engine-architecture-preview-kor/blob/master/image/017.png)
1. d
    - d
2. d
    - d
3. d
    - d
4. d
    - d

### Runtime Gameplay Foundation Systems
![018.png](https://github.com/BaeMinCheon/game-engine-architecture-preview-kor/blob/master/image/018.png)
1. d
    - d
2. d
    - d
3. d
    - d
4. d
    - d
5. d
    - d
6. d
    - d
7. d
    - d
8. d
    - d
9. d
    - d
10. d
    - d

---

# 05 Conclusion

### You Mean There's More ?
![019.png](https://github.com/BaeMinCheon/game-engine-architecture-preview-kor/blob/master/image/019.png)
1. d
    - d
2. d
    - d

---
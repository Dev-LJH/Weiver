# 🎬 **Weiver**
### 🎬 Weiver는 뮤지컬 정보 제공, 후기 공유 커뮤니티입니다.
![logo](https://github.com/Weiver-project/Weiver/assets/116157924/af5207db-9c59-4600-a519-c42211897935)

<br>

## ✨Overview
뮤지컬 정보, 현재 진행중인 뮤지컬, 배우가 참여한 뮤지컬과 같은 정보를 얻을 수 있고

커뮤니티를 통해 후기를 공유하고 다른 사용자와 의견의 주고 나눌 수 있습니다.

**📆 프로젝트 기간 : 2023.06.15 ~ 2023.07.25**
 <hr style="border: 0px;">
<br>

## 🙂 업무분배 
|**이름**|**업무**|
|:---:|:---:|
|**이석현**|playDB 배우 정보 크롤링, Youtube API, 관리자 페이지 기능 담당|
|**정찬영**|playDB 뮤지컬 정보 크롤링, 뮤지컬 관련 기능, 배포 담당|
|**곽유섭**|마이 페이지(구독, 유저, 문의) 기능 담당, 관리자 페이지 기능 담당|
|**김현수**|커뮤니티 페이지(게시글, 상세게시글, 좋아요) 기능 담당, UI 디테일 담당|
|**이종형**|카카오 로그인 API, 유저 등록, 로그인 기능, 배우 정보 기능 담당|

### 주요기능
뮤지컬 정보 조회 : 검색어, 뮤지컬 포스터 클릭 시 해당 뮤지컬의 정보(공연 기간, 출연진 정보 등)를 조회합니다.
배우 정보 조회 : 배우 사진을 클릭 시 해당 배우가 참여한 뮤지컬을 조회합니다.
리뷰 작성 : 내가 본 뮤지컬을 검색하여 해당 뮤지컬에 대한 리뷰를 작성할 수 있습니다.
잡담(일반 게시글) 작성 : 

### 개발환경 :

## 서비스 아키텍처
![image](https://github.com/Weiver-project/Weiver/assets/76997735/6e881153-f943-4c2f-a562-c80dda027428)

## ERD
![ERD](https://github.com/Weiver-project/Weiver/assets/78299214/d9689a4f-1e36-499f-beb1-9a8d57292528)
## 구현 결과
### 뮤지컬   
- [X] **메인 페이지**   
+ 인기 뮤지컬: '봤어요' 클릭이 가장 많은 뮤지컬 상위 3개 출력   
+ 커뮤니티 인기글: '조회수' 기준 상위 게시글 9개 출력   
+ 추천 배우: 랜덤으로 배우 프로필 사진과 출연작 출력, 클릭 시 배우 상세 페이지 이동, 새로고침 시 배우 정보 변동   
+ 공연 중인 뮤지컬: 공연 기간 기준 현재 공연 중인 뮤지컬 리스트 출력
   <p>
![뮤지컬 메인 페이지](https://github.com/Weiver-project/Weiver/assets/81962257/fbf2cc82-c97d-4032-8195-ba350ce451c4)
     </p>

- [X] **상세 페이지**   
+ 뮤지컬 기본 정보 조회   
+ '찜하기', '봤어요' 클릭   
+ 출연 배우 정보 조회   
+ Youtube API 통한 유튜브 클립 출력
     <p>    
![뮤지컬 상세 페이지](https://github.com/Weiver-project/Weiver/assets/81962257/2a88980a-3075-4e37-9507-e85e8976f389)
     </p>
   
### 커뮤니티  
- [X] **메인 페이지**   
+ 커뮤니티 인기글: '조회수' 기준 상위 게시글 9개 출력   
+ 게시글: 카테고리(리뷰, 잡담)에 따라 게시글 구분하여 출력   
+ 로그인 시, 유저 간략 정보 측면 nav바에 출력   
     <p>    
![커뮤니티 메인 페이지](https://github.com/Weiver-project/Weiver/assets/81962257/f6d4e069-5717-4d00-957b-99b3daa58e7d)
     </p>

- [X] **상세 페이지**   
+ 게시글 정보 상세 조회   
+ 댓글, 대댓글 작성   
+ 본인 작성에 한하여 게시글, 댓글, 대댓글 수정 및 삭제 가능   
     <p>    
![게시글 상세 페이지](https://github.com/Weiver-project/Weiver/assets/81962257/cb916d13-dbd6-4d7e-a8f8-6ef17936db47)
     </p>

- [X] **글 작성 페이지**   
+ 글 카테고리(잡담, 리뷰) 선택 가능   
+ 리뷰 선택 시, 뮤지컬 정보 연동   
+ 이미지 첨부 가능   
     <p>    
![제목 없는 동영상](https://github.com/Weiver-project/Weiver/assets/81962257/6fb59d44-8cba-4805-aedc-b767fa8a2023)
     </p>

    

## 힘들었던 점
세 번의 DB 변경
![image](https://github.com/Weiver-project/Weiver/assets/129250941/670269c8-1450-4acd-a550-69c1d3c4f010)
1. 불규칙적인 KOPIS API 뮤지컬 정보와 PLAY DB 배우 정보와의 매핑 과정을 거쳐서 각각의 테이블에 저장하는 방법보다 한 번에 하나의 컬렉션에 전부 저장하는 방식이 조회 속도와 삽입 속도 측면에서 보다 더 효과적일 것이라고 생각되어 MongoDB를 사용
2. 뮤지컬과 배우를 제외한 나머지 데이터들은 정형화되어있고 관계성이 높기 때문에 Oracle DB를 도입하여 두 가지 데이터베이스를 사용
3. KOPIS API를 사용했을 때 PLAY DB 배우 정보와 서로 매핑되는 비율이 444건 중 25건인 5%정도로 매우 낮아 KOPIS API를 포기하고 PLAY DB에서 뮤지컬 정보도 같이 크롤링하는 방식을 사용 -> 뮤지컬 데이터도 정형화되었고 배우 정보와 동일한 페이지에서 데이터를 가져옴 -> 매핑 방식이 이전보다 수월해져 전체 DB를 Oracle로 사용

## 트러블 슈팅
크롤링 시 TimeOutException
1. 크롤링 시 Timeout Option을 주는 방법과 Thread.sleep()을 주는 방식을 사용했지만 해결이 되지 않음
2. 크롤링으로 데이터를 가져오는 과정과 DB에 데이터를 저장하는 과정이 같은 텀에서 실행되는 것이 리소스를 많이 잡아먹는다는 의문
3. 데이터를 메모리에 전부 저장한 다음 DB에 일괄 저장하는 방식을 사용 (Exception 발생 시기가 뒤로 늦춰졌을 뿐 여전히 발생)
4. 버퍼와 같이 일정량의 데이터를 저장한 후 비워주는 방식을 사용하여 해결
```
/*뮤지컬 상세 페이지에서 뮤지컬 정보 저장*/
@SneakyThrows
public void saveAllMusical(List<String> musicalIds){
  List<Musical> musicals = new ArrayList<>();
    
    for(int i =0; i < musicalIds.size(); i++){
        //뮤지컬 1개에 대한 데이터 크롤링
        Musical musical = getMusical(musicalIds.get(i));
        musicals.add(musical);
        log.info(i + "번 MUSICAL(" + musicalIds.get(i) + ") 저장: " + musical);

        // 데이터를 1000개씩 저장
        if(i != 0 && i % 1000 == 0){
          // musical 저장
          musicalRepository.saveAll(musicals);

          // 새로운 MusicalId를 채우기 위해 기존 리스트 초기화
          musicals.clear();
        }
    }
```

## 회고


## 수상내역

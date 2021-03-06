# 닌텐도 스위치 클리너 및 빌더 (NSC_Builder)
https://github.com/julesontheroad/NSC_BUILDER 

## 1. 설명

NSC_Builder는 xci_builder 및 Nut_Batch_Cleaner를 계속하는 병합 된 프로젝트입니다.

NSC_Builder는 Blawar의 nut.py와 Luca Fraga의 hacbuild를 기반으로하며, 제목-권리 수정 기능을 조정하면서 CDN 기반 기능을 제거하고 추가 기능을 추가하여 "squirrel"을 제공합니다. 파일 관리. 버전 v0.8에서 프로그램은 xci 생성을 위해 hacbuild에 의존하지 않고 다람쥐와의 더 나은 통합을 위해 새로운 코드가 작성되었습니다.
버전 v0.8에서 프로그램은 xci 생성을 위해 hacbuild에 의존하지 않고 다람쥐와의 더 나은 통합을 위해 새로운 코드가 작성되었습니다.

다람쥐는 곧 새로운 github 저장소를 얻게 될 것이고 베타 v0.8에서 NSCB를 위한 exe로 패킹 될 것입니다. NSCB 메인 저장소에서 오래된 다람쥐 코드를 볼 수 있으며, 코드를 정리한 후 NSCB 베타 단계가 끝나면 새로운 코드가 저장소에 게시됩니다.

## 2. 소유권 삭제의 의미는 무엇입니까?
nsp 파일에서 titlerights 암호화를 제거하면 티켓을 필요로하지 않고 게임을 설치할 수 있으므로 콘솔에서 추적 가능한 공간이 작아지므로 닌텐도에 원격 측정 데이터를 보낼 필요가 없습니다.
또한 외부에서 티켓을 설치하지 못하게하는 nsp에서 xci 파일로의 변환에 도움이됩니다.

## 3. 이 프로그램으로 무엇을 할 수 있습니까?

현재 버전의 프로그램을 사용하면 다음을 수행할 수 있습니다:
1.- 멀티 컨텐트 xci 또는 nsp 파일 제작
2.- nsp 파일에서 titlerights 암호화를 지움.
3.- "파티션 업데이트" 없이 xci 파일을 빌드하여 스토리지 공간을 적게 차지
4.- 업데이트에서 델타 제거
5.- 다중 컨텐츠를 xci 또는 nsp 파일로 다시 분할
6.- xci와 nsp 사이의 콘텐츠 패킹 변경 
7.- 필요한 시스템 버전을 실제 게임 암호화로 낮춤
8.- 게임 해독에 필요한 마스터 키를 낮춤
9.- xci 및 nsp에서 실행 가능한 펌웨어, 게임 정보, nca 콘텐츠의 크기 등의 정보를 확인
10.- fat32와 호환되는 형식으로 xci 및 nsp 내용을 리팩
11.- 단일 및 다중 컨텐트 형식의 xci 파일 및 nsp 파일 대량 빌드
12.- nsp, xci 파일의 내용을 일치하도록 이름 바꾸기
13.- nsp, nsx, xci y nca 파일 확인
14.- 텍스트 형식의 정보 출력
15.- nsp 파일의 내용을 추출하고 xci 파일의 파티션을 보호
16.- 나중에 멀티 모드로 작업 설정
17.- 멀티 모드에서 based-titleid 기준으로 작업 분리

## 4. 일괄 처리 모드:

일괄 처리에는 두 가지 모드가 있습니다:

- 자동 모드: nsp 파일을 개별적으로 드래그하거나 일괄 처리를 통해 여러 파일이 있는 폴더를 자동 모드로 드래그합니다.

- 수동 모드: 배치를 두 번 클릭하면 처리할 파일 목록을 작성할 수 있습니다.

자동 모드의 동작은 수동 모드의 구성 메뉴를 통해 구성됩니까?

## 5. 수동 모드 옵션:

- 모드 0: 구성 모드. 프로그램이 자동 및 수동 모드에서 작동하는 방식 구성
- 모드 1: 개별 패킹. 파일 목록을 처리하고 개별적 압축
  * nsp\xci로 패킹
  * xci 파일 Supertrimm
  * xci 또는 nsp 파일의 이름 바꾸기
  * cnmt 오더로 nsp 파일을 다시 빌드하고 cnmt.xml을 추가
  * nsp, xci 파일 확인
- 모드 2: 멀티 패킹. 하나의 xci 또는 nsp 파일에 파일 목록 압축
  * basedid로 파일을 분리
  * 나중에 사용할 작업 설정
  * 이전 작업 처리
- 모드 3: 멀티 콘텐츠 분배기. 콘텐츠를 nsp 및 xci 파일로 분리
- 모드 4: 파일 정보. nsp 및 xci 파일에 대한 정보를 보고 내보냄
- 모드 5: 데이터베이스 모드. 대량 생산 정보 출력
- 모드 6: 고급 모드. 현재 xci\nsp에서 추출 (더 추가해야 함)
- L: 레거시 모드, 오래된 기능

## 6. 구성 모드:
### 자동 모드 옵션. (자동 모드에만 적용)
#### 리팩 구성
- NSP 
- XCI
- BOTH
#### 폴더 처리
- 폴더의 파일을 개별적으로 리팩 (단일 컨텐트 파일)
- 폴더의 파일을 함께 리팩 (다중 컨텐트 파일)
#### RSV 패치 구성
- 필요한 시스템 버전이 암호화보다 크다면 패치하십시오.
- 암호화보다 크면 필수 시스템 버전을 패치하지 마십시오.
#### 키생성 구성
- 파일이 가질 수 있는 최대 키 생성 (암호화)을 설정하십시오.
### 글로벌 옵션. (프로그램이 세계적으로 어떻게 작동하는지에 영향을 미침))
#### 텍스트 및 배경색
- cmd 창의 색상을 선택
#### 작업 폴더의 이름
- 작업 폴더의 이름 선택
#### 출력 폴더의 이름
- 출력 폴더의 이름과 위치 선택
#### 델타 파일 처리
- 델타 NCA 파일을 포장할지 여부 결정. 기본값은 false로 설정.
#### ZIP 구성
- 파일 정보를 저장하는 zip 파일 생성 선택. 기본값은 false로 설정.
#### 자동 종료 설정
- 작업을 완료 한 후 cmd 창이 닫히는지 선택.
#### 키 생성 프롬프트
- 수동 모드에서 RSV와 키 생성을 패치하라는 프롬프트를 보고 싶다면 선택.
#### 파일 스트림 버퍼
- 파일 스트림 작업을 위한 버퍼
#### 파일 FAT32 \ EXFAT 옵션
xci 또는 nsp를 fat32 호환 형식 또는 exfat 형식으로 패킹하십시오.
- 카드 포맷을 exfat로 변경 (기본값)
- SX OS 용 카드 포맷을 fat32로 변경 (xc0 및 ns0 파일)
- 모든 CFW에 대해 카드 포맷을 fat32로 변경 (보관 폴더)

#### 출력 파일 정리 방법
- 파일을 별도로 구성 (기본값)
- 콘텐츠로 설정된 폴더에서 파일 구성

## 7. 중요

이 프로그램은 nsp 및 xci 파일에서 가능한 최소 데이터를 수정하려고 시도합니다. 그 이유는 NCA 헤더에서 서명을 모두 무시하는 서명 패치가 필요하기 때문입니다. 이미 포함 된 펌웨어는 다음과 같습니다:
- SX OS
- ReiNX
https://github.com/Reisyukaku/ReiNX/releases
- RShadowhand의 스타터 팩 "Singularité"는 사전 구성된 분위기로 필요한 패치와 홈브류 시작을 포함하여 Hekate trough fusee 기본을 통해 자동 실행되도록 만들어졌습니다.
https://github.com/RShadowhand/singularite/releases
- kosmos의 경우 수정된 hekate의 hekate를 sigpatches가 추가된 것으로 바꿉니다:
https://github.com/Joonie86/hekate/releases

multi-nsp를 설치하려면 해당 설치 프로그램과 호환되는 설치 프로그램이 필요합니다. 보고된 호환 설치 프로그램은 다음과 같습니다.:
- SX OS rom-menu
- SX OS 설치 프로그램
- Blawar의 tinfoil:
https://github.com/digableinc/tinfoil
- Blawar의 lithium:
https://github.com/blawar/lithium

## 8. 요구사항 

- 윈도우 OS가 설치된 컴퓨터가 필요합니다.
- ztools 폴더에 keys_template.txt를 넣고 keys.txt로 이름을 바꿉니다.
  콘솔이 FW6.2면 당신은 Lockpick으로 전체 키셋을 얻을 수 있습니다.
  친구가 필요한 열쇠를 빌려 줄 수 있습니다.
  xci_header_key를 추가하려면 친구가 그것을 빌려줘야합니다.
  https://github.com/shchmue/Lockpick/releases

## 9. 제한사항 
- 8 개 이상의 게임으로 다중 컨텐츠 xci 파일을 만들 수는 없습니다. 수평으로 로딩할 때 오류가 발생합니다. 그것이 qlauncher 제한일지도 모른다라고 생각해서 그것은 그것은 테마 mods와 함께 작동하지만 INTRO는 그것을 테스트하지 않았습니다.
참고: 이는 "게임", 업데이트 및 dl car가 해당 제한사항을 지키지 않음을 의미합니다.
- 타이틀 권한 제거 dlcs는 6.0 이후의 일부 게임에 대한 불완전한 내용의 메시지 프롬프트를 제공합니다. 이 메시지는 건너 뛸 수 있으며 dlcs는 프롬프트에도 불구하고 정상적으로 작동합니다.

## 7. 감사와 크레딧

NSC_Builder는 다음을 기반으로합니다.

a.) Nut: 가장 재능있는 Switch sceners 중 하나 인 "blawar"의 작업 없이는 이 시점에서 이 모든 작업을 수행할 수 없습니다.
https://github.com/blawar/nut

b.) Hacbuild: xci repacking 함수는 LucaFraga가 만든 hacbuild 코드를 기반으로합니다.

- 오리지널 hacbuild: LucaFraga에 의한 https://github.com/LucaFraga/hacbuild)

- 나에 의해 수정된 hacbuild: https://github.com/julesontheroad/hacbuild

또한 아래의 사람들에게 감사합니다:

AnalogMan. 그는 splitNSP.py를 만들었고 Horizon 형식으로 분할된 nsp (분할된 xci 블록 크기와 다름) 및 필요한 폴더를 보관할 필요가 있는 블록 크기를 계산했습니다.
https://github.com/AnalogMan151/splitNSP/releases

MadScript77에게 그의 훌륭한 제안, 특히 배치의 프로파일 아이디어에 감사드립니다.

Liam과 0mn0이 항상 도움이 되었기 때문에 오래된 SH discord에 감사드립니다.

그들의 도움과 좋은 제안에 대해 evolved, Cinnabar, certain dragon에 감사드립니다.

XCI-Explorer의 제작자 StudentBlake에게 감사의 말을 전합니다. 그의 프로그램이 hacbuild에 대한 수정 항을 쉽게 찾을 수 있었기 때문입니다.

또한 gbatemp, elotrolado.net, discord의 내 친구들의 모든 회원에게 감사드립니다. ;)

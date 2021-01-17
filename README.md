# 𝐐𝐮𝐢𝐜𝐤𝐒𝐨𝐫𝐭𝐓𝐞𝐬𝐭

### 목차
1. <a href="#1">QuickSortTest.exe 사용법</a>
2. <a href="#2">result.txt 설명</a>
3. <a href="#3">QuickSortTest 프로젝트 사용법</a>
4. <a href="#4">makegraph_quicksorttest.py 사용법</a>

<a name="1"></a>
# QuickSortTest.exe 사용법

<img src="/img/consoleQuickSortTest.JPG">

- 해당 테스트를 사용한 레파지토리 글 링크는 [이곳](https://github.com/JooMal/ProblemSolving/tree/master/SortAlgorithm)입니다.

1. 레파지토리에 포함되어 있는 QuickSortTest.exe 파일을 다운로드받아 더블클릭하여 실행합니다.
2. 콘솔창에서 질의에 따라 원하는 값을 입력합니다.
  2.1. **START NUMBER OF ARRAY NODE** : 배열 요소의 시작 갯수를 입력합니다. 해당 갯수부터 사용자가 정하는 increment를 매 loop마다 증가하며 quick sort를 시행합니다. 배열 내부의 값은 0부터 배열길이 사이의 랜덤값으로 할당됩니다. 해당 갯수가 클 수록 프로그램의 iteration 당 실행 시간이 늘어나며, 테스트에 사용한 값은 10,000 입니다.  
  2.2. **NUMBER OF ITERATION** : 반복 횟수를 정합니다. 해당 횟수만큼 loop을 돌며 배열의 길이를 증가시키며 quick sort를 진행하게 되며, 테스트에 사용한 값은 1,000이며 너무 큰 값을 주면 사용자의 환경에 따라 프로그램이 강제로 종료될 수 있습니다.
  2.3. **INCREMENT PER ITERATION** : 매 iteration마다 증가시킬 배열의 길이를 정합니다. 초기 배열 길이가 1,000이고, increment가 100인 경우에는 1회차에는 1,000 길이의 랜덤 배열로 quick sort가 진행되며, 2회차에는 1,100 길이의 랜덤 배열로, 3회차에는 1,200 길이의 랜덤 배열로 시행됩니다. 테스트에 사용한 값은 100입니다.
3. 2의 과정을 통해 전역변수값을 설정하면, 매 iteration마다 직접 구현한 코드(Implement QuickSort)의 실행에 걸린 시간과 C++ Algorithm 헤더의 sort의 실행에 걸린 시간이 출력됩니다. 또한, 매 iteration마다 상단에 현재 배열의 길이를 출력해줍니다.
4. 모든 실행이 끝나면, quick sort가 종료되고 프로젝트 폴더 내에 결과값을 담은 `result.txt`가 생성됩니다.

<a name="2"></a>
# result.txt 설명
- `result.txt`는 매 iteration에 사용된 Array Length, Implement QuickSort의 실행시간, C++ Algorithm 헤더 sort함수 실행시간을 `,`으로 분리하여 담고 있습니다. 매 iteration의 끝에는 `\n`문자가 포함되어있습니다.
- 해당 파일은 프로젝트 폴더에 자동으로 추가됩니다. 만약 `result.txt`가 이미 있는 경우에는, 새로운 파일을 생성하기 위해 이전의 `result.txt`파일을 삭제해주어야합니다.

<a name="3"></a>
# QuickSortTest 프로젝트 설명

<img src="/img/vsQuickSort.JPG">

### QuickSortTest.exe에서 사용했던 사용자 입력값은 다음의 전역변수와 대응합니다.
1. START NUMBER OF ARRAY NODE == MAX_LEN == MAX_RAND
  - MAX_LEN은 초기 배열의 길이, MAX_RAND는 해당 배열에서 랜덤으로 생성될 요소값의 최댓값을 의미합니다.
2. NUMBER OF ITERATION == REP : 반복 횟수입니다.
3. INCREMENT PER ITERATION == INC : 매 iteration마다 증가시킬 배열의 길이입니다.

### `Print(int list[], int len)` 함수
- 배열의 내용을 출력해보기 위해 사용하는 Print 함수입니다. 파라미터로는 리스트의 이름과, 리스트의 길이를 입력합니다.

### `makeArr(int list[])` 함수
- 최대 MAX_RAND까지의 값을 갖는 랜덤한 값을 요소에 할당하며 배열을 만들어주는 함수입니다.

### `swap(int &a, int&b)` 함수
- 변수 a의 값과 b의 값을 바꾸어주는 함수입니다.

# QuickSortTest 프로젝트 사용법
- VisualStudio 2017 버전에서 구현되었습니다.
1. 레파지토리의 QuickSortTest 폴더를 다운받습니다.
2. 파일 > 열기 > 프로젝트/솔루션에서 다운받은 QuickSortTest 폴더를 연 후, `QuickSortTest.sln`을 더블클릭하여 열어줍니다.
3. VisualStudio 2017 기준 `F5`를 클릭하여 디버깅과 런을 진행할 수 있습니다.
4. 내용 수정 후 재빌드하기 원하는 경우, 빌드 > 솔루션 빌드 를 클릭하여 새로운 빌드파일을 만들 수 있습니다. 이 경우, 프로젝트 파일의 디버그 폴더에 생성되는 QuickSortTest.exe 파일을 새로운 빌드 파일이 덮어씌우게 됩니다.

<a name="4"></a>
# makegraph_quicksorttest.py 사용법
- 해당 파일은 Google Colab에서 작성되었으며, txt파일 입력을 위해 Google Colab 사용을 권장합니다.
1. 각 코드블럭은 `Ctrl`+`Enter`를 사용하여 실행할 수 있습니다. 첫 코드블럭을 선택하면, 다음과 같은 인증 문구가 만들어집니다.  

<img src="/img/googleAuth.JPG">

  1.1. Go to this URL in a browser 이후의 주소창을 클릭하여 인증창을 띄웁니다.  
  1.2. 구글 인증을 진행합니다.    
  1.3. 하단에 생성된 인증코드를 복사합니다. 오른쪽의 클립보드 복사 버튼을 클릭하면 보다 효율적으로 복사가 가능합니다.  
  1.4. 복사한 인증코드를 Enter your authorization code 하단의 여백칸에 입력 후 엔터를 치면 인증이 완료됩니다.  
2. 이전에 `QuickSortTest` 프로젝트를 시행하며 생성된 `result.txt`파일을 Google Drive 루트(=`/content/gdrive/My Drive/`)에서 `resData` 폴더를 생성한 후, 해당 폴더에 `result.txt`파일을 복사합니다. 반드시 `resData` 폴더여야하며, 폴더명을 바꾸고 싶을 경우에는 `with ... as file object`문의 파일 루트를 변경해주어야 합니다.  
3. 그래프 생성을 위해 맨 하단의 코드블럭까지 차례로 실행하면, 파싱을 통해 array에 데이터를 저장한 후 해당 데이터를 그래프로 변환할 수 있습니다. 만약 따로 파일로 저장하기 원할 경우에는 `savefig`을 사용하여 저장할 수 있습니다.  


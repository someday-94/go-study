## Composite Pattern

### Problem
B폴더 안에 b파일이 존재하는지 알아보고 싶다. 하지만, B폴더 안에는 A폴더도 c파일도 있다. 이처럼 폴더 안에 또 다른 폴더가 존재하고 그 폴더 안에 또 다른 폴더가 존재할 수 있다. 마치 트리 구조처럼되어 있다. 그렇다면,B폴더 안에 b파일이 존재하는지 알아보려고 모든 폴더를 직접 열어봐야 하나? 

### Solution
폴더와 파일을 하나의 인터페이스인 Component로 묶어서 Search라는 메소드를 정의해놓으면 내가 선택한 폴더의 Search 메소드만 실행하면 해당 폴더 내부의 모든 폴더와 파일의 Search 메소드가 마치 깊이우선탐색(DFS)처럼 작동하게 된다.
- React를 사용하기 전에는 Parcel이라는 빌드 도구를 사용할 예정
- 개발자들이 사용하는 자바스크립트의 버전이 다르기 때문에 Babel이라는 도구를 사용해서 옛날 버전의 자바스크립트를 사용할 수 있게 해준다. 
- code formater로 코드를 정리한다.(사람이 정리하는 게 X)
    - 특히, 협업할 때 사용
- Visual Studio Code Setting
    -> 사용자 설정: 전역으로 적용됨. 모든 프로젝트마다 적용.
    -> 작업 영역 설정: 프로젝트마다 다르게 설정.
    - 왠만하면 작업 영역 설정으로 하기
- `.gitignore`에 git 저장소에 올라가면 안되는 파일들의 목록을 적음
    - ex) visualCode 설정 파일들은 올리면 X. 
    - ex)`.vscode/`라고 넣으면 `.vscode`라는 폴더가 무시됨.(git에 올리지 X)'
- `package.json`
- scss에서는 앞에 $를 붙여서 css에서 변수를 사용할 수 있다.
- npm start를 해서 사용하는 서버는, 개발용 빌드 서버임.
- 스크립트는 body태그 가장 아래에 써주는 게 관례이다. 

---
[파이널 팀프로젝트 관련]
- **토큰을 어떻게 포함시켜야 하는지 서버 개발자에게 물어봐야 한다.**
- **서버 개발자가 토큰을 어떻게 포함시킬지 설명서를 줄 것이다.**

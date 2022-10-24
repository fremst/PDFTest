pdf.js를 이용한 PDFViewer demo 파일입니다.
출처: https://github.com/mozilla/pdf.js#online-demo

1. demo 폴더는 demo html (demo/viewer/viewer.html) 실행에 필요한 필수 파일(개발자 도구 - 네트워크 이용해 확인)을 따로 백업해둔 폴더입니다.

2. viewerUsingLinks.html은 다른 파일 없이 실행 가능하도록 로컬 파일 대신 깃허브 링크로 수정한 파일입니다. (link 및 script의 rel과 src 수정)
   그 외 수정한 부분은 다음과 같고, 해당 부분은 소스 코드에서 '//'로 검색하면 찾을 수 있습니다.

- viewer.js 파일을 html에 통합하였습니다.
- pdfUrl을 사용해 파일을 읽어오도록 하였습니다. (queryString 대신 loadPdf()함수의 인자로 pdfUrl을 넘겨주도록)
- sendMessage / onmessage 추가하였습니다. (wix에서 iframe 외부 html과 연동하기 위함)

3. viewerUsingMyLinks.html 파일은 viewerUsingLinks.html에서 자체 제작한 cdn을 이용해 수정한 파일입니다. (원본 파일은 pdf-js 폴더에 백업하였습니다.)
   (pdf.js 버전업 오류 방지. 현재 버전 3.0.246)

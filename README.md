1. [DEV] Build target을 debug로 설정하면 local에서 svelte app을 run dev을 띄운 것 처럼 dev환경에서 run하고 mount한 src를 수정하여 새로고침하면 livereload됨
2. [Prod] Build target을 prod로 하면 build를 가져가서 static 페이지를 생성하여 nginx/html에 바인딩시킴. 추후에 docker-compose에 nginx service를 올려 conf를 설정할 예정

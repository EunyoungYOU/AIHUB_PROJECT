# AIHUB_PROJECT_동작 방식

bash 01. conda activate lib. 설치된 env. [일반 User APP] <br>
cd ./web_user <br> 
python app_server.py <br>

http://127.0.0.1:9070/ #열어서 알람 허용, push btn 눌러 '/static/sub_token.txt'에 구독 정보 저장 <br>

http://127.0.0.1:9070/fire #알람 눌러 page 들어가서 qr 촬영 or 층수 선택하면 detect server에 user type: user + 위치 log 전송 <br>
http://127.0.0.1:9070/fire > /end #탈출 완료 btn 누르면 detect server에 user_id 전송해 저장된 위치 log 삭제 <br>

bash 02. conda activate lib. 설치된 env. [재난 취약 계층 APP] <br>
cd ./web_usertype <br>
python app_server_barrier.py <br>

http://127.0.0.1:9060/ #열어서 알람 허용, push btn 눌러 '/static/sub_token.txt'에 구독 정보 저장 <br>

http://127.0.0.1:9060/fire #알람 눌러 page 들어가서 qr 촬영 or 층수 선택하면 detect server에 user type: barrier_free + 위치 log 전송 <br>
http://127.0.0.1:9060/fire > /end #탈출 완료 btn 누르면 detect server에 user_id 전송해 저장된 위치 log 삭제 <br>

bash 03. conda activate lib. 설치된 env. [모니터링 (관리자용)] <br>
cd ./yolo_service <br>
python detect.py --weights ./weight/last.pt (weight file path) --source ./monitor_1.mp4 (input source file path) <br>

http://[local ip address]:8080/ #모니터링 web page 열면, 위 두 client에 알람 및 화재 위치 전송 <br>


$$ 일부 파일 용량이 커서 git에 업로드 하지 못함. 모든 소스는 아래 google drive에서 download 가능 <br>
$$ 상황 발생 가정 시연 영상과 라이브 시연 영상 또한 아래 google drive에서 확인 가능 <br>
https://drive.google.com/drive/folders/1vu1rYWzuZlnTgJg0S2KrmK8vOeuFCExl?usp=sharing <br>




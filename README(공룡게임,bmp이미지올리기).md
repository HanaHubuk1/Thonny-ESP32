LCD 구글 공룡게임 만들기 전 필독

## 하드웨어: ST7735S(1.8'128x160 RGB_TFT), ESP32 확장보드, 암-암 핀 8개, 암-수 핀 4개, 브레드보드 1개, 데이터 전송용 케이블(포트 선)

## 소프트웨어 : Thonny 사용, MicroPython 사용

## 사용한 라이브러리 :
  - ST7735 드라이버 [https://github.com/boochow/MicroPython-ST7735/blob/master/ST7735.py]
  - 작성자 : GuyCarver (원작), boochow (수정작)

## 하드웨어 연결(핀 연결)

### ST7735S 디스플레이
---------------------------------------
BLK(백라이트{항상 켜짐}) - 3.3V
CS(Chip Select) - GPIO 15
DC(Data/Command) - GPIO 2
RST(Reset) - GPIO 4
SDA(MOSI{SPI 데이터 출력}) - GPIO 23
SCL(SCK{SPI 클럭}) - GPIO 18
VDD(5V 금지) - 3.3V
GND(그라운드) - GND
----------------------------------------
### 버튼 모듈 (3핀)
----------------------------------------
GND(그라운드) - GND
VCC(전원) - 3.3V
OUT(신호 출력{누르면 HIGH}) - GPIO 25
----------------------------------------
## 주의사항

**ST7735S는 반드시 3.3V 사용** - 5V 연결 시 디스플레이 손상! 
**GPIO 0 사용 금지** - 부팅 모드에 영향을 줄 수 있음

#공룡게임영상
[https://youtube.com/shorts/YLUvQQmYTL8?feature=share]
=========================================================================================================
.bmp 사진 올리기 전 필독

#ESP32보드에 image.bmp 파일을 cmd를 활용해서 업로드할 것
  
#1. cmd에 "pip install ampy" 입력 후 ampy 다운로드
#2. .jpg 사진을 128 x 160 사이의 크기로 조정
#3. .jpg 사진을 .bmp로 변환
#4. 그림판을 사용하여 32비트 사진에서 24비트 사진으로 저장(다른 이름으로 저장 하면 됨)
#5. ampy --port COM3 put C:\Users\사용자명\Desktop\image.bmp (COM3 부분은 본인의 포트번호로 변경, 사용자명은 본인 컴퓨터 명)
#6. ESP32 보드에 이 코드 main.py로 저장 후 실행 => LCD에 image.bmp 사진이 업로드됨

## 하드웨어: ST7735S(1.8'128x160 RGB_TFT), ESP32 확장보드, 암-암 핀 8개, 데이터 전송용 케이블(포트 선)

## 소프트웨어 : Thonny 사용, MicroPython 사용

## 사용한 라이브러리 :
  - ST7735 드라이버 [https://github.com/boochow/MicroPython-ST7735/blob/master/ST7735.py]
  - 작성자 : GuyCarver (원작), boochow (수정작)

## 하드웨어 연결(핀 연결)

### ST7735S 디스플레이
---------------------------------------
BLK(백라이트{항상 켜짐}) - 3.3V
CS(Chip Select) - GPIO 15
DC(Data/Command) - GPIO 2
RST(Reset) - GPIO 4
SDA(MOSI{SPI 데이터 출력}) - GPIO 23
SCL(SCK{SPI 클럭}) - GPIO 18
VDD(5V 금지) - 3.3V
GND(그라운드) - GND

## 주의사항

**ST7735S는 반드시 3.3V 사용** - 5V 연결 시 디스플레이 손상! 
**GPIO 0 사용 금지** - 부팅 모드에 영향을 줄 수 있음

#bmp 사진올리기 사진
![Uploading LCD에 사진 띄우기 1.jpg…]()
![Uploading LCD에 사진 띄우기 2.jpg…]()


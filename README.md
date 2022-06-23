# synth_labeling

# ABOUT

- generated된 한글 파일을 출력하여, 스캔한 후 나온 이미지 파일에 대해서 ocr labeling을 진행하는 방법에 관한 레포지토리

# Process
1) synth hwp(한글파일)데이터에서 사용되어있는 모든 단어의 위치를 자동으로 태깅
|![image](https://user-images.githubusercontent.com/63445349/175221551-dfc53c93-5fac-491f-a0a7-45b05d535ff3.png)
|![image](https://user-images.githubusercontent.com/63445349/175221455-64327b90-41b2-4a48-9133-21327653ff0e.png)|

2) 이 파일을 출력하여, 스캔한 이미지에서 해당 단어 위치정보를 그대로 사용하여 위치 추측


3) 스캔과 원본 한글 파일 사이의 차이(돌아감, 상하좌우정렬 등)를 자동으로 보정하도록 만듬
- 이미지가 어떻게 틀어져있는지 확인하기 위해서 문서 각 모서리에 보정용 사각형 사용

4) 세부 미세조정
![image](https://user-images.githubusercontent.com/63445349/175222460-c440767a-d39c-474f-a186-9b0dbbdbc413.png)
가로세로 최대 3픽셀 차이 허용, 가로선이나 세로선, 다른 글자의 일부가 label에 포함되면 안됨, 폰트마다 개별적용해야 함


# Todo

# Method

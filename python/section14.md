# [section14 파일 입출력의 활용] 

01. 파일 복사
    - 원본 파일 읽기 => 변수 저장 => 복사본 생성
    - 텍스트 파일뿐만 아니라 바이너리파일(이미지, 동영상 등)도 복사가 가능 하려면 바이너리 모드 파일을 열어야 한다.
    - 원본 파일을 한 번에 다 읽어 변수에 저장하면 메모리 용량이 부담스럽다. 
    - 따라서 한번에 읽는 데이터의 크기를 1kb(1024btye)로 설정한다.

02. csv(Comma Separated Values) 파일 입출력
    - csv란 쉼표로 구분된 데이터를 의미한다. 
    - 많은 양의 데이터를 주고받기 위한 표준 중 하나이다.
    ```
        # csv 파일 생성하기
        import csv
        file_name = '차량관리.csv'
        with open(file_name, 'w', newline='', encoding='utf-8') as file:
            csv_maker = csv.writer(file, delimiter=',')
            csv_maker.writerow([1, '08러1234', '2020-10-20 14:00'])
            csv_maker.writerow([2, '12다1234', '2020-10-20 14:00'])
            csv_maker.writerow([3, '67노1234', '2020-10-20 14:00'])
        print(file_name + ' 파일이 생성되었습니다.')

        # csv 파일 읽기
        import csv
        file_name = '차량관리.csv'
        with open(file_name, 'r', encoding='utf-8') as file:
            csv_reader = csv.reader(file, delimiter=',')
            for line in csv_reader:
                print(line)
    ```

03. json(JavaScript Object Notation) 파일 입출력
    - json이란 경량 데이터 전송에서 사용되는 표준 형식이다. 
    
    ```
        import json
        dict_list = [
            {   'name':'james',
                'age':20,
                'spec':[175.5, 70.5]
             }, 
            {   'name':'alice',
                'age':22,
                'spec':[168.5, 60.5]
            }
        ]
        json_string = json.dumps(dict_list)
        file_name = 'dictList.json'
        with open(file_name, 'w') as file:
            file.write(json_string)
        print(file_name + '파일이 생성 되었습니다.')
    ```

### MISSION ###
- 파일을 읽고 쓰는 방법만 알면 쉽게 파일 복사 프로그램을 구현할 수 있다.
- csv란 쉼표로 구분된 데이터를 의미한다. 많은 양의 데이터를 주고받기 위한 표준 중 하나이다.
- json이란 경량 데이터 전송에서 사용되는 표준 형식이다. 
- 비교적 적은 양의 데이터를 주고받는데 사용되며 현재 가장 널리 사용되는 데이터 전송 파일 형식이다.

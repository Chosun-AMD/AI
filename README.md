# Chosun A.M.D - AI

특성 추출과 학습을 위해 사용되는 Jupyter Notebook 파일입니다.

## 사용방법
### 종속 패키지 설치
다음 명령어를 사용하여 종속 패키지 설치를 해야 됩니다.
```
pip install -r src/requirements.txt
```

### 실행
#### 특성 추출
##### 문자열 특성 추출
다음과 같은 명령어를 통해서 파일의 문자열을 추출합니다.
```
$ export PATH=$PATH:`pwd`/src/features/src/
$ find [TARGET_DIR] -name '*.vir' | xargs -I {} 'extract_ascii {} DEST_PATH'
$ find [TARGET_DIR] -name '*.vir' | xargs -I {} 'extract_utf16le {} DEST_PATH'
```

추출한 문자열을 경로를 기억한 뒤 `strings.ipynb`을 실행하면서 입력을 하면 됩니다. 자세한 사항은 `strings.ipynb`를 참조하면 됩니다.

##### 기타 특성 추출
기타 특성 추출의 경우 대상이 되는 PE파일의 경로를 요구합니다. 해당 경로를 Jupyter Notebook을 실행하면서 해당 상황에 맞춰서 넣으면 됩니다.

#### AI 학습
AI는 텐서플로우를 사용합니다. 각 환경에 맞춰 텐서플로우를 설치 한뒤 추가로 다음 명령어를 실행합니다.
```
$ pip install silence_tensorflow
$ pip install numpy pandas
```

학습은 Jypter Notebook을 실행하면 됩니다.

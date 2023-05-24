# Code Peer Review Templete
- 코더 : 김다인
- 리뷰어 : 장승우


# PRT(PeerReviewTemplate)
각 항목을 스스로 확인하고 체크하고 확인하여 작성한 코드에 적용하세요.
- [O] 1.코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
- [O] 2.주석을 보고 작성자의 코드가 이해되었나요?
- [O] 3.코드가 에러를 유발한 가능성이 있나요?
- [O] 4.코드 작성자가 코드를 제대로 이해하고 작성했나요?
- [O] 5.코드가 간결한가요?

# 예시
1. 코드의 작동 방식을 주석으로 기록합니다.
2. 코드의 작동 방식에 대한 개선 방법을 주석으로 기록합니다.
3. 참고한 링크 및 ChatGPT 프롬프트 명령어가 있다면 주석으로 남겨주세요.
```
#validation set 10000건 분리
x_val = x_train[:10000]   
y_val = y_train[:10000]
#나머지
partial_x_train = x_train[10000:]  
partial_y_train = y_train[10000:]
 >> load_data 함수에서 x_train과 x_test를 나눠줬기 때문에 개인적으로는 별도로 나누지 않고 했었는데 k-fold같이 다시 분류하는 것도 괜찮은 것 같습니다.

word_vector_dim = 100  

model = tf.keras.Sequential()
model.add(keras.layers.Embedding(vocab_size, 
                                 word_vector_dim, 
                                 embeddings_initializer=Constant(embedding_matrix),  #카피한 임베딩을 여기서 활용
                                 input_length=maxlen, 
                                 trainable=True))   #trainable을 True로 주면 Fine-tuning
model.add(keras.layers.LSTM(128))
>> 입력 차원수에 맞게 layer의 차원도 맞아야 하는 것으로 알고 있었는데 아니라는 것을 알게되었습니다.
```

# 참고 링크 및 코드 개선 여부
```python
#
#
#
#
```

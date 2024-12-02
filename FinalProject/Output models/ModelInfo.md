1201best.pt
    DataSet: FOOD-INGREDIENTS-dataset-4 / project = rf.workspace("food-recipe-ingredient-images-0gnku").project("food-ingredients-dataset")
    Training env: BATCH_SIZE = 16 EPOCHS = 15 LR = 5e-5
// 현재 식재료 탐지 성능이 매우 떨어짐
// epochs 수를 늘리고 lr을 높여 다시 학습 예정

1202best.pt
    DataSet: FOOD-INGREDIENTS-dataset-4 / project = rf.workspace("food-recipe-ingredient-images-0gnku").project("food-ingredients-dataset")
    Training env: BATCH_SIZE = 16 EPOCHS = 50 LR = 0.001
// 나쁘지 않은 성능 향상인데.. 좀 더 성능을 높일 필요가 있음
// 이 모델에서 lr만 조금 줄여서 추가로 학습을 진행해 볼까 생각중.
// epoch 40 부근에서 dfl에 많은 변화가 있음. 근데 이 부근에서 box loss도 많이 감소함. 왜 그런지는 잘 모르겠음.
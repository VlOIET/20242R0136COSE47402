## YOLO
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
// epoch 40 부근에서 dfl에 많은 변화가 있음. 근데 이 부근에서 box loss도 많이 감소함. 왜 그런지는 잘 모르겠음. 그냥 상호작용일 수도?

1205best.pt
    DataSet: FOOD-INGREDIENTS-dataset-4 / project = rf.workspace("food-recipe-ingredient-images-0gnku").project("food-ingredients-dataset")
    model: YOLOv8m / Training env: BATCH_SIZE = 32 EPOCHS = 70 LR = 0.001
// 돈 덕분에 nano -> medium 모델로 바꿈. 확실히 nano보다는 성능이 뛰어나고 BATCH_SIZE도 늘려서 학습시간이 꽤 줄었음.

## llama
1203
    DataSet: Shengtao/recipe / dataset = load_dataset("Shengtao/recipe")
    model: meta-llama/Llama-2-7b-hf / Training env: BATCH_SIZE = 4 EPOCHS = 3 LR = 5e-5 

1205
    DataSet: Shengtao/recipe / dataset = load_dataset("Shengtao/recipe")
    model: meta-llama/Llama-2-7b-hf / Training env: BATCH_SIZE = 4 EPOCHS = 3 LR = 5e-5
// 1203에서 사용했던 데이터 셋을 전처리할 때 Q&A 방식으로 되도록 변경
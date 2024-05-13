# Использование
---
## Обучение 
`$ python3 train.py --img 640 --batch 8 --epochs 150 --data data.yaml --optimizer SGD`      
Результаты сохранятся в `runs/`
Наилучшая модель сохранится в `runs/train/exp2/weights/best.pt`

---
## Проверка и использование
Далее можно проверить модель на наборе данных с помощью:     
`$ python val.py --weights runs/train/exp2/weights/best.pt --data data.yaml --img-size 640 --conf-thres 0.25 --iou-thres 0.45 --device cpu`       
Также можно использовать модель для обнаружения объектов на изображении текстов с помощью `detect.py`:      
`$ python detect.py --weights runs/train/exp2/weights/best.pt --data data.yaml --img-size 640 --conf-thres 0.25 --iou-thres 0.45 --source ***.jpg`

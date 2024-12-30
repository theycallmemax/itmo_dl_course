### Дополнительное задание 2 - 5 баллов

Реализуйте модель для классификации изображений датасета [FashionMNIST](https://pytorch.org/vision/0.20/generated/torchvision.datasets.FashionMNIST.html#torchvision.datasets.FashionMNIST) на PyTorch Lightning
1. **1 балл** Создайте класс `FashionMNISTDataModule`, реализуйте в нем:
    - загрузку данных, 
    - предобработку (перевод в тензоры, нормализация, etc
    - разбиение на train/val/test части
    - создание dataloader'ов- **1 балл**
2. **2 балла** Создайте класс модели `FashionMNIST` (наследник `LightningModule`), реализуйте в нем:
    - training_step, validation_step, test_step
    - расчет метрик на валидации и тестировании из TorchMetrics: F1, ROC AUC
    - логирование метрик и функций потерь на каждой эпохе валидации/теста
    - подберите подходящие, на ваш взгляд, optimizer и lr-scheduler, а также их гиперпараметры
3. **1 балл** Обучите модель с помощью trainer'а:
    - добавьте `EarlyStopping`
    - реализуйте визуализацию логов через tensorboard
    - проверьте качество на тестовой части данных
    

Обеспечена воспроизводимость решения: зафиксированы random_state, ноутбук воспроизводится от начала до конца без ошибок - **1 балл**

# 📊 Detalles del modelo

La arquitectura del modelo se basa en una **Red Neuronal Convolucional (CNN)** construida con **Keras**, que incluye múltiples capas de convolución, normalización, pooling y capas densas, finalizando con una capa **softmax** para clasificación multiclase. 

| 🧩 Layer (type)                           | Output Shape         | Param # |
| ----------------------------------------- | -------------------- | ------- |
| 🟦 **conv2d_20 (Conv2D)**                 | (None, 230, 230, 16) | 160     |
| 🟪 **batch_normalization_10 (BatchNorm)** | (None, 230, 230, 16) | 64      |
| 🟩 **max_pooling2d_25 (MaxPooling2D)**    | (None, 115, 115, 16) | 0       |
| 🟦 **conv2d_21 (Conv2D)**                 | (None, 115, 115, 32) | 4,640   |
| 🟪 **batch_normalization_11 (BatchNorm)** | (None, 115, 115, 32) | 128     |
| 🟩 **max_pooling2d_26 (MaxPooling2D)**    | (None, 57, 57, 32)   | 0       |
| 🟦 **conv2d_22 (Conv2D)**                 | (None, 57, 57, 64)   | 18,496  |
| 🟪 **batch_normalization_12 (BatchNorm)** | (None, 57, 57, 64)   | 256     |
| 🟩 **max_pooling2d_27 (MaxPooling2D)**    | (None, 28, 28, 64)   | 0       |
| 🟨 **global_average_pooling2d (GAP)**     | (None, 64)           | 0       |
| 🔴 **dropout_16 (Dropout)**               | (None, 64)           | 0       |
| 🟧 **dense_24 (Dense)**                   | (None, 64)           | 4,160   |
| 🔴 **dropout_17 (Dropout)**               | (None, 64)           | 0       |
| 🟧 **dense_25 (Dense)**                   | (None, 11)           | 715     |

- **📝 Total params:** 28,619 (≈111.79 KB)
- **⚡ Trainable params:** 28,395 (≈110.92 KB)
- **❌ Non-trainable params:** 224 (≈896 B)


## 🏷️ Clasificacion

```python
label_map = {
    0: 'motherboard',
    1: 'gpu',
    2: 'cpu',
    3: 'hard_drive',
    4: 'ram',
    5: 'pc_case',
    6: 'power_supply',
    7: 'liquid_cooling',
    8: 'case_fan',
    9: 'cpu_fan',
    10: 'sound_card'
}
```
### 1. 数据集准备

ImageNet : https://image-net.org/download-images.php

Forest Cover Type : https://www.kaggle.com/c/forest-cover-type-prediction/data

使用以下.py文件得到图像直方图特征
```bash
python gen_data.py
```

### 2. 使用CMake文件进行编译

```bash
mkdir build
cd build
cmake ..
make all
```

### 3. 运行可执行文件

```bash
./main [number of pivot point] [number of cluster] [dimention of point] [evaluate the clustering or not(0 /1 : [min number of cluster] [max number of cluster] [step size])]
```





# ImageNet-Caltech-101
Mid-term project of DATA620004: Fine-tuning a CNN pre-trained on ImageNet for Caltech-101 classification​.

This project uses a pre-trained ResNet-50 model from [PyTorch Vision](https://pytorch.org/vision/stable/models.html),  
which is licensed under [BSD 3-Clause](LICENSE-PYTORCH), and the [Caltech-101 dataset](http://www.vision.caltech.edu/Image_Datasets/Caltech101/).

## 📥 Download Instructions
```bash
# Download the dataset from Caltech's official website
wget http://www.vision.caltech.edu/Image_Datasets/Caltech101/101_ObjectCategories.tar.gz

# Extract the dataset
tar -xvzf 101_ObjectCategories.tar.gz
```

This will create a folder named 101_ObjectCategories/ containing 101 object categories.

We make split datasets into trianing, validating and testing set in __task1.ipynb__.

## 📊 Visualizing with TensorBoard

To monitor training metrics such as loss and accuracy, use [TensorBoard](https://www.tensorflow.org/tensorboard):

```bash
tensorboard --logdir runs
```
## 🏋️ Model weight

After training your model, you can save its weights using:

```python
torch.save(model.state_dict(), f"resnet18_caltech101_lr{lr}_mom{momentum}_ep{num_epochs}.pth")
```

and load weights using:

```python
model.load_state_dict(torch.load("your path"))
```



### 🔗 Google Drive
The trained model weight of Alexnet and Resnet can be found in:
- [Model Weight 1](https://drive.google.com/file/d/1SbtC3HwTijjCy57pbnTD6PehE71VpZgv/view?usp=sharing)
- [Model Weight 2](https://drive.google.com/file/d/1zLLmux0JkzHPDW_W2iU6Biz1slylDkUr/view?usp=sharing)

# Muusa.github.io
1
import numpy as np

# 数据
x = np.array([1, 2, 3])
y = np.array([2, 4, 6])

# 初始化参数
w, b = 0.0, 0.0
lr = 0.01

# 训练
for _ in range(1000):
    y_pred = w * x + b
    loss = ((y - y_pred) ** 2).mean()
    
    # 梯度
    dw = -2 * ((y - y_pred) * x).mean()
    db = -2 * (y - y_pred).mean()
    
    # 更新
    w -= lr * dw
    b -= lr * db

print(w, b)

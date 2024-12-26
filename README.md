# Artificial-Potential-Field-based-RL-for- Path-Planning
环境依赖：

stable-baselines3            1.8.0

gym                          0.21.0

奖励函数优化目标

引力奖励（目标吸引力）：
鼓励车辆靠近目标位置，但需要避免在接近目标时奖励震荡。
改为平滑的距离递减函数，例如高斯衰减函数或对数衰减函数。

斥力奖励（障碍回避）：
保留原本的障碍斥力，但增强对危险区域的惩罚，避免车辆过于接近障碍物。
在距离较远时弱化斥力影响，以减少对学习的干扰。

边界惩罚：
提供更平滑的边界惩罚，鼓励车辆保持在车道内。

碰撞惩罚：
立即惩罚，确保车辆尽量避免碰撞。

成功奖励：
到达目标后，提供较大的奖励以显式鼓励。

时间步惩罚：
加入时间步惩罚，防止车辆停滞不前。

训练时将train=True
测试时将train=False

绝对位置观测空间测试：

![simulation](https://github.com/user-attachments/assets/836ebc5e-5e57-4fff-8074-16ad75f0eb87)

相对位置观测空间（前方两个障碍物）

![relative_front_2_position](https://github.com/user-attachments/assets/4b04e21c-8d68-4eb7-9c2d-b46185ddc974)


人工势场法：

![trajectory](https://github.com/user-attachments/assets/40f02cdb-a4b7-4f21-baf2-d9d9b35560e0)


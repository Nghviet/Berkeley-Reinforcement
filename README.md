# Berkeley-Reinforcement

Họ tên : Nguyễn Hoàng Việt

MSSV : 18020063

Lớp INT 3401 8

autograder_result.txt chứa result của 1 lần autograder, không phải lúc quay film để báo cáo

# Bài 1: 

QValue của 1 cặp state,action được tính bằng tổng điểm thưởng của hành động cộng với giá trị của state tiếp theo nhân với xác suất đạt được và discount

Việc lấy hành động của 1 state đơn giản là lấy hành động có điểm QValue lớn nhất

# Bài 2:

Tắt noise, giữ nguyên discount = 0.9

# Bài 3:

Để chọn con đường xa thì discount lớn ( gần 1 và trên 1) , và ngược lại, con đường ngắn sẽ có discount nhỏ ( gần 0)
Để tránh con đường gần vực thì livingReward = 0. Đề chon con đường đi xa gần vực thì em để livingReward < 0 vì  giá trị livingReward > 0 em thử đều chon điểm thưởng ở gần để đến


# Bài 4:

Các cặp giá trị QValue (state,action) được lưu vào 1 map 2 chiều.

Value của 1 state được tính là giá trị QValue lớn nhất của các legal action

Action của 1 state sẽ là ngẫu nhiên 1 hành động từ legal action mà có giá trị QValue(state,action) bằng với giá trị value của state đó

Công thức update trong slide newValue = oldValue + alpha * (reward + discount * QValue(state,action) - oldValue)

# Bài 5:

Nếu hàm flipCoin(epsilon) trả lại giá trị True thì hành động tiếp theo được trả lại là ngẫu nhiên từ những tập hợp nhưng hành động của state, ko thì vẫn tuân theo policy


# Bài 8:

Sửa lại các hàm getQValue và update trong ApproximateQAgent theo công thức được cung cấp trong đề bài

Thêm một số biến trong PacmanQAgent do không thể sử dụng các giá trị alpha, gamma và epsilon trong ApproximateQAgent


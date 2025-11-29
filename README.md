# 🚦 Traffic + 🌫️ Air Quality Dashboard (Smart City Project)

## 📌 Tổng quan
Dự án này tập trung vào việc **phân tích mối quan hệ trực tiếp giữa giao thông và chất lượng không khí** trong bối cảnh **Smart City**.  
Ý tưởng chính:  
- Lượng xe tăng → PM2.5, CO2 tăng  
- Kẹt xe → Ô nhiễm không khí tăng theo thời gian thực  

Hệ thống giúp hiển thị, cảnh báo và phân tích dữ liệu để hỗ trợ quản lý đô thị thông minh.

---

## 🎯 Tính năng chính
- **Dashboard trực quan**: hiển thị mức độ ô nhiễm theo từng tuyến đường.  
- **Cảnh báo thời gian thực**: phát hiện và cảnh báo khi mật độ xe tăng dẫn đến khí độc vượt ngưỡng.  
- **Phân tích nguyên nhân**: thống kê và phân tích ô nhiễm theo giờ cao điểm, hỗ trợ hoạch định chính sách giao thông.  

---

## 🛠️ Kiến trúc hệ thống
- **Traffic Data**: thu thập từ **Kafka** (streaming real-time).  
- **Air Quality Data (AQI)**: lấy từ **API bên ngoài** hoặc **mô phỏng dữ liệu**.  
- **Data Processing**: tích hợp, đồng bộ và phân tích dữ liệu giao thông + chất lượng không khí.  
- **Visualization**: dashboard hiển thị trực quan, dễ theo dõi.  

---

## 📊 Luồng dữ liệu
1. Kafka nhận dữ liệu giao thông (mật độ xe, tốc độ, tình trạng kẹt xe).  
2. API/mô phỏng cung cấp dữ liệu AQI (PM2.5, CO2, NOx...).  
3. Hệ thống phân tích mối quan hệ giữa traffic và AQI.  
4. Dashboard hiển thị kết quả + cảnh báo thời gian thực.  

---

## 🚀 Hướng dẫn triển khai
### Yêu cầu
- Python 3.9+  
- Apache Kafka  
- Node.js (cho phần frontend dashboard)  
- API key (nếu dùng dịch vụ AQI thật)

### Cài đặt
```bash
# Clone repo
git clone https://github.com/your-username/traffic-air-quality.git
cd traffic-air-quality

# Cài đặt dependencies
pip install -r requirements.txt

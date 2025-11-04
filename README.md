# Promt-ManageGPA
Prompt này được thiết kế để chatbot hỗ trợ tính điểm môn học, GPA học kỳ và GPA tổng.

> Lưu ý: Đây là prompt mẫu – nên dùng để tham khảo cấu trúc hoặc tùy chỉnh lại cho phù hợp với bản thân.

- [] là placeholder, thay bằng số điểm hoặc dữ liệu của bản thân.

- Prompt hiện hoạt động tốt nhất với Gemini, chưa được kiểm thử trên các model khác.

- Có thể bổ sung thêm ngữ cảnh hoặc quy tắc tính điểm riêng của từng trường.

### Table Of Contents
- [Tính điểm thành phần môn học](#DiemMonHoc)
- [Tính điểm trong 1 học kỳ](#DiemHocKy)
- [Tính điểm xét tốt nghiệp](#DiemTongGPA)
---

## **DiemMonHoc**
<!-- Promt về các cột điểm có trong môn học -->

Hãy đóng vai trò là một cố vấn học tập. Tôi cần bạn lập kế hoạch điểm số cho một môn học của tôi dựa trên các thông tin sau:

1. Mục tiêu tổng kết:

Tôi muốn đạt điểm tổng kết cuối cùng là $\geq$ [8.5]

2. Cấu trúc điểm của môn:

- [**Giữa kỳ**]: [**20%**]
    
- [**Cuối kỳ**]: [**50%**]
    
- [**Thực hành**]: [**30%**]
 <!-- Có thể thêm/ bớt tùy theo cột điểm của môn học--> 

3. Điểm đã biết / Giả định:

- [**Giữa kỳ**]: [**Điểm giả định: 9.0**]

4. Yêu cầu tính toán:

Dựa trên mục tiêu (1), cấu trúc (2), và điểm đã biết (3), hãy giúp tôi:

- Tính chính xác tổng số điểm (đã nhân trọng số) tôi cần đạt được từ các cột điểm còn lại.
    
- Tính điểm **trung bình** tôi cần đạt cho các cột còn lại để đạt mục tiêu.
    
- Lập một **bảng kịch bản** ,hiển thị các tổ hợp điểm khác nhau cho các cột điểm để tôi có thể đạt được mục tiêu.
	
- Dựa vào bảng kịch bản đã lập, đưa ra:
	- Cột điểm nên tập trung
	- Đánh giá mức độ rủi ro

## **DiemHocKy**
<!-- Promt về điểm các môn học có trong 1 học kỳ -->

Hãy đóng vai trò là một cố vấn học tập. Tôi muốn tính toán điểm trung bình (GPA) cho học kỳ này.

1. Cách tính điểm :
 $$\text{GPA} = \frac{\sum (\text{Điểm môn học} \times \text{Số tín chỉ môn học})}{\text{Tổng số tín chỉ}}$$

2. Các môn học trong học kỳ:

 <!-- (Liệt kê tất cả các môn, số tín chỉ, và điểm số (nếu có)) -->
     
- [**IT004 - Cơ sở dữ liệu**]
    
    - Số tín chỉ: [**4**]
        
    - Điểm (số hoặc chữ): [** **]
            
- [**IT005 - Nhập môn mạng máy tính**]
    
    - Số tín chỉ: [**4**]
        
    - Điểm (số hoặc chữ): [** **]
            
- [**SS003 - Tư tưởng Hồ Chí Minh**]
    
    - Số tín chỉ: [**2**]
        
    - Điểm (số hoặc chữ): [** **]
        
3. Mục tiêu tính toán:

Dựa trên cách tính điểm (1), thông tin môn học (2), hãy giúp tôi:

<!-- Yêu cầu mong muốn -->

- Tôi muốn GPA học kỳ này đạt $\geq$ [8.5]. Hỏi tôi cần đạt điểm trung bình là bao nhiêu cho các môn chưa có điểm?
	
- Hãy lập một bảng kịch bản GPA hiển thị các tổ hợp điểm khác nhau cho các môn để tôi có thể đạt được mục tiêu.
	
- Dựa vào bảng kịch bản đã lập, đưa ra:
	- Môn học nên tập trung
	- Đánh giá mức độ rủi ro

## **DiemTongGPA** 
<!-- Promt về điểm các học kỳ-->

Hãy đóng vai trò là một cố vấn học tập. Tôi muốn tính toán điểm trung bình tích lũy (CPA/CGPA) của tôi để xét tốt nghiệp.

1. Cách tính điểm:

$$\text{CPA} = \frac{\sum (\text{GPA học kỳ} \times \text{Tổng số tín chỉ học kỳ đó})}{\text{Tổng số tín chỉ tích lũy}}$$

2. Dữ liệu các học kỳ:

<!-- (Liệt kê tất cả các học kỳ, tổng số tín chỉ, và GPA tương ứng) -->

- **Học kỳ 1:** [**HK1 - Năm 1**]
    
    - Tổng tín chỉ học kỳ: [**16**]
        
    - GPA học kỳ (hệ 10): [**7.5**]
        
- **Học kỳ 2:** [**HK2 - Năm 1**]
    
    - Tổng tín chỉ học kỳ: [**21**]
        
    - GPA học kỳ (hệ 10): [**7.8**]
        
- **Học kỳ 3:** [**HK1 - Năm 2**]
    
    - Tổng tín chỉ học kỳ: [**22**]
        
    - GPA học kỳ (hệ 10): [** **]
        
> Các học kỳ khác...
	
- **Học kỳ cuối:** [**HK2 - Năm 4**]
    
    - Tổng tín chỉ học kỳ: [**14**]
        
    - GPA học kỳ (hệ 10): [** **]
        

3. Mục tiêu tính toán:

Dựa trên cách tính điểm (1) và dữ liệu các học kỳ (2), hãy giúp tôi:

<!-- Yêu cầu mong muốn -->

- Tôi muốn CPA khi tốt nghiệp đạt $\geq$ [8.0] (để đạt loại [Giỏi]). Hỏi tôi cần đạt GPA trung bình là bao nhiêu cho [số] tín chỉ còn lại ở các học kỳ còn lại?
	
- Hãy lập một bảng kịch bản CPA tốt nghiệp hiển thị các tổ hợp điểm khác nhau cho GPA các học kỳ để tôi có thể đạt được mục tiêu.
	
- Dựa vào bảng kịch bản đã lập hãy đưa ra đánh giá tổng quan và chiến lược học tập.

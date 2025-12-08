---
title: "Event 5"
date: ""
weight: 5
chapter: false
pre: " <b> 4.5. </b> "
---
# Bài thu hoạch “Workshop: AWS Well-Architected Security Pillar”

### Mục Đích Của Sự Kiện

- Hiểu rõ tầm quan trọng của trụ cột Bảo mật (Security Pillar) trong khung kiến trúc AWS Well-Architected.
- Nắm vững mô hình trách nhiệm chia sẻ (Shared Responsibility Model) và các nguyên tắc cốt lõi: Least Privilege, Zero Trust, Defense in Depth.
- Học cách áp dụng 5 lĩnh vực bảo mật chính: IAM, Detection, Infrastructure Protection, Data Protection và Incident Response.
- Nhận diện các mối đe dọa an ninh phổ biến tại Việt Nam và cách phòng chống.

### Danh Sách Diễn Giả

- **Đội ngũ chuyên gia bảo mật từ AWS (AWS Security Specialists).**

### Nội Dung Nổi Bật

Buổi workshop tập trung sâu vào 5 lĩnh vực chính (5 Pillars) của bảo mật trên Cloud:

#### 1. Identity & Access Management (Quản lý định danh)
- **Nguyên tắc:** Tránh sử dụng thông tin xác thực dài hạn (long-term credentials) cho người dùng.
- **Giải pháp:**
    - Sử dụng **IAM Roles** thay vì Access Keys cố định.
    - **IAM Identity Center:** Quản lý đăng nhập một lần (SSO) tập trung.
    - **SCP (Service Control Policies):** Thiết lập rào chắn bảo mật cho môi trường nhiều tài khoản (multi-account).
    - Bắt buộc kích hoạt **MFA** và xoay vòng credential định kỳ.

#### 2. Detection (Phát hiện mối đe dọa)
- **Logging toàn diện:** Kích hoạt CloudTrail (ở cấp organization), VPC Flow Logs, và S3 access logs.
- **Công cụ phát hiện:**
    - **Amazon GuardDuty:** Phát hiện hành vi bất thường nhờ Machine Learning.
    - **AWS Security Hub:** Trung tâm quản lý tư thế bảo mật (security posture).
- **Detection-as-Code:** Tự động hóa việc tạo rule cảnh báo thông qua code hạ tầng.

#### 3. Infrastructure Protection (Bảo vệ hạ tầng)
- **Network Security:** Phân đoạn mạng (VPC segmentation), đặt resources vào private subnet nếu không cần public.
- **Defense in Depth (Bảo mật đa lớp):** Kết hợp Security Groups (firewall mức instance), NACLs (firewall mức subnet), AWS WAF (Web App Firewall) và AWS Shield (chống DDoS).

#### 4. Data Protection (Bảo vệ dữ liệu)
- **Encryption:** Mã hóa dữ liệu cả khi lưu trữ (at-rest) và khi truyền tải (in-transit).
- **Key Management:** Sử dụng **AWS KMS** để quản lý khóa mã hóa, thiết lập chính sách xoay vòng khóa (key rotation).
- **Secrets Management:** Không hard-code mật khẩu trong code, sử dụng **AWS Secrets Manager** để lưu và tự động xoay vòng DB credentials.

#### 5. Incident Response (Phản ứng sự cố)
- **IR Lifecycle:** Chuẩn bị -> Phát hiện -> Kiềm chế -> Điều tra -> Phục hồi.
- **Automation:** Sử dụng AWS Lambda và Step Functions để tự động hóa các hành động phản ứng (ví dụ: tự động thu hồi quyền của IAM user bị lộ key, cô lập EC2 nhiễm mã độc).

### Những Gì Học Được

#### Tư Duy Bảo Mật (Security Mindset)
- **Security is Day 0:** Bảo mật không phải là bước cuối cùng trước khi deploy, mà phải được tích hợp ngay từ khâu thiết kế (Shift Left Security).
- **Zero Trust:** Không tin tưởng bất kỳ ai hay thiết bị nào, luôn xác thực và ủy quyền lại cho mỗi request.
- **Automate Security:** Con người có thể sai sót, nhưng code thì ổn định. Tự động hóa càng nhiều quy trình bảo mật càng tốt.

#### Kiến Thức Kỹ Thuật
- Phân biệt rõ sự khác nhau và cách phối hợp giữa **Security Group** (stateful) và **NACL** (stateless).
- Hiểu cách hoạt động của **KMS Envelope Encryption** (mã hóa phong bì) để bảo vệ dữ liệu hiệu quả.

### Ứng Dụng Vào Công Việc

- **Audit lại dự án:** Kiểm tra ngay các Security Group trong dự án thực tập, loại bỏ các rule `0.0.0.0/0` không cần thiết (đặc biệt là port SSH/RDP).
- **Bảo vệ Secrets:** Chuyển toàn bộ database credentials đang để trong file cấu hình sang **AWS Secrets Manager**.
- **Kích hoạt GuardDuty:** Đề xuất bật GuardDuty để giám sát các hành vi đáng ngờ trong tài khoản AWS của team.

### Trải nghiệm trong event

Workshop **Well-Architected Security Pillar** đã thay đổi hoàn toàn quan điểm của em về bảo mật.

#### "Giật mình" với các mối đe dọa thực tế
- Phần chia sẻ về **Top threats** tại Việt Nam khiến em nhận ra rằng việc lộ Access Key hay mở public S3 bucket là những lỗi rất sơ đẳng nhưng hậu quả lại cực kỳ nghiêm trọng.

#### Demo trực quan
- Việc xem demo trực tiếp cách hacker khai thác một lỗ hổng IAM và cách hệ thống tự động phát hiện, ngăn chặn bằng Lambda thực sự rất thuyết phục. Nó chứng minh sức mạnh của **Automated Incident Response**.

#### Quy trình chuẩn chỉnh
- Em học được rằng phản ứng sự cố không phải là "loay hoay" sửa lỗi, mà phải có **Playbook** (kịch bản) rõ ràng: cô lập, thu thập bằng chứng (forensics) rồi mới phục hồi.

#### Bài học rút ra
- Bảo mật là trách nhiệm của tất cả mọi người (Shared Responsibility), không chỉ của đội Security. Là một Developer, viết code an toàn và cấu hình hạ tầng đúng chuẩn là đóng góp lớn nhất cho bảo mật của tổ chức.

#### Một số hình ảnh khi tham gia sự kiện
* Thêm các hình ảnh chụp slide về mô hình Shared Responsibility, demo GuardDuty, hoặc không gian workshop *

> Tổng kết: Sự kiện giúp em xây dựng nền tảng vững chắc để trở thành một kỹ sư không chỉ giỏi về tính năng mà còn đáng tin cậy về bảo mật (Security-first Engineer).
---
title: "Event 4"
date: ""
weight: 4
chapter: false
pre: " <b> 4.4. </b> "
---

# Bài thu hoạch “Workshop: DevOps on AWS”

### Mục Đích Của Sự Kiện

- Hiểu đúng về tư duy và văn hóa DevOps (DevOps Mindset & Culture).
- Nắm vững bộ công cụ CI/CD của AWS để tự động hóa quy trình phát triển phần mềm.
- Học cách quản lý hạ tầng dưới dạng mã (Infrastructure as Code - IaC).
- Làm quen với công nghệ Container và các chiến lược triển khai ứng dụng hiện đại.
- Thiết lập hệ thống giám sát (Monitoring) và khả năng quan sát (Observability) toàn diện.

### Danh Sách Diễn Giả

- **Đội ngũ chuyên gia kỹ thuật từ AWS (AWS Technical Experts).**

### Nội Dung Nổi Bật

Đây là workshop diễn ra cả ngày (Full-day) với hàm lượng kiến thức chuyên sâu, bao gồm hai phiên chính:

#### 1. Phiên Sáng: CI/CD & Infrastructure as Code
- **DevOps Mindset:** DevOps không chỉ là công cụ mà là sự kết hợp giữa văn hóa, quy trình và công cụ. Giới thiệu các chỉ số đo lường hiệu quả (DORA metrics) như tần suất deploy, thời gian phục hồi lỗi (MTTR).
- **AWS CI/CD Pipeline:**
    - **Source Control:** Quản lý mã nguồn với AWS CodeCommit và các chiến lược Git (GitFlow, Trunk-based).
    - **Build & Test:** Tự động hóa việc build và test code với AWS CodeBuild.
    - **Deployment:** Triển khai ứng dụng tự động với AWS CodeDeploy (hỗ trợ Blue/Green, Canary).
    - **Orchestration:** Điều phối toàn bộ quy trình bằng AWS CodePipeline.
- **Infrastructure as Code (IaC):**
    - **CloudFormation:** Tạo và quản lý tài nguyên AWS bằng template JSON/YAML, phát hiện sai lệch cấu hình (drift detection).
    - **AWS CDK:** Định nghĩa hạ tầng bằng ngôn ngữ lập trình quen thuộc (Python, TypeScript, Java), giúp tái sử dụng code dễ dàng hơn.

#### 2. Phiên Chiều: Containers & Observability
- **Container Services:**
    - **Amazon ECR:** Kho lưu trữ Docker image an toàn.
    - **Amazon ECS & EKS:** So sánh các dịch vụ điều phối container, chiến lược scaling.
    - **AWS App Runner:** Giải pháp deploy container đơn giản hóa cho developer.
- **Monitoring & Observability:**
    - **CloudWatch:** Thu thập metrics, logs, tạo dashboard và cảnh báo (alarms).
    - **AWS X-Ray:** Truy vết (tracing) các request đi qua hệ thống phân tán để tìm điểm nghẽn (bottleneck).
- **DevOps Best Practices:** Các chiến lược triển khai an toàn (Feature flags, A/B testing) và quản lý sự cố (Incident management).

### Những Gì Học Được

#### Kiến thức Kỹ thuật
- **Automation is King:** Hiểu được sức mạnh của việc tự động hóa mọi thứ, từ việc commit code đến khi deploy ra production, giúp giảm thiểu lỗi do con người.
- **IaC vs Click-ops:** Nhận thức rõ sự ưu việt của việc dùng code để quản lý hạ tầng (CDK/CloudFormation) so với việc thao tác thủ công trên Console (Click-ops), đặc biệt là khả năng tái tạo môi trường nhanh chóng.
- **Observability:** Phân biệt được Monitoring (hệ thống có đang hoạt động không?) và Observability (tại sao hệ thống hoạt động như vậy?), vai trò quan trọng của X-Ray trong microservices.

#### Kỹ năng Thực hành
- Biết cách thiết lập một pipeline CI/CD cơ bản.
- Biết cách viết một đoạn script CDK đơn giản để tạo S3 bucket hoặc EC2 instance.

### Ứng Dụng Vào Công Việc

- **Cải tiến dự án:** Áp dụng ngay AWS CodePipeline vào dự án thực tập hiện tại để tự động hóa việc deploy code mỗi khi có update mới.
- **Chuyển đổi sang IaC:** Bắt đầu tập viết CloudFormation/CDK cho các tài nguyên đang sử dụng thay vì tạo tay, giúp dễ dàng chia sẻ cấu hình cho các thành viên khác trong team.
- **Tối ưu giám sát:** Thiết lập CloudWatch Alarms để nhận cảnh báo qua email/Slack khi CPU hoặc Memory của server tăng cao bất thường.

### Trải nghiệm trong event

Workshop **DevOps on AWS** là một ngày học tập cường độ cao nhưng vô cùng giá trị.

#### Sự chuyên sâu và liền mạch
- Chương trình đi từ tư duy (Mindset) đến công cụ (Tools) và thực hành (Practice) tạo nên một luồng kiến thức rất logic.
- Các demo về **Blue/Green Deployment** giúp em "mắt thấy tai nghe" cách update ứng dụng mà không gây gián đoạn dịch vụ (zero downtime) - điều mà trước đây em chỉ đọc trong lý thuyết.

#### Cơ hội định hướng nghề nghiệp
- Phần Q&A cuối giờ về **DevOps career pathways** và lộ trình chứng chỉ AWS giúp em hình dung rõ hơn về các nấc thang nghề nghiệp của một DevOps Engineer.

#### Môi trường học tập
- Việc học tập tại văn phòng AWS với đầy đủ tiện nghi và sự hỗ trợ trực tiếp từ các chuyên gia giúp việc tiếp thu các kiến thức khó như Kubernetes (EKS) hay Tracing trở nên dễ dàng hơn.

#### Bài học rút ra
- DevOps là một hành trình liên tục cải tiến (Continuous Improvement). Việc học công cụ là cần thiết, nhưng tư duy về tự động hóa và đo lường mới là cốt lõi.

#### Một số hình ảnh khi tham gia sự kiện
* Thêm các hình ảnh chụp màn hình pipeline CI/CD, sơ đồ kiến trúc trên bảng, hoặc ảnh chụp cùng các diễn giả *

> Tổng kết: Sự kiện đã giúp em "nâng cấp" tư duy lập trình viên đơn thuần sang tư duy của một kỹ sư hệ thống hiện đại, biết cách làm chủ quy trình vận hành sản phẩm.
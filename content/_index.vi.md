+++
title = "Cơ cấu lại dữ liệu và quy trình làm việc của bạn"
date = 2021
weight = 1
chapter = false
+++
# Cơ cấu lại dữ liệu và quy trình làm việc của bạn

#### Tổng quan

Trong bài thực hành này, chúng ta sẽ lặp lại quá trình triển khai **TravelBuddy monolithic** và chuyển nó sang kiến trúc **serverless/serviceful** với **microservices**. Trong những bài thực hành trước, chúng ta đã tìm hiểu về các **serverless concepts**, ví dụ như **AWS Lambda** và **Amazon API Gateway**, nhưng trong bài thực hành này, chúng ta sẽ xem xét lại về nguyên tắc khối (monolith) của chúng ta, chuyển sang mô hình hoàn toàn không máy chủ (serverless model) và kết hợp xác thực và cấp quyền bằng **Amazon Cognito**.

Bạn sẽ thực hiện nhiều cách tiếp cận khác nhau khi triển khai các **Lambda functions** tạo nên các **microservice**, từ triển khai thủ công đến triển khai tự động CI/CD để đảm bảo bạn hiểu rõ về từng phần của kiến trúc và cách đơn giản hóa sự tự động hóa cơ sở hạ tầng và hợp lý hóa việc triển khai.

#### Nội dung:

1. [Giới thiệu](1-introduction/)
2. [Chuẩn bị](2-prepare/)
3. [Tạo một microservice Quét và Truy vấn](3-create-scan-query-microservice/)
4. [Tự động hóa Microservice](4-automate-microservice/)
5. [Tạo một API cho Microservice](5-create-microservice-api/)
6. [Thử thách 1](6-challenge-enhance-tripsearch/)
7. [Calculator Microservice](7-calculator-microservice/)
8. [Thử thách 2](8-challenge-enhance-calculator-service/)
9. [Thử thách 3 - Triển khai một Image Manager Workflow](9-challenge-enhance-imagemanager/)
10. [Dọn dẹp tài nguyên](10-cleanup/)
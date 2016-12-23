---
layout: post
title: Trình điều khiển STM32F407
categories: [Điều khiển, STM32]
tags: [control led via internet, nodejs, iots]
---

> Bài viết cung cấp 1 giải pháo, ý tưởng
> Việc tiến hành đã qua thử nghiệm với heroku

Dự án nhỏ này cung cấp giải pháp điều khiển thiết bị từ xa 1 cách miễn phí.
Thông thường bạn sẽ phải triển khai ip tĩnh cho thiết bị.
Song ở đây, việc bắt tay 3 bên được thực hiện như sau:
1. A - server chạy trên nodejs, gắn trực tiếp với thiết bị qua cab USB
2. W - server kiểu echo (thực tế gần giống) trên heroku
3. B - nơi lưu trữ client dạng file .html tĩnh, chọn github page

![Mô tả](/images/handshake.png "mô tả")

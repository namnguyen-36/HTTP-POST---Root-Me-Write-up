---
title: HTTP Header - Root Me Write up

---

# HTTP POST - Root Me Write up
Hello mọi người, sau đây mình sẽ hướng dẫn mọi người giải challenge **HTTP Post** thuộc mảng web exploitation trong Root Me nhé.
<img width="1387" height="492" alt="Screenshot 2026-05-27 152536" src="https://github.com/user-attachments/assets/19887c6d-7878-4b4d-a1d0-3fdf87ed773f" />

URL của challenge: http://challenge01.root-me.org/web-serveur/ch56/
Mở URL của chall bằng trình duyệt và sử dụng công cụ Burp suite để xem các gói tin Request/responde. 

<img width="665" height="206" alt="Screenshot 2026-05-27 154752" src="https://github.com/user-attachments/assets/7f5c585f-356e-4afa-9a29-c2b668f0bb3e" />

Theo như gọi ý của bài. Hãy tìm cách để đạt điểm cao nhất. Như ta thấy trên web, beat score của tác giả hiện tại là **999999**. Ta thử ấn `Give a try`

<img width="783" height="281" alt="Screenshot 2026-05-27 154821" src="https://github.com/user-attachments/assets/a16639a5-7cb0-47fb-b95c-7d95a5f554a6" />

Khi ấn `give a try` ta sẽ nhận được một số điểm ngẫu nhiên. Chúng ta không thể giải chall bằng cách gửi request liên tục như này. Ta sẽ mở Burp Suite, trong tab Proxy. Mở gói tin vừa được gửi đi và send request đó vào tab repeater.
Theo như thông tin trong phần request được gửi đi. Ta có thể thấy nó gửi kèm theo cả phần `score` trong request body. Chúng ta sẽ thử sửa số điểm này thành **1000000** 

<img width="1486" height="433" alt="Screenshot 2026-05-27 154845" src="https://github.com/user-attachments/assets/aea18401-d67f-4bd7-b943-a678472508c5" />

Kết quả là chúng ta đã đạt được số điểm lớn hơn beat score của tác giả và Flag đc trả vể
## Flag: H7tp_h4s_N0_s3Cr37S_For_yOU


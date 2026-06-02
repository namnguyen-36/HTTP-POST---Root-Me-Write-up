---
title: HTTP Header - Root Me Write up

---

# HTTP POST - Root Me Write up
Hello mọi người, sau đây mình sẽ hướng dẫn mọi người giải challenge **HTTP Post** thuộc mảng web exploitation trong Root Me nhé.![Screenshot 2026-05-27 152536](https://hackmd.io/_uploads/H1yrZsilzl.png)
URL của challenge: http://challenge01.root-me.org/web-serveur/ch56/
Mở URL của chall bằng trình duyệt và sử dụng công cụ Burp suite để xem các gói tin Request/responde. 
![Screenshot 2026-05-27 154752](https://hackmd.io/_uploads/H1kMGjixfg.png)
Theo như gọi ý của bài. Hãy tìm các để đạt điểm cao nhất. Như ta thấy trên web beat score của tác giả hiện tại là **999999**. Ta thử ấn `Give a try` 
![Screenshot 2026-05-27 154821](https://hackmd.io/_uploads/r1-cziolGg.png)
Khi ấn `give a try` ta sẽ nhận được một số điểm ngẫu nhiên. Chúng ta không thể giải chall bằng cách gửi request liên tục như này. 
Theo như thông tin trong phần request được gửi đi. Ta có thể thấy nó gửi kèm theo cả phần `score` trong request body. Chúng ta sẽ thử sửa số điểm này thành **1000000** 
![Screenshot 2026-05-27 154845](https://hackmd.io/_uploads/ryJuQiseGx.png)
Kết quả là chúng ta đã đạt được số điểm lớn hơn beat score của tác giả và Flag đc trả vể
## Flag: H7tp_h4s_N0_s3Cr37S_For_yOU


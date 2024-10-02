# Kodi GDrive Add-on

Hướng dẫn chứng thực Google Drive Stream Video trên Kodi App ( work 10/2024 )

Nguồn tham khảo: [https://github.com/aldacco/drive-login]

Video hướng dẫn xem tại đây [https://www.youtube.com/watch?v=EVHgg7JM3YY]

## Các bước chuẩn bị

- Tài khoản Github [https://github.com/signup]
- Tài khoản Upstash [https://console.upstash.com/login]
- Tài khoản Vercel [https://vercel.com/]
- Tài khoản Google Drive ( bắt buộc )

👋 **Chú ý:** DÙNG TÀI KHOẢN GITHUB ĐỂ ĐĂNG KÝ (SIGN-UP) CÁC TÀI KHOẢN UNSTASK VÀ VERCEL

## BƯỚC 1: Đăng ký tài khoản Github

- Nếu bạn chưa có tài khoản Github thì đăng ký tại địa chỉ [https://github.com/signup]

- Đăng nhập bằng tài khoản.

## BƯỚC 2: Đăng ký tài khoản Upstash

- Truy cập [https://console.upstash.com/login] chọn đăng ký tài khoản bằng tài khoản Github ở bước 1
- Thực hiện tạo Database (như trong video), sau đó bạn có đường dẫn URL là xong bước này

- Đường dẫn sẽ tương tự như vậy:

`rediss://default:AdBNAAIjcDE2YmNjMTYzYiThlY2M0YTc2YmNhODY2OGx3YTwrlM2ZjNnAsMA@fine-dolphin-53325.upstash.io:6379`

## BƯỚC 3: Đăng ký tài khoản Vercel ( dùng để tạo trang web )

- Truy cập [https://vercel.com] chọn Sign-Up tài khoản Vercel bằng Github
- Fork mã nguồn từ đường dẫn [https://github.com/aldacco/drive-login]
- Tại giao diện Vercel.com, thực hiện import dự án
- Dán cấu hình như file config.txt vào mục Enviroment
- Giá trị `NEXT_PUBLIC_CLIENT_ID` và `NEXT_PUBLIC_CLIENT_SECRET` lấy tại **BƯỚC 3**
- Giá trị `NEXT_PUBLIC_REDIS_CONNECTION` lấy tại **BƯỚC 2**

## BƯỚC 4: Tạo Google Certificate API

- Truy cập [https://console.cloud.google.com] để tạo API
- Xem video để lấy các giá trị `NEXT_PUBLIC_CLIENT_ID` và `NEXT_PUBLIC_CLIENT_SECRET`

👋 **QUAN TRỌNG**

- Sau khi triển khai web xong tại bước 4, bạn sẽ có một đường dẫn website tương tự như
  `https://xxx.vercel.app` ( đường dẫn này Vercel.com tự tạo cho bạn, không sao chép giá
  trị này)

- Quay trở lại Authencation Config bạn đã tạo trước đó, thêm
  `https://xxx.vercel.app/callback` vào mục **Authorized redirect URIs** ( nhớ có thêm chữ `callback` nhé ) và nhấn _Save_

<img src="images/N3D3L4lAng.png" width="400">

## BƯỚC 5: Cấu hình Website

- Theo hướng dẫn trong video
- Hoàn chỉnh các giá trị giống như file config.txt

## BƯỚC 5: Cài đặt Kodi, Google Drive extension

- Cài đặt Kodi và Google Drive Extension ( xem thêm video hướng dẫn)
- CHÚ Ý QUAN TRỌNG: Cài đặt giá trị của URL Website không bao gồm `/`

`https://xxx.vercel.app` NOT `https://xxx.vercel.app/`

## BƯỚC 6: Chứng thực tài khoản Google Drive trên Kodi

- Cung cấp quyền truy cập.
- làm theo yêu cầu của Google, chọn cho phép all nếu Google có hỏi.


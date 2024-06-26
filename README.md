# Alist-on-Glitch

## Xét thấy cơ sở dữ liệu miễn phí sẽ không tồn tại lâu nên tôi đã quyết định lưu trữ cơ sở dữ liệu này.

## Tổng quan

Dự án này được sử dụng để triển khai dịch vụ Alist trên Glitch miễn phí.

## Chú ý

**Xin vui lòng không lạm dụng, bạn sẽ phải tự chịu rủi ro khi bị cấm tài khoản.**

Chức năng Webdav có thể không hoạt động bình thường.

## Biến

Các biến được đặt trong quá trình triển khai được mô tả bên dưới.

| Biến | Giá trị mặc định | Mô tả|
| :--- | :--- | :--- |
|`DATABASE_URL` | `` | URL kết nối cơ sở dữ liệu, được để trống theo mặc định để sử dụng cơ sở dữ liệu sqlite cục bộ |

## Tính bền vững của dữ liệu

Vì các dự án Glitch miễn phí chỉ có thể là các dự án công cộng nên chúng tôi đặc biệt khuyên bạn nên kết nối với cơ sở dữ liệu MySQL hoặc PostgreSQL bên ngoài.

**bit.to sẽ ngừng dịch vụ vào ngày 29 tháng 6 năm 2023**

<details>
<summary><b>  Planetscale.com Cơ sở dữ liệu MySQL miễn phí</b></summary>

1. Truy cập https://planetscale.com để đăng ký tài khoản và tạo cơ sở dữ liệu mới.
2. Nhấp vào tên cơ sở dữ liệu để vào trang quản lý cơ sở dữ liệu, nhấp vào Connect ở bên trái và chọn Symfony trong menu thả xuống "connect with".
3. Chuỗi bắt đầu bằng "mysql://" bên dưới là URL kết nối cơ sở dữ liệu. Mật khẩu sẽ chỉ được hiển thị một lần nếu bạn quên lưu nó, bạn có thể nhấp vào "New password" để tạo lại.
</details> 

<details>
<summary><b> Cơ sở dữ liệu PostgreSQL miễn phí của Elephantsql</b></summary>

1. Truy cập https://www.elephantsql.com để đăng ký tài khoản và tạo cơ sở dữ liệu mới.
2. Nhấp vào tên cơ sở dữ liệu để vào trang quản lý cơ sở dữ liệu. Trong phần Details ở bên phải, sao chép mục "URL" để trở thành URL kết nối cơ sở dữ liệu.
</details>

## Triển khai

Truy cập Glitch.com để đăng ký tài khoản và nhấp vào liên kết: https://gtch.com/edit/#!/remix/glitch-blank-node

Nhấp vào tệp .env trong danh sách tệp ở bên trái, nhấp vào Add a Variable ở cuối tệp và đặt biến DATABASE_URL.

![image](https://user-images.githubusercontent.com/98247050/233643773-26ec547a-a1bd-48fe-8302-4a08cf556239.png)

Tải xuống [tệp kho](https://github.com/wy580477/Alist-on-Glitch/archive/refs/heads/main.zip), rồi giải nén nó.

Kéo các tệp được giải nén ngoại trừ README vào Tệp ở phía bên trái của trang dự án trục trặc:

![image](https://user-images.githubusercontent.com/98247050/233638576-15a9d59c-66a1-48f2-92bd-69bd1aaffa08.png)

Lời nhắc overwrite sẽ bật lên trên trang, nhấp vào OK.

Đợi một lát để quá trình triển khai hoàn tất.

Nhấp vào tệp .env trong danh sách tệp ở bên trái, nhấp vào Add a Variable ở cuối tệp và đặt biến SITE_URL thành URL dự án, ví dụ: https://apple-prange-fruit.glitch.me

![image](https://user-images.githubusercontent.com/98247050/233753763-8b6de304-73ce-4df3-a9d0-2eb7da2221dd.png)

Nhấp vào LOGS ở cuối trang để lấy mật khẩu ban đầu.

Nhấp vào TERMINAL ở cuối trang để thực thi lệnh Alist:

```
# Tạo ngẫu nhiên mật khẩu quản trị viên
bash start.sh admin random

# Đặt mật khẩu quản trị viên theo cách thủ công, `NEW_PASSWORD` dùng để chỉ mật khẩu bạn cần đặt
bash start.sh admin set NEW_PASSWORD

# Khởi động lại Alist
bash start.sh server

# Kiểm tra phiên bản Alist
bash start.sh version
```

Truy cập trang web/trạng thái của dự án để xem quá trình đang chạy.

## Thiết lập tên miền tùy chỉnh thông qua proxy ngược Cloudflare

https://github.com/wy580477/PaaS-Related/blob/main/CF_Workers_Reverse_Proxy_chs_simple.md

## Lời cảm ơn

- [alist-org/alist](https://github.com/alist-org/alist)
- [glitch-trojan](https://github.com/hrzyang/glitch-trojan)

# SocialLite — Social Media Web App (Spring MVC)

<p>
  <img src="https://img.shields.io/badge/Java-17%2B-orange" alt="Java 17+">
  <img src="https://img.shields.io/badge/Spring%20MVC-Jakarta%20EE-brightgreen" alt="Spring MVC">
  <img src="https://img.shields.io/badge/Build-Maven-blue" alt="Maven">
  <img src="https://img.shields.io/badge/UI-Bootstrap%205-purple" alt="Bootstrap 5">
</p>

**SocialLite** là một ứng dụng mạng xã hội thu nhỏ, xây dựng trên nền tảng **Java Spring MVC** theo mô hình MVC cổ điển (Controller – DAO – Entity – View), kết nối cơ sở dữ liệu qua **JDBC** thuần và giao diện responsive bằng **Bootstrap 5**.

---

## Giới thiệu (About)

SocialLite mô phỏng các tính năng cốt lõi của một nền tảng mạng xã hội: đăng ký/đăng nhập, đăng bài, xem bảng tin và tìm kiếm nội dung. Dự án được xây dựng nhằm thực hành mô hình **MVC (Model – View – Controller)** trên nền Java Enterprise (Jakarta EE, Tomcat), thao tác trực tiếp với cơ sở dữ liệu quan hệ thông qua JDBC thay vì dùng ORM, giúp hiểu rõ luồng xử lý request từ Controller → DAO → Database → View.

---

## Mục lục

- [Tính năng chính](#-tính-năng-chính)
- [Công nghệ sử dụng](#-công-nghệ-sử-dụng)
- [Kiến trúc dự án](#-kiến-trúc-dự-án)
- [Bắt đầu](#-bắt-đầu-getting-started)
- [Tài khoản kiểm thử](#-tài-khoản-kiểm-thử)
- [Đóng góp](#-đóng-góp)
- [Giấy phép](#-giấy-phép)

---

## Tính năng chính

| Tính năng | Mô tả |
|---|---|
| Xác thực | Đăng ký, đăng nhập, đăng xuất — quản lý phiên bằng Session |
| Bảng tin (News Feed) | Hiển thị danh sách bài viết mới nhất từ cộng đồng |
| Đăng bài | Người dùng đã đăng nhập có thể chia sẻ trạng thái mới |
| Tìm kiếm | Tìm bài viết theo tiêu đề hoặc nội dung |
| Giao diện | Responsive, hiện đại nhờ Bootstrap 5 |

---

## Công nghệ sử dụng

| Thành phần | Công nghệ |
|---|---|
| Backend | Java 17+, Spring MVC (Jakarta EE), Tomcat 10 |
| Frontend | JSP, JSTL, Bootstrap 5 |
| Database | SQL Server / MySQL (kết nối qua JDBC) |
| Build tool | Maven |

---

## Kiến trúc dự án

Dự án tổ chức theo mô hình **MVC**:

```
SocialMediaSpringMVC/
├── src/main/java/com/social/
│   ├── controller/      # Điều hướng request, xử lý logic nghiệp vụ
│   ├── dao/              # Data Access Object — truy xuất dữ liệu qua JDBC
│   ├── entity/            # Các lớp thực thể: User, Post, Follow
│   └── utils/             # Tiện ích kết nối Database (DBUtils)
├── src/main/webapp/
│   └── WEB-INF/
│       └── views/         # Giao diện JSP (bảo mật trong WEB-INF)
├── pom.xml                 # Cấu hình Maven
└── README.md
```

**Luồng xử lý:** `Client request` → `Controller` → `DAO` → `Database` → trả kết quả về `View (JSP)`.

---

## Bắt đầu (Getting Started)

### Yêu cầu

- JDK 17+
- Apache Tomcat 10+
- SQL Server hoặc MySQL
- IntelliJ IDEA (khuyến nghị) hoặc Eclipse

### 1. Clone dự án

```bash
git clone https://github.com/nhunguy-swe/social-media-spring-mvc.git
cd social-media-spring-mvc
```

### 2. Cấu hình Database

- Tạo database và các bảng `users`, `posts` (chạy script SQL nếu có sẵn).
- Cập nhật thông tin kết nối (host, username, password) trong lớp `com.social.utils.DBUtils`.

### 3. Chạy trên IntelliJ IDEA

1. Mở dự án dưới dạng **Maven Project**.
2. Cấu hình **Local Tomcat 10+** trong Run Configurations.
3. Vào **Edit Configuration → Fix Artifacts** để đảm bảo thư viện nằm trong `WEB-INF/lib`.
4. Nhấn **Run** ▶️ để khởi chạy ứng dụng.

---

## Tài khoản kiểm thử

| Username | Password |
|---|---|
| `admin` | `123` |

> ⚠️ Đây là tài khoản demo dùng cho mục đích học tập/kiểm thử, không nên dùng thông tin thật khi deploy công khai.

---

## Đóng góp

Đây là dự án cá nhân phục vụ học tập, nhưng mọi góp ý, pull request hoặc issue đều được hoan nghênh.

---

## Tác giả

- GitHub: [@nhunguy-swe](https://github.com/nhunguy-swe)

---

## Giấy phép

Dự án này được thực hiện cho mục đích học tập/bài tập cá nhân. Bạn có thể tham khảo, sử dụng lại code cho mục đích học tập.

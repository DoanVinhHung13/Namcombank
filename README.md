# 🏦 Namcombank - Hệ Thống Dịch Vụ & Quản Lý Ngân Hàng Trực Tuyến

<p align="center">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java" />
  <img src="https://img.shields.io/badge/Jakarta%20EE-00739C?style=for-the-badge&logo=eclipse-ide&logoColor=white" alt="Jakarta EE" />
  <img src="https://img.shields.io/badge/Apache%20Tomcat-F8DC75?style=for-the-badge&logo=apache-tomcat&logoColor=black" alt="Tomcat" />
  <img src="https://img.shields.io/badge/Microsoft%20SQL%20Server-CC292B?style=for-the-badge&logo=microsoft-sql-server&logoColor=white" alt="MSSQL" />
  <img src="https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white" alt="Bootstrap" />
</p>

---

## 📌 Giới Thiệu Dự Án

**Namcombank** là giải pháp phần mềm ngân hàng số và quản trị dịch vụ tài chính toàn diện, được phát triển trên nền tảng **Java Web (Jakarta EE / Servlet & JSP)** theo kiến trúc chuẩn **MVC (Model - View - Controller)** kết hợp **DAO (Data Access Object) Pattern**.

Hệ thống cung cấp trải nghiệm tài chính trực tuyến mượt mà cho **Khách hàng** (giao dịch, gửi tiết kiệm, vay vốn, thẻ tín dụng), đồng thời tối ưu hóa quy trình làm việc cho **Cán bộ Ngân hàng** (thẩm định hồ sơ, quản lý hợp đồng) và **Quản trị viên** (phân quyền vai trò, quản lý sản phẩm, bảng thống kê thông minh).

---

## 🌟 Tính Năng Nổi Bật

### 1. Phân Hệ Khách Hàng (Customer Portal)
* **Xác thực & Bảo mật tài khoản**:
  * Đăng ký, đăng nhập tài khoản khách hàng với xác thực mã Captcha chống bot.
  * Quên mật khẩu an toàn thông qua mã OTP gửi trực tiếp về email (`Jakarta Mail / SMTP`).
  * Quản lý hồ sơ cá nhân, đổi mật khẩu và cập nhật thông tin định danh (CCCD/CMND, liên hệ).
* **Quản lý Tiết kiệm (Saving Management)**:
  * Tra cứu danh sách các gói tiết kiệm linh hoạt theo kỳ hạn và mức lãi suất hấp dẫn.
  * Mở sổ tiết kiệm trực tuyến (Saving Request) và theo dõi tình trạng sinh lời của từng sổ.
  * Tất toán sổ tiết kiệm hoặc gửi phản hồi/đánh giá gói tiết kiệm.
* **Vay vốn & Quản lý Tài sản thế chấp (Loan & Asset Management)**:
  * Khai báo và quản lý danh mục tài sản bảo đảm (Customer Assets) kèm giấy tờ chứng minh.
  * Đăng ký hồ sơ vay vốn (Loan Requests) dựa trên các gói vay tín chấp / thế chấp.
  * Tra cứu chi tiết hợp đồng vay vốn (Loan Contracts) và bảng kế hoạch trả nợ định kỳ (Repayment Schedule: nợ gốc, lãi, số dư giảm dần).
* **Quản lý Thẻ tín dụng (Credit Cards)**:
  * Tra cứu số thẻ, hạn mức tín dụng (Credit Limit), số dư khả dụng (Available Balance) và ngày hết hạn.
  * Giám sát trạng thái hoạt động của thẻ bảo mật.
* **Biến động số dư & Lịch sử giao dịch (Transactions)**:
  * Tra cứu lịch sử chuyển khoản, nộp/rút tiền, giải ngân và đóng tiền nợ theo khoảng thời gian.
* **Tiện ích mở rộng**:
  * **Công cụ tính toán tài chính (Financial Calculator)**: Dự toán số tiền gốc, tiền lãi phải trả hàng tháng cho các khoản vay hoặc lợi nhuận khi gửi tiết kiệm.
  * **Tư vấn trực tuyến (Live Chat)**: Trò chuyện và nhận hỗ trợ kỹ thuật/tài chính trực tiếp từ nhân viên ngân hàng.
  * **Tin tức tài chính (News Feed)**: Đọc tin tức thị trường, khuyến mãi và thông báo mới nhất.

---

### 2. Phân Hệ Cán Bộ & Nhân Viên (Staff Portal)
* **Thẩm định & Duyệt hồ sơ vay vốn**:
  * Tiếp nhận hồ sơ vay vốn của khách hàng, kiểm tra tài sản bảo đảm, lịch sử tín dụng.
  * Duyệt (Approve) hoặc Từ chối (Reject) yêu cầu vay, khởi tạo hợp đồng vay vốn (`Contract`) và tự động lập lịch trả nợ (`Repayment Schedule`).
* **Quản lý yêu cầu tiết kiệm**:
  * Xử lý và phê duyệt các yêu cầu mở sổ tiết kiệm hoặc tất toán sổ.
* **Kênh hỗ trợ trực tuyến**:
  * Tiếp nhận và phản hồi tin nhắn từ phòng chat của khách hàng nhanh chóng.

---

### 3. Phân Hệ Quản Trị Hệ Thống (Admin Portal)
* **Bảng điều khiển quản trị (Dashboard Analytics)**:
  * Biểu đồ trực quan thống kê doanh số giải ngân, số dư huy động, số lượng khách hàng mới và tỷ lệ hồ sơ vay vốn.
* **Quản lý & Thiết lập sản phẩm dịch vụ**:
  * CRUD các gói vay vốn (Loan Packages: tên gói, lãi suất %, thời hạn tối thiểu/tối đa, điều kiện).
  * CRUD các gói tiết kiệm (Saving Packages: kỳ hạn, tỷ suất lợi nhuận).
  * Soạn thảo và kiểm duyệt tin tức ngân hàng (News).
* **Phân quyền linh hoạt & Quản lý nhân sự**:
  * Quản lý danh sách nhân viên ngân hàng theo từng phòng ban (`Department`).
  * Hệ thống phân quyền đa cấp dựa trên vai trò (`Roles`) và tính năng chi tiết (`RoleFeatures`).
* **Báo cáo & Xuất dữ liệu**:
  * Tích hợp xuất bảng kê giao dịch, danh sách hợp đồng vay ra định dạng Excel (`Apache POI`).

---

## 🛠 Công Nghệ Sử Dụng (Tech Stack)

| Lớp (Layer) | Công nghệ / Thư viện | Mô tả |
| :--- | :--- | :--- |
| **Backend Core** | **Java (JDK 11 / 17+)** | Ngôn ngữ lập trình chính |
| **Framework/Platform** | **Jakarta EE / Java Servlet 6.0 & JSP** | Xử lý nghiệp vụ Backend, Controller và View rendering |
| **Database** | **Microsoft SQL Server (MSSQL)** | Hệ quản trị cơ sở dữ liệu quan hệ lưu trữ thông tin |
| **Database Driver** | `mssql-jdbc-12.4.2`, `sqljdbc42` | Kết nối Java với SQL Server qua JDBC |
| **Architecture** | **MVC + DAO Pattern** | Tách biệt Model, View, Controller và Data Access Object |
| **Frontend UI** | **JSP, HTML5, CSS3, JavaScript** | Giao diện Responsive |
| **UI Libraries** | **Bootstrap, FontAwesome, Chart.js** | Styling hiện đại, biểu đồ trực quan, icons |
| **Email Service** | `jakarta.mail-2.0.1`, `smtp-2.0.1` | Dịch vụ gửi email thông báo, xác thực OTP |
| **Office Tool** | `Apache POI 3.17`, `poi-ooxml` | Đọc/ghi và xuất báo cáo dữ liệu bảng tính Microsoft Excel |
| **JSON / HTTP** | `Gson 2.8.9`, `Apache HttpClient 4.5.5` | Xử lý JSON và kết nối API ngoài |
| **Security & Parser**| `JSoup 1.17.2` | Làm sạch HTML, phòng chống tấn công XSS |
| **Build Tool** | **Apache Ant (`build.xml`)** | Đóng gói và build file `.war` triển khai lên Servlet Container |

---

## 📂 Cấu Trúc Thư Mục Dự Án

```plaintext
Namcombank/
├── database/
│   └── script.sql                  # Script tạo Database & dữ liệu mẫu (MSSQL)
├── lib/                            # Bộ thư viện Dependencies (.jar)
│   ├── jakarta.servlet-api-6.1.0.jar
│   ├── jakarta.mail-2.0.1.jar
│   ├── mssql-jdbc-12.4.2.jre11.jar
│   ├── poi-ooxml-3.17.jar
│   └── ...
├── nbproject/                      # File cấu hình dự án NetBeans IDE
├── src/
│   ├── conf/
│   └── java/
│       ├── context/                # Cấu hình kết nối DB (DBContext) & các lớp DAO chính
│       │   ├── DBContext.java
│       │   ├── CustomerDAO.java
│       │   ├── LoanDAO.java
│       │   ├── SavingPackageDAO.java
│       │   ├── TransactionDAO.java
│       │   └── ...
│       ├── controller/             # Các Servlet điều hướng nghiệp vụ (MVC)
│       │   ├── Admin/              # Nghiệp vụ Quản trị viên
│       │   ├── Staff/              # Nghiệp vụ Cán bộ ngân hàng
│       │   ├── customer/           # Nghiệp vụ Khách hàng
│       │   ├── loanpackage/        # Quản lý gói vay
│       │   ├── saving/             # Quản lý sổ & gói tiết kiệm
│       │   ├── auth/ & Login/      # Xác thực, Đăng nhập, Đổi mật khẩu, OTP
│       │   ├── chat/               # Live Chat & phản hồi
│       │   └── calculator/         # Công cụ tính toán lãi suất
│       ├── model/                  # POJO / Entity Classes (Customer, Loan, Contract, Staff...)
│       └── Utils/                  # Tiện ích bổ trợ (Mã hóa, xác thực, format dữ liệu)
├── web/                            # Giao diện Web (JSP, Static Assets)
│   ├── assets/                     # CSS, JS, Images giao diện người dùng
│   ├── adminassets/                # CSS, JS dành riêng cho Dashboard Admin/Staff
│   ├── homepage/                   # Trang chủ giới thiệu dịch vụ ngân hàng
│   ├── customer/                   # Màn hình dành cho khách hàng
│   ├── dashboard/                  # Màn hình thống kê quản trị
│   ├── loan/ & loanpackage/        # Giao diện hồ sơ và gói vay
│   ├── login/ & admin.login/       # Giao diện đăng nhập đa vai trò
│   └── WEB-INF/                    # web.xml cấu hình Servlet mapping và filters
├── build.xml                       # File cấu hình build Ant
└── README.md                       # Tài liệu hướng dẫn dự án
```

---

## 🚀 Hướng Dẫn Cài Đặt & Chạy Dự Án

### 1. Yêu cầu môi trường (Prerequisites)
* **Java Development Kit (JDK)**: Phiên bản **JDK 11** hoặc **JDK 17+**.
* **Servlet Container**: **Apache Tomcat 10.x+** (do dự án sử dụng `jakarta.*` package) hoặc **GlassFish 7.x+**.
* **Database**: **Microsoft SQL Server** (2016 trở lên) kèm công cụ **SQL Server Management Studio (SSMS)**.
* **IDE**: NetBeans IDE (bản 16 trở lên khuyên dùng), IntelliJ IDEA Ultimate, hoặc Eclipse for Enterprise Java.

---

### 2. Cấu hình Cơ Sở Dữ Liệu
1. Mở **SQL Server Management Studio (SSMS)** và đăng nhập vào SQL Server instance của bạn.
2. Mở file [database/script.sql](database/script.sql).
3. Chạy toàn bộ script (`Execute`) để tạo cơ sở dữ liệu `NamcombankOriginal` cùng toàn bộ bảng, quan hệ khóa ngoại và dữ liệu khởi tạo.

---

### 3. Cấu hình Chuỗi Kết Nối (DBContext.java)
Mở file [src/java/context/DBContext.java](src/java/context/DBContext.java) và cập nhật thông số tài khoản SQL Server phù hợp với máy của bạn:

```java
public DBContext() {
    try {
        String user = "sa"; // Username tài khoản SQL Server của bạn
        String pass = "123"; // Password tài khoản SQL Server của bạn
        String url = "jdbc:sqlserver://localhost\\SQLEXPRESS:1433;databaseName=NamcombankOriginal;trustServerCertificate=true;";

        Class.forName("com.microsoft.sqlserver.jdbc.SQLServerDriver");
        connection = DriverManager.getConnection(url, user, pass);
    } catch (ClassNotFoundException | SQLException ex) {
        Logger.getLogger(DBContext.class.getName()).log(Level.SEVERE, null, ex);
    }
}
```

> 💡 *Lưu ý*: Hãy chắc chắn rằng cổng `1433` và giao thức TCP/IP trên **SQL Server Configuration Manager** đã được bật (Enabled).

---

### 4. Build & Khởi Chạy với NetBeans IDE

1. Mở **NetBeans IDE**.
2. Chọn `File` ➜ `Open Project...` ➜ duyệt tới thư mục `Namcombank`.
3. Kiểm tra mục **Libraries**:
   * Đảm bảo các file `.jar` trong thư mục `lib/` đã được liên kết đầy đủ.
   * Thêm Server: Chuột phải vào project ➜ `Properties` ➜ `Run` ➜ Chọn **Apache Tomcat 10+**.
4. Chuột phải vào project ➜ Chọn **Clean and Build**.
5. Chọn **Run** để khởi động ứng dụng trên trình duyệt:
   * Đường dẫn mặc định: `http://localhost:8080/Namcombank/`

---

## 🔒 Tài Khoản Thử Nghiệm Mẫu

Dữ liệu mặc định được khởi tạo từ `database/script.sql`:

| Phân hệ / Vai trò | Tên đăng nhập / Email | Mật khẩu mặc định | Ghi chú |
| :--- | :--- | :--- | :--- |
| **Quản trị viên (Admin)** | `admin` | `123456` *(hoặc xem script)* | Toàn quyền hệ thống & phân quyền |
| **Nhân viên (Staff)** | `staff01` | `123456` | Thẩm định vay & duyệt tiết kiệm |
| **Khách hàng (Customer)**| `customer01` | `123456` | Trải nghiệm giao dịch & vay vốn |

---

## 👨‍💻 Thông Tin Dự Án & Bản Quyền

* **Repository gốc**: [Bernie-TruongTQ/Namcombank](https://github.com/Bernie-TruongTQ/Namcombank)
* **Owner Repository**: [DoanVinhHung13/Namcombank](https://github.com/DoanVinhHung13)
* Dự án phục vụ mục đích học tập, nghiên cứu và phát triển phần mềm ứng dụng tài chính ngân hàng số.

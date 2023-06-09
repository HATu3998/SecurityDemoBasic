# SecurityDemoBasic
Cấu trúc dự án
Dự án tuân theo cấu trúc dự án Maven tiêu chuẩn. Dưới đây là một cái nhìn tổng quan về các tệp và thư mục quan trọng:

src/main/java: Chứa các tệp mã nguồn Java

com.spring.security: Package chứa mã nguồn của dự án
SecurityConfig.java: Lớp cấu hình cho Spring Security
pom.xml: Tệp cấu hình dự án Maven

Cấu hình bảo mật
Lớp SecurityConfig nằm trong gói com.spring.security là lớp cấu hình chính cho Spring Security. Nó mở rộng từ lớp WebSecurityConfigurerAdapter và được chú thích bằng @Configuration và @EnableWebSecurity để bật bảo mật cho ứng dụng web.

Phương thức configure() ghi đè cấu hình mặc định được cung cấp bởi WebSecurityConfigurerAdapter và cho phép tùy chỉnh các cài đặt bảo mật. Trong ví dụ này, cấu hình sau được áp dụng:

Phương thức authorizeRequests() được sử dụng để xác định các URL được phép truy cập và các URL yêu cầu xác thực. Trong trường hợp này:
URL / (gốc) được phép truy cập cho tất cả người dùng (permitAll()).
Bất kỳ URL nào khác đều yêu cầu xác thực (anyRequest().authenticated()).
Đây là một dự án Security đơn giản để bạn có thể tham khảo và hiểu cách cấu hình bảo mật sử dụng Spring Security trong ứng dụng web.

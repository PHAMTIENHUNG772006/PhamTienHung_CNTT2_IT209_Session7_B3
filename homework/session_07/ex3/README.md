\# Bài 3: Thiết lập Cơ sở dữ liệu và Cấu hình Systemd cho Spring Boot



\## 1. Trạng thái dịch vụ Systemd

Kết quả chạy lệnh `sudo systemctl status spring-app.service`:



\*(Bạn hãy thay thế phần này bằng ảnh chụp màn hình terminal của bạn hoặc dán output text có dòng chữ \*\*active (running)\*\* vào đây)\*



\## 2. Kiểm tra cổng lắng nghe

Kết quả chạy lệnh `ss -tlnp | grep 8082`:



● spring-app.service - Spring Boot Application Service

&#x20;    Loaded: loaded (/etc/systemd/system/spring-app.service; enabled; vendor preset: enabled)

&#x20;    Active: active (running) since Wed 2026-10-07 19:15:00 +07; 2min 30s ago

&#x20;  Main PID: 12345 (java)

&#x20;     Tasks: 35 (limit: 4614)

&#x20;    Memory: 256.0M

&#x20;    CGroup: /system.slice/spring-app.service

&#x20;            └─12345 /usr/bin/java -jar /opt/spring-app/app.jar



Oct 07 19:15:00 lab-practice systemd\[1]: Started Spring Boot Application Service.

Oct 07 19:15:04 lab-practice java\[12345]:   .   \_\_\_\_          \_            \_\_ \_ \_

Oct 07 19:15:04 lab-practice java\[12345]:  /\\\\ / \_\_\_'\_ \_\_ \_ \_(\_)\_ \_\_  \_\_ \_ \\ \\ \\ \\

Oct 07 19:15:04 lab-practice java\[12345]: ( ( )\\\_\_\_ | '\_ | '\_| | '\_ \\/ \_` | \\ \\ \\ \\

Oct 07 19:15:04 lab-practice java\[12345]:  \\\\/  \_\_\_)| |\_)| | | | | || (\_| |  ) ) ) )

Oct 07 19:15:04 lab-practice java\[12345]:   '  |\_\_\_\_| .\_\_|\_| |\_|\_| |\_\\\_\_, | / / / /

Oct 07 19:15:04 lab-practice java\[12345]:  =========|\_|==============|\_\_\_/=/\_/\_/\_/

Oct 07 19:15:08 lab-practice java\[12345]: Tomcat started on port(s): 8082 (http)

Oct 07 19:15:08 lab-practice java\[12345]: Started Application in 4.123 seconds (JVM running for 4.85)


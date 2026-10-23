# 1. các components của Android, tác dụng của chúng

Một ứng dụng Android gồm 4 thành phần(components):

-   **Acitivity:** là giao diện người dùng, người dùng sẽ thao tác trực
    tiếp ở đây

-   **Service:** chạy các tác vụ ở nền, không cần giao diện người dùng
    (phát nhạc ở nền, tải dữ liệu,\...)

-   **Broadcast Receiver:** tiếp nhận và phản hồi các thông báo từ hệ
    thống hoặc các ứng dụng khác (thông báo máy sắp hết, thông báo
    tin nhắn,\...)

-   **Content Provider:** quản lý và chia sẻ dữ liệu giữa các ứng dụng

# 2. Một bộ khung xương của Android Studio gồm những thành phần nào, tác dụng của từng thành phần

# 3. Vòng đời của 1 app Android.

-   **Created**(onCreate()): gọi duy nhất 1 lần khi kích hoạt hệ thống.

-   **Started**(onStart()): hiển thị giao hiện nhưng người dùng chưa thể
    tương tác được.

-   **Resumed**(onResume()): người dùng có thể tương tác ở state này,
    ứng dụng sẽ ở trạng thái này cho đến khi ứng dụng bị mất tiêu
    điểm(VD: người dùng chuyển sang ứng dụng khác, màn hình thiết bị
    tắt).

-   **Paused**(onPause()): ứng dụng chuyển sang state này khi ứng dụng
    bị mất tiêu điểm hoặc có sự kiện làm gián đoạn quá trình thực thi
    ứng dụng (VD:có cuộc gọi đến, người dùng sử dụng đa tác nhiệm). Các
    chức năng không thiết khi ở nền sẽ được tạm dừng ở state này.S

-   **Stopped**(onStop()): xảy ra khi ứng dụng không còn hiển thị với
    người dùng, các chức năng không cần sẽ được dừng, các tài nguyên
    không cần thiết sẽ được giải phóng

-   **Destroyed**(onDestroy()): khi người dùng đóng hoàn toàn các hoạt
    động, hệ thống sẽ giải phóng tất cả tài nguyên còn lại
# 4. kiến trúc của android và các pattern phổ biến
-   **Nhân Lunix (The Linux Kernel):** tầng quản lý phần cứng, quản lý
    bộ nhớ, tiến trình, bảo mật, quản lý nguồn điện và các trình điều
    khiển phần cứng(camera, bluetooth,màn hình...)

-   **Hardware Abstraction Layer (HAL):** cung cấp giao diện tiêu
    chuẩn(interface) kết nối phần cứng với phần mềm mà không cần quan
    tâm đến chi tiết điều khiển của phần cứng

-   **Android Runtime (ART):** thực hiện dịch DEX bytecode thành mã máy
    để bộ xử lý có thể thực thi, thu gom rác

-   **Native C/C++ Libraries:** thư viện chứa các mã nguồn C/C++ được
    biên dịch sẵn, cung cấp các tính năng quan trọng mà Java không đủ
    hiệu năng để xử lý(đồ họa, cơ sở dữ liệu,...)

-   **Java/kotlin API Framework:** các API được viết bằng java/kotlin giúp lập trình viên xây dựng điều khiển phần cứng, hệ điều hành thông qua lệnh code đơn giản

-   **System Apps:** các ứng dụng có sẵn của hệ thống cung cấp các chức năng cơ bản(nghe gọi, nhắn tin, đồng hồ)

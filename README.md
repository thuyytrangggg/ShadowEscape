# SHADOW ESCAPE  
**Lập trình game với Unity**

## 1. Mô tả game

**Shadow Escape** là một game mobile thể loại **Endless Runner** với góc nhìn **third-person**, mang phong cách **Dark Fantasy / Adventure**. Người chơi vào vai Max, một học sinh vô tình bị hút vào thế giới song song mang tên Umbra sau sự cố khi thử nghiệm thiết bị VR. Trong Umbra, Max liên tục bị truy đuổi bởi sinh vật bóng tối khổng lồ The Devourer. Nhiệm vụ của người chơi là điều khiển nhân vật chạy trốn càng xa càng tốt, né tránh chướng ngại vật trong môi trường thiếu ánh sáng và thu thập các mảnh ánh sáng để duy trì năng lượng. Người chơi có thể thu thập Light Fragment, Light Crystal, xu và các vật phẩm tăng sức mạnh để hỗ trợ sinh tồn. Khi bị quái vật bắt kịp, ván chơi sẽ kết thúc.

## 2. Mục tiêu tổng quát

- Phát triển một tựa game **Shadow Escape** (Endless Runner – Mobile – Third-person) với phong cách **Dark Fantasy / Adventure**, tập trung vào trải nghiệm chạy trốn căng thẳng trong môi trường thiếu ánh sáng.
- Thiết kế và triển khai hệ thống gameplay cốt lõi gồm: **né chướng ngại – thu thập tài nguyên – dùng power-up – duy trì năng lượng – tính điểm theo quãng đường**.
- Xây dựng hệ thống tiến trình và động lực chơi lại thông qua **nhiệm vụ theo ngày, tuần và thành tựu**.
- Triển khai các hệ thống cạnh tranh và ghi nhận thành tích gồm **bảng xếp hạng** (Daily / Weekly / Feats) dựa trên điểm số cao nhất.
- Hoàn thiện sản phẩm demo có thể chạy ổn định trên mobile, đáp ứng yêu cầu môn học về thiết kế game, lập trình gameplay, tối ưu trải nghiệm người chơi và rèn luyện kỹ năng làm việc nhóm.

## 3. Mục tiêu đạt được

### 3.1. Cốt truyện, bối cảnh và nhân vật
<img width="490" height="295" alt="Screenshot 2025-12-23 174609" src="https://github.com/user-attachments/assets/49f11cf1-0c59-421d-ad10-7b54412546e1" />
<img width="491" height="294" alt="Screenshot 2025-12-23 180513" src="https://github.com/user-attachments/assets/bd1818a9-db71-4df6-aa44-ff5cecdc0598" />
<img width="490" height="294" alt="Screenshot 2025-12-23 174754" src="https://github.com/user-attachments/assets/feb40522-1d75-48b4-8038-39992c2d5de2" />

- Xây dựng bối cảnh thế giới song song “Umbra” – không gian bóng tối với ánh sáng hiếm hoi, tạo cảm giác áp lực và nguy hiểm xuyên suốt quá trình chơi.
- Thiết kế tuyến truyện đơn giản nhưng đủ dẫn dắt: Max bị hút vào chiều không gian VR lỗi và bị truy đuổi bởi The Devourer, mục tiêu là sống sót đủ lâu để tìm cổng thoát.
- Định hình nhân vật và vai trò:
    - Max (nhân vật mặc định): nhân vật người chơi điều khiển.
    - The Devourer: kẻ truy đuổi liên tục, tạo áp lực thời gian và nhịp độ chơi.
- Danh sách nhân vật

| Nhân vật            | Mô tả        | Hình ảnh minh họa |
|---------------------|--------------|----------------|
| Max     | Max là một học sinh bình thường bị hút vào Umbra sau sự cố VR. Không có sức mạnh đặc biệt, cậu chỉ dựa vào bản năng sinh tồn và ý chí để tìm đường thoát khỏi bóng tối.     |<img width="124" height="336" alt="MaxDance" src="https://github.com/user-attachments/assets/42dc7f28-c718-40c1-890e-f397d568ce3c" /> |
| Akio     | Akio là thiếu niên ninja bí ẩn, di chuyển nhanh và gần như vô hình trong bóng tối Umbra.     | <img width="124" height="312" alt="Akio" src="https://github.com/user-attachments/assets/7e1fbac4-ff58-4b21-9646-8fadbd5bdc83" /> |
| RockStar     | RockStar là một rocker nổi loạn, mang tinh thần tự do và năng lượng bùng cháy giữa bóng tối.     | <img width="124" height="336" alt="Rock" src="https://github.com/user-attachments/assets/3ebb6ce9-859b-4ee7-94ef-cdffea27d8e1" />  |
| Runubos    | Runubos là tư tế cổ đại, sử dụng biểu tượng linh thiêng để kết nối với ánh sáng bị lãng quên.     | <img width="124" height="332" alt="Runubos" src="https://github.com/user-attachments/assets/15fa5247-7ac0-4c3b-9c08-408fdc741c52" /> |
| Stela       | Stela là cô bé ít nói với khả năng quan sát và phản xạ vượt trội, sinh tồn trong im lặng.     | <img width="124" height="336" alt="stela" src="https://github.com/user-attachments/assets/0d83c672-60cf-4bde-986e-136fcf661728" /> |
| Kiki| Kiki là nhân viên công sở lý trí, thích nghi với Umbra bằng chiến lược và kỷ luật. | <img width="124" height="336" alt="KIki" src="https://github.com/user-attachments/assets/ae3c1e1f-15be-4fb1-8422-861bb382d692" />   |
| Tadita | Tadita là chiến binh thổ dân, có khả năng hòa hợp với năng lượng nguyên thủy của Umbra. |  <img width="124" height="336" alt="Tadita 1" src="https://github.com/user-attachments/assets/f176a5c8-63f9-4a31-a784-5408148868dd" />|

### 3.2. Core Gameplay
- Triển khai gameplay Endless Runner góc nhìn third-person với các hành động:
    - Vuốt trái/phải: đổi lane / né
    - Vuốt lên: nhảy
    - Vuốt xuống: trượt / né thấp
    - Chạm chọn item: kích hoạt vật phẩm/kỹ năng
    - Hồi sinh: dùng xu
- Thiết kế hệ thống chướng ngại vật đảm bảo:
    - Độ khó tăng dần theo quãng đường/thời gian sống sót
    - Nhịp độ hợp lý: có khoảng “thở” và khoảng “dồn dập”
<img width="1303" height="792" alt="Screenshot 2025-12-23 170109" src="https://github.com/user-attachments/assets/e845ac29-76a2-439f-b4d8-6b0fbcf3d986" />
    
- Tích hợp cơ chế truy đuổi của The Devourer và sự xuất hiện của Ghost tạo áp lực: người chơi sai lầm liên tiếp hoặc cạn năng lượng sẽ bị bắt kịp.

### 3.3. Hệ thống năng lượng, thu thập và tính điểm
- Thiết kế hệ thống Energy:
    - Energy giảm theo thời gian/hành động 
    - Khi Energy về 0 → Không thể thực hiện các hành động -> dễ dàng bị hạ gục
- Triển khai cơ chế thu thập:
    - Light Fragment: tài nguyên chính giúp duy trì năng lượng + cộng điểm cơ bản
    - Light Crystal: hồi năng lượng tức thì (+5, +10…)
    - Xu: dùng để mua trang phục/vật phẩm
- Triển khai cơ chế tính điểm theo quãng đường: +1 điểm mỗi mét

### 3.4. Hệ thống vật phẩm
- Xây dựng hệ thống power-up với thời gian hiệu lực rõ ràng và chức năng khác biệt:
  
| Vật phẩm          | Mô tả                                                                 | Hình ảnh minh họa |
|------------------|-----------------------------------------------------------------------|------------------|
| Wings of Hope    | Cho phép người chơi bay lơ lửng trên các chướng ngại vật               | <img width="120" height="120" alt="ChatGPT Image Dec 21, 2025, 11_11_29 PM" src="https://github.com/user-attachments/assets/50a48a42-085c-4481-b0c0-00aa0062d941" /> |
| Shadow Bane      | Làm chậm tốc độ truy đuổi của quái vật xuống 50%                       | <img width="120" height="120" alt="ChatGPT Image Dec 21, 2025, 11_14_25 PM" src="https://github.com/user-attachments/assets/d773e438-4d03-4052-85d8-6d85d7c71561" /> |
| Time Shard       | Làm chậm toàn bộ thế giới (ngoại trừ Kane)                             | <img width="120" height="120" alt="ChatGPT Image Dec 21, 2025, 11_13_44 PM" src="https://github.com/user-attachments/assets/fd901a52-d977-4301-81bb-8b61889de0f0" /> |
| Score Multiplier | Nhân đôi số xu nhặt được trong thời gian hiệu lực                      | <img width="120" height="120" alt="ChatGPT Image Dec 21, 2025, 11_16_49 PM" src="https://github.com/user-attachments/assets/af24aa21-d7d9-41b4-bad9-24ab2026988c" /> |
| Magnet Field     | Hút Light Fragment + Light Crystal + Coin trong bán kính gần           |<img width="120" height="120" alt="ChatGPT Image Dec 21, 2025, 11_17_29 PM" src="https://github.com/user-attachments/assets/6d355205-6d51-434b-b68d-baa6888ccc59" />  |
| Ghost Phase      | Kane trở nên vô hình và có thể xuyên qua các chướng ngại vật           | <img width="120" height="120" alt="GhostPhase" src="https://github.com/user-attachments/assets/e2a44edb-25c5-4e46-97d9-b991e2f90160" /> |



- Đảm bảo các power-up có:
    - Điều kiện xuất hiện/tần suất hợp lý
    - Ưu tiên cân bằng để tránh “quá mạnh” hoặc “vô dụng”

### 3.5. Hệ thống nhiệm vụ và bảng xếp hạng

- Xây dựng hệ thống nhiệm vụ đa dạng nhằm định hướng lối chơi và khuyến khích người chơi khai thác đầy đủ các cơ chế gameplay, bao gồm:
  - Thu thập vật phẩm
  - Sử dụng vật phẩm & kỹ năng
  - Khoảng cách / sinh tồn
  - Hiệu suất chơi
  - Thử thách đặc biệt / online
<img width="1219" height="968" alt="Screenshot 2025-12-23 171139" src="https://github.com/user-attachments/assets/e56427dd-e279-4573-b269-f9d5a50a6f70" />

- Triển khai hệ thống lưu điểm và hiển thị bảng xếp hạng gồm:
    - **Daily Ranking**: xếp hạng người chơi theo điểm số cao nhất đạt được trong vòng 24 giờ gần nhất.
    - **Weekly Ranking**: xếp hạng người chơi theo thành tích cao nhất trong từng tuần.
    - **Feats Ranking**: xếp hạng dựa trên thành tích.
- Đảm bảo leaderboard có cơ chế cập nhật điểm sau mỗi ván và lưu “best score”.

<img width="1100" height="975" alt="Screenshot 2025-12-23 171339" src="https://github.com/user-attachments/assets/40f0742d-1891-4fef-b13a-2fb240063ecb" />

### 3.6. Hệ thống Cửa hàng và Nhân vật
- Thiết kế **Cửa hàng** sử dụng xu làm tiền tệ trong game:
  - Cho phép mua các vật phẩm hỗ trợ, mở khóa nhân vật.
  - Hiển thị giá, số lượng sở hữu và trạng thái có đủ xu hay không.
  - Lưu trữ và cập nhật dữ liệu xu/vật phẩm sau mỗi lần mua.
  - Mỗi nhân vật có giá mở khóa riêng và trạng thái: Locked / Unlocked.
  - Sau khi mở khóa, nhân vật được lưu vào dữ liệu người chơi để sử dụng cho các lần chơi sau.
<img width="471" height="455" alt="Screenshot 2025-12-23 194547" src="https://github.com/user-attachments/assets/f0456d5f-03b6-4c37-9120-3db84644789a" />
<img width="473" height="456" alt="Screenshot 2025-12-23 194727" src="https://github.com/user-attachments/assets/32e91793-de46-4b13-a58e-c2720cb37d89" />

- Kho **Nhân vật** cho phép người chơi:
  - Xem danh sách nhân vật, thông tin và trạng thái mở khóa.
  - Đổi nhân vật đang sử dụng trước khi vào gameplay.
  - Đồng bộ nhân vật đang chọn vào màn chơi.
![Screenshot 2025-12-23 212553](https://github.com/user-attachments/assets/f7228cf0-14c2-47b8-ba66-0b242a6d01ee)


### 3.7. Giao diện và trải nghiệm người dùng

- Thiết kế UI tối giản, dễ thao tác và phù hợp phong cách dark fantasy:

<img src="https://github.com/user-attachments/assets/9c6d5142-1cc7-4973-9720-307b926e0e3a" width="1100" height="1000" />
    
    Login/Register


<img width="1919" height="965" alt="Screenshot 2025-12-23 172020" src="https://github.com/user-attachments/assets/64c293cc-48f8-448f-b0d5-35a3ef780243" />
    
    Menu: Cửa hàng/Nhân vật/nhiệm vụ/Xếp hạng/Cài đặt

<img width="1919" height="994" alt="image" src="https://github.com/user-attachments/assets/9924901c-f633-4dce-a904-60b73606ab3f" />

    
    HUD hiển thị energy, điểm, vật phẩm đang kích hoạt
<img width="1919" height="994" alt="Screenshot 2025-12-23 172220" src="https://github.com/user-attachments/assets/ff6d47f3-e79b-4b76-89dd-b8ae4627d857" />
    
    Màn hình game over: tổng điểm, quãng đường, phần thưởng, tùy chọn hồi sinh


- Tối ưu trải nghiệm:
    - Thao tác vuốt mượt, phản hồi nhanh
    - Hiệu ứng ánh sáng rõ ràng để người chơi đọc được chướng ngại trong môi trường tối

### 3.8. Triển khai kỹ thuật

- Thực hành quy trình phát triển phần mềm theo nhóm trên nền tảng mã nguồn có sẵn của game Endless Runner, bao gồm quản lý mã nguồn, ứng dụng công cụ AI, phân công nhiệm vụ, trao đổi và phối hợp triển khai thông qua các công cụ hỗ trợ, từ đó rèn luyện kỹ năng làm việc nhóm trong môi trường phát triển thực tế.

- Mở rộng và nâng cấp bổ sung các hệ thống gameplay, nội dung và hệ thống mới.

- Thiết kế và triển khai kiến trúc client–server nhằm hỗ trợ lưu trữ, quản lý và đồng bộ dữ liệu người chơi, bao gồm thông tin đăng nhập, điểm số và tiến trình chơi.

- Phát triển và tích hợp thêm các yếu tố nội dung như bản đồ, chướng ngại vật và vật phẩm mới, đảm bảo tính ổn định của hệ thống và mở rộng chiều sâu gameplay cho trò chơi.

## 4. Ý tưởng cải thiện game

- Thiết kế cơ chế hoàn thành 3 nhiệm vụ để mở khóa mini game Light Scratch Card, trong đó:
  - Người chơi được lựa chọn 1 trong 2 thẻ cào ánh sáng.
  - Phần thưởng được phân phối ngẫu nhiên dựa trên hệ thống nhiệm vụ, bao gồm: xu, vật phẩm tăng sức mạnh, mạng hồi sinh, tinh thể ánh sáng hoặc trang phục.
- Đảm bảo hệ thống nhiệm vụ có thể làm mới theo chu kỳ, góp phần tăng tính thử thách, giảm sự lặp lại và nâng cao động lực chơi lại của người chơi.
- Triển khai chế độ chơi trực tuyến

## 5. Hướng dẫn khởi tạo dự án

### 5.1. Cài đặt Unity

- **Cài đặt Unity Hub**
  - Truy cập trang chủ Unity: https://unity.com/
  - Tải và cài đặt phần mềm Unity Hub
- **Cài đặt Unity Editor**
  - Mở Unity Hub → tab **Installs** → chọn **Install Editor**
  - Lựa chọn phiên bản Unity phù hợp (ví dụ: *Unity 6.2 (6000.2.7f2)*)
  - Cài đặt các module cần thiết:
    - Android Build Support  
    - Android SDK & NDK Tools  
    - OpenJDK  
    - (Tuỳ chọn) iOS Build Support  
### 5.2. Chạy dự án trên Unity Editor (vai trò nhà phát triển)

- **Mở dự án**
  - Mở Unity Hub → tab **Projects** → chọn **Add**
  - Chọn thư mục gốc của dự án (folder `cnpm`)
  - Nhấn **Open** để mở dự án trong Unity Editor
- **Chuyển nền tảng build (Android)**
  - Vào menu **File → Build Profiles**
  - Chọn nền tảng **Android**
  - Nhấn **Build And Run** để Unity cấu hình môi trường build
- **Tải các package cần thiết**
  - Người chơi tải về toàn bộ thư mục từ Google Drive  
  - Link Google Drive: [assetpackage](https://drive.google.com/drive/folders/1yPUfxNWXFrJbgJeJesqBCTaN4Xt_8dvE?usp=sharing)
  - Giải nén thư mục vào máy tính
- **Import các package cần thiết**
  - Vào menu **Assets → Import Package → Custom Package**
  - Chọn các file package đã giải nén và nhấn Open
  - Trong cửa sổ hiện ra, nhấn **Import** để thêm các package vào dự án
- **Kiểm tra Scene**
  - Trong cửa sổ **Project**, mở thư mục `Assets/Scenes`
  - Mở Scene **Authentication**
- **Chạy thử game**
  - Nhấn nút **Play** trên thanh công cụ của Unity Editor
  - Trò chơi sẽ chạy trực tiếp trong cửa sổ **Game**, phục vụ việc kiểm tra logic, giao diện và chức năng

### 5.3. Chạy game Unity sau khi Build (vai trò người chơi)

- **Tải bản build của trò chơi**
  - Người chơi tải về toàn bộ thư mục build từ Google Drive  
  - Link Google Drive: [release_build](https://drive.google.com/drive/folders/17pa_6PX-pDCsfD2limc-B2IMXtbDlmXr?usp=sharing)
- **Giải nén dữ liệu**
  - Giải nén thư mục build vừa tải về vào máy tính
- **Chạy trò chơi**
  - Mở thư mục đã giải nén
  - Chạy file thực thi **`ShadowEscape.exe`** để khởi động trò chơi
- **Trải nghiệm game**
  - Trò chơi sẽ được khởi động và chạy độc lập như một ứng dụng thông thường
  - Người chơi không cần cài đặt Unity Editor để sử dụng




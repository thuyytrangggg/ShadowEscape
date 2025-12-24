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
<img src="https://github.com/user-attachments/assets/e81e822e-e75f-46fe-ab48-1ee976aa64b1" width="40%"/>

<img src="https://github.com/user-attachments/assets/649e2c2a-4db9-4827-81ea-734cbb7b0b12" width="40%"/>

<img src="https://github.com/user-attachments/assets/6aa6d686-7440-4456-89e8-2b7b112bfe71" width="40%"/>

- Xây dựng bối cảnh thế giới song song “Umbra” – không gian bóng tối với ánh sáng hiếm hoi, tạo cảm giác áp lực và nguy hiểm xuyên suốt quá trình chơi.
- Thiết kế tuyến truyện đơn giản nhưng đủ dẫn dắt: Max bị hút vào chiều không gian VR lỗi và bị truy đuổi bởi The Devourer, mục tiêu là sống sót đủ lâu để tìm cổng thoát.
- Định hình nhân vật và vai trò:
    - Max (nhân vật mặc định): nhân vật người chơi điều khiển.
    - The Devourer: kẻ truy đuổi liên tục, tạo áp lực thời gian và nhịp độ chơi.
- Danh sách nhân vật

| Nhân vật            | Mô tả        | Hình ảnh minh họa |
|---------------------|--------------|----------------|
| Max     | Max là một học sinh bình thường bị hút vào Umbra sau sự cố VR. Không có sức mạnh đặc biệt, cậu chỉ dựa vào bản năng sinh tồn và ý chí để tìm đường thoát khỏi bóng tối.     |<img width="124" height="336" alt="529649283-42dc7f28-c718-40c1-890e-f397d568ce3c" src="https://github.com/user-attachments/assets/39fab756-5123-4ab2-805e-fa9f3f11e251" /> |
| Akio     | Akio là thiếu niên ninja bí ẩn, di chuyển nhanh và gần như vô hình trong bóng tối Umbra.     | <img width="124" height="312" alt="akio" src="https://github.com/user-attachments/assets/a9a24615-99a1-4778-bc23-cccdbe6aef2e" /> |
| RockStar     | RockStar là một rocker nổi loạn, mang tinh thần tự do và năng lượng bùng cháy giữa bóng tối.     | <img width="124" height="336" alt="RockStar" src="https://github.com/user-attachments/assets/a8803840-7aef-4f84-b855-fa56ad8dc9e6" /> |
| Runubos    | Runubos là tư tế cổ đại, sử dụng biểu tượng linh thiêng để kết nối với ánh sáng bị lãng quên.     | <img width="124" height="312" alt="Runubos" src="https://github.com/user-attachments/assets/1eb07795-6130-4f88-84f0-eb9ae48c2853" /> |
| Stela       | Stela là cô bé ít nói với khả năng quan sát và phản xạ vượt trội, sinh tồn trong im lặng.     | <img width="124" height="336" alt="Stela" src="https://github.com/user-attachments/assets/7f95ae3d-ff97-4353-9e9d-22b103ac6561" /> |
| Kiki| Kiki là nhân viên công sở lý trí, thích nghi với Umbra bằng chiến lược và kỷ luật. | <img width="124" height="336" alt="Kiki" src="https://github.com/user-attachments/assets/7050c8b8-b61f-4864-8203-b371a37b368c" />  |
| Tadita | Tadita là chiến binh thổ dân, có khả năng hòa hợp với năng lượng nguyên thủy của Umbra. | <img width="124" height="336" alt="Tadita" src="https://github.com/user-attachments/assets/867ae5be-e828-4478-ad80-358256b874ad" /> |

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

![529603087-e845ac29-76a2-439f-b4d8-6b0fbcf3d986](https://github.com/user-attachments/assets/2bf4efae-01fa-461a-9d65-2a5eaa2fe976)

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
| Wings of Hope    | Cho phép người chơi bay lơ lửng trên các chướng ngại vật               | <img width="120" height="120" alt="Wings" src="https://github.com/user-attachments/assets/cc688617-18be-4738-a118-4ca8818ef295" /> |
| Shadow Bane      | Làm chậm tốc độ truy đuổi của quái vật xuống 50%                       | <img width="120" height="120" alt="Shadow " src="https://github.com/user-attachments/assets/32e3b733-d4d7-4501-a452-63fe4556b048" /> |
| Time Shard       | Làm chậm toàn bộ thế giới (ngoại trừ Kane)                             | <img width="120" height="120" alt="Time" src="https://github.com/user-attachments/assets/f33c2d69-8577-41dd-80ac-1667773474fe" /> |
| Score Multiplier | Nhân đôi số xu nhặt được trong thời gian hiệu lực                      | <img width="120" height="120" alt="Score" src="https://github.com/user-attachments/assets/a6abc94a-bee9-46f4-941a-1f8e0c3865d9" /> |
| Magnet Field     | Hút Light Fragment + Light Crystal + Coin trong bán kính gần           | <img width="120" height="120" alt="Magnet" src="https://github.com/user-attachments/assets/c152b5b0-08eb-4d1e-8df9-76f41d3bb31e" /> |
| Ghost Phase      | Kane trở nên vô hình và có thể xuyên qua các chướng ngại vật           | <img width="120" height="120" alt="Ghost" src="https://github.com/user-attachments/assets/ce8989a8-653a-4967-be1c-13b5257375b4" /> |



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

![529604878-e56427dd-e279-4573-b269-f9d5a50a6f70](https://github.com/user-attachments/assets/879cd613-6ebb-421a-a396-3fef1f562d71)

- Triển khai hệ thống lưu điểm và hiển thị bảng xếp hạng gồm:
    - **Daily Ranking**: xếp hạng người chơi theo điểm số cao nhất đạt được trong vòng 24 giờ gần nhất.
    - **Weekly Ranking**: xếp hạng người chơi theo thành tích cao nhất trong từng tuần.
    - **Feats Ranking**: xếp hạng dựa trên thành tích.
- Đảm bảo leaderboard có cơ chế cập nhật điểm sau mỗi ván và lưu “best score”.

![529605499-40f0742d-1891-4fef-b13a-2fb240063ecb](https://github.com/user-attachments/assets/c974c3f7-cddb-4c5b-9abe-ff6c345b6d70)

### 3.6. Hệ thống Cửa hàng và Nhân vật
- Thiết kế **Cửa hàng** sử dụng xu làm tiền tệ trong game:
  - Cho phép mua các vật phẩm hỗ trợ, mở khóa nhân vật.
  - Hiển thị giá, số lượng sở hữu và trạng thái có đủ xu hay không.
  - Lưu trữ và cập nhật dữ liệu xu/vật phẩm sau mỗi lần mua.
  - Mỗi nhân vật có giá mở khóa riêng và trạng thái: Locked / Unlocked.
  - Sau khi mở khóa, nhân vật được lưu vào dữ liệu người chơi để sử dụng cho các lần chơi sau.

<img src="https://github.com/user-attachments/assets/ee2e3a1f-9d6b-4146-9bb8-32933bf577d6" width="45%"/>

<img src="https://github.com/user-attachments/assets/2c2a72bb-81ce-4bcb-9e7b-4c088210ad87" width="45%"/>


- Kho **Nhân vật** cho phép người chơi:
  - Xem danh sách nhân vật, thông tin và trạng thái mở khóa.
  - Đổi nhân vật đang sử dụng trước khi vào gameplay.
  - Đồng bộ nhân vật đang chọn vào màn chơi.
  
![529686802-f7228cf0-14c2-47b8-ba66-0b242a6d01ee](https://github.com/user-attachments/assets/34bb7c54-31cb-433f-ab14-81f42c8f583b)


### 3.7. Giao diện và trải nghiệm người dùng

- Thiết kế UI tối giản, dễ thao tác và phù hợp phong cách dark fantasy:

![529704218-9c6d5142-1cc7-4973-9720-307b926e0e3a](https://github.com/user-attachments/assets/ce541642-9f03-48fa-b3fc-86adbca095b3)
    
    Login/Register


![main](https://github.com/user-attachments/assets/a7149249-6142-4e69-b525-6006b30422a5)
    
    Menu: Cửa hàng/Nhân vật/nhiệm vụ/Xếp hạng/Cài đặt

![hud](https://github.com/user-attachments/assets/ec885a76-7aa4-45a0-b5a0-5d99bb4992b7)

    
    HUD hiển thị energy, điểm, vật phẩm đang kích hoạt
![over](https://github.com/user-attachments/assets/0d93f1eb-ada9-4d33-a58f-44c4bd70580d)
    
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




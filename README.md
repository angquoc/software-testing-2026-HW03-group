# HW03 GUI & Usability on EShop: Repo chung của nhóm

Repo này **chỉ dùng cho GitHub Issues** (bug report của cả nhóm) và bảng phân công.
Bài làm của mỗi người nằm ở **repo cá nhân riêng** (xem mục 2).

- SUT: [EShop](https://github.com/ttbhanh/eshop-sut) (commit `85af3ba`)
- Đặc tả (oracle): `README.md` của repo EShop. Phần giao diện nằm ở mục 8: FR-21 (IA-01 Chuẩn chung), FR-22 (IA-02 Form), FR-23 (IA-03 Điều hướng), FR-24 (IA-04 Phản hồi / trạng thái); một số ý giao diện khác nằm trong FR-03, FR-05, FR-06, FR-07

---

## 1. Phân công

Quy tắc (đề §5, nhóm dùng cách hiểu chặt nhất):

- Mỗi người chọn đúng **1 màn hình chính** cho GUI checklist (Task 1) và **1 luồng** cho usability evaluation (Task 2).
- Không ai được trùng **màn hình chính** hay trùng **luồng** với người khác. Cùng một màn hình hoặc một luồng trên Web và Mobile được tính là trùng (ví dụ Thanh toán Web và Thanh toán Mobile).
- **Màn hình phụ** (để đủ hơn 40 mục checklist) dùng chung được.
- Task 3 (ít nhất 3 nền tảng) chạy trên checklist của chính mình, không cần chia. Mỗi người tự ghi nền tảng vào bảng khi đã chốt.
- Mã màn hình (W-xx, A-xx, M-xx) và mã luồng (FL-xx) lấy theo sheet chọn màn hình của nhóm.

| Thành viên | MSSV | Màn hình chính (Task 1) | Màn hình phụ | Luồng usability (Task 2) | Nền tảng (Task 3) |
|---|---|---|---|---|---|
| Trần Thanh An | 23120017 | | | | |
| Hồ Thùy Hương | 23120046 | W-08 Thanh toán (có mã giảm giá) | W-01 Trang chủ, W-02 Chi tiết sản phẩm, W-07 Giỏ hàng | FL-01 Web: Mua hàng có coupon | |
| Nguyễn Thị Ánh Ngọc | 23120061 | W-06 Hồ sơ cá nhân & lịch sử đơn hàng | W-04 Đăng ký, W-03 Đăng nhập | FL-05 Admin: Tạo danh mục → Thêm sản phẩm | |

Muốn đổi lựa chọn thì báo cả nhóm trước, sửa sheet, sau đó sửa bảng này. Lịch sử commit giữ lại mọi thay đổi.

---

## 2. Repo cá nhân (mỗi người tự tạo)

HW03 là **bài cá nhân**. Đề ghi rõ: Chép bài của nhau, **kể cả chép prompt**, thì cả hai người đều bị 0 điểm.

1. Mỗi người tự tạo một repo **Private** trên GitHub cho bài làm của mình, ví dụ `software-testing-2026-HW03`.
2. **Không** add thành viên khác vào repo cá nhân, **không** gửi prompt, prompt log, checklist do AI sinh hay Agent Skill cho nhau.
3. Commit theo từng bước (đề §12 bắt buộc, kể cả **từng phiên usability**). Cuối cùng xuất `git log` ra file text để nộp.
4. Khi review chéo (policy môn học yêu cầu), chỉ gửi nhau **báo cáo** (report, checklist đã chạy, bug report), không gửi prompt.
5. **Người tham gia usability:** Không đưa thông tin cá nhân của người tham gia (họ tên, SĐT, Zalo, email, khuôn mặt) lên repo nhóm.

Những thứ dùng chung trong nhóm: **Bảng phân công mục 1**, **quy ước commit mục 3**, **quy ước Issues mục 4**, và **môi trường EShop mục 5**.

---

## 3. Quy ước commit

```
[<phạm vi>][<bước>] <Verb> <nội dung>
```

- Viết bằng **tiếng Anh**, bắt đầu bằng **động từ ở dạng mệnh lệnh** (Add, Review, Execute, Report, Fix, Update…), không có dấu chấm ở cuối.
- Mỗi commit chỉ chứa **một bước**, không gộp nhiều bước vào một commit.
- Nếu phải sửa lại một bước đã commit thì giữ nguyên tag của bước đó, ví dụ `[T1][review] Fix duplicated items in IA-02`.

### 3.1 Task 1: GUI Checklist (`T1`)

| Bước | Nội dung | Ví dụ |
|---|---|---|
| `survey` | Khảo sát màn hình, chụp ảnh, liệt kê thành phần UI | `[T1][survey] Survey profile, register and login screens` |
| `oracle` | Trích yêu cầu giao diện từ SRS, ánh xạ sang IA-01 đến IA-04 | `[T1][oracle] Extract UI requirements and map to IA` |
| `ai-draft` | Lưu checklist bản AI (nguyên văn) | `[T1][ai-draft] Add AI-generated checklist draft for IA-02` |
| `review` | Review từng mục AI (giữ / sửa / bỏ / gộp) | `[T1][review] Review AI checklist items` |
| `add` | Thêm mục AI bỏ sót, kèm lý do | `[T1][add] Add items missed by AI with reasons` |
| `excel` | Xuất file Excel checklist | `[T1][excel] Build Excel checklist` |
| `exec` | Chạy checklist, ghi Passed / Failed, Notes, ảnh mục Failed | `[T1][exec] Execute checklist on Chrome Windows` |
| `bugs` | Báo bug lên Issues, cập nhật bug report | `[T1][bugs] Report GUI bugs` |

### 3.2 Task 2: Usability Evaluation (`T2`)

| Bước | Nội dung | Ví dụ |
|---|---|---|
| `plan` | Test plan (mục tiêu, chân dung người dùng, phương pháp, số liệu) | `[T2][plan] Write usability test plan` |
| `scenario` | Kịch bản nhiệm vụ, tiêu chí hoàn thành, thời gian chuẩn | `[T2][scenario] Write task scenario` |
| `instruments` | Thang đo SUS / UEQ-S, câu hỏi mở, phiếu ghi chú | `[T2][instruments] Prepare SUS form and probe questions` |
| `participants` | Bảng người tham gia (liên lạc đã che số) | `[T2][participants] Add participant list` |
| `pilot` | Phiên pilot và các chỉnh sửa sau pilot | `[T2][pilot] Run pilot session and refine scenario` |
| `P1` đến `P7` | Hồ sơ từng phiên: Ghi chú quan sát, thang đo, câu trả lời mở | `[T2][P3] Record session P3 notes and SUS answers` |
| `score` | Tính điểm thang đo và số liệu hiệu suất | `[T2][score] Score SUS results across 7 sessions` |
| `analysis` | Gom pain point, tách bug và vấn đề thiết kế, xếp severity | `[T2][analysis] Synthesise findings and rank by severity` |
| `bugs` | Báo bug thật lên Issues | `[T2][bugs] Report usability bugs` |

### 3.3 Task 3: Cross-Browser / Cross-Platform (`T3`)

| Bước | Nội dung | Ví dụ |
|---|---|---|
| `setup` | Đăng ký trial, cấu hình tunnel, lớp chữ đè trên ảnh | `[T3][setup] Set up BrowserStack trial and local tunnel` |
| `<nền tảng>` | Chạy checklist trên một nền tảng (`chrome`, `firefox`, `safari`, `android-chrome`, `expo-go`) | `[T3][firefox] Execute checklist on Firefox Windows` |
| `bugs` | Báo bug chỉ xuất hiện trên một số nền tảng | `[T3][bugs] Report cross-platform bugs` |
| `compare` | Bảng so sánh kết quả giữa các nền tảng | `[T3][compare] Compare results across platforms` |

### 3.4 Commit không thuộc task nào

| Phạm vi | Dùng khi | Ví dụ |
|---|---|---|
| `[setup]` | Cấu trúc thư mục, công cụ, cấu hình | `[setup] Init folder structure` |
| `[skill]` | Agent Skill | `[skill] Add GUI checklist skill` |
| `[report]` | Báo cáo chung, README, AI Critique, Audit | `[report] Add AI critique` |
| `[forms]` | Các form AI-0x | `[forms] Fill AI-02 audit report` |
| `[docs]` | Tài liệu của repo chung | `[docs] Update allocation table` |
| `[template]` | Issue template của repo chung | `[template] Add IA field` |

---

## 4. Quy ước GitHub Issues

### 4.1 Ai báo bug nào

- Mỗi người báo bug tìm được **trong phạm vi của mình**: Màn hình chính và màn hình phụ của mình (Task 1, Task 3), luồng của mình (Task 2). Mỗi bug là một issue riêng.
- Trước khi tạo issue, **tìm xem đã có issue tương tự chưa**:
  - Bug ở **thành phần dùng chung** (navbar, header, footer) hoặc **màn hình phụ dùng chung** mà đã có issue: Không tạo issue mới. Comment vào issue đó (MSSV, mã mục checklist hoặc mã phiên, nền tảng) và ghi `Related #<số issue>` trong bug report cá nhân.
  - Bug nằm trên **màn hình chính của người khác**: Báo cho người đó, không tự tạo issue.
  - Bug trùng với bug đã báo ở HW02: Được tạo issue mới cho HW03 nếu nhìn từ góc giao diện, nhưng phải ghi `Related angquoc/software-testing-2026-HW02-group#<số issue>` ở phần ghi chú.
- **Task 2:** Chỉ đưa lên Issues những **bug thật** (hệ thống sai so với đặc tả hoặc chặn người dùng). Vấn đề thiết kế mang tính hệ thống (gây khó hiểu, chậm, thiếu tin cậy nhưng không sai đặc tả) chỉ ghi trong report cá nhân, không tạo issue.
- Bắt buộc dùng template **Bug report**. Phải có **ảnh chụp**: Kéo thả ảnh vào ô "Ảnh chụp".
- Tự gán (Assignees) issue cho chính mình.

### 4.2 Tiêu đề issue

```
[MSSV][T1|T2|T3][<Mã màn hình hoặc mã luồng>][<Nền tảng>] Mô tả ngắn: Hành vi sai so với đặc tả
```

Ví dụ (giả định, chỉ minh họa cách viết; `2312xxxx` thay cho MSSV thật):

- `[2312xxxx][T1][W-xx][Chrome] Ô nhập không có nhãn mô tả`
- `[2312xxxx][T3][W-xx][Safari iOS] Nút xác nhận bị bàn phím ảo che mất`
- `[2312xxxx][T2][FL-xx][Chrome] Người dùng không thấy thông báo lỗi sau khi bấm Lưu`

`<Nền tảng>` ghi trình duyệt hoặc thiết bị đã gặp lỗi: `Chrome`, `Firefox`, `Safari macOS`, `Safari iOS`, `Android Chrome`, `Expo Go`.

### 4.3 Label

| Nhóm | Label | Ý nghĩa |
|---|---|---|
| Loại | `bug` | Tự gắn bởi template |
| Mức độ | `severity: critical` | Mất dữ liệu, lộ thông tin, chặn luồng chính (không đăng nhập, đăng ký, mua hàng, quản lý shop được) |
| | `severity: high` | Sai đặc tả quan trọng, người dùng không có cách đi vòng |
| | `severity: medium` | Sai đặc tả hoặc gây khó dùng, có cách đi vòng |
| | `severity: low` | Lỗi hiển thị, câu chữ, màu sắc, căn chỉnh; ảnh hưởng nhỏ |
| Nền tảng | `platform: web` / `platform: admin` / `platform: mobile` | Frontend Web / Web Admin / App Mobile |
| Task | `task: T1 checklist` / `task: T2 usability` / `task: T3 cross-platform` | Bug tìm ra ở task nào |
| Khía cạnh giao diện | `ia: IA-01` / `ia: IA-02` / `ia: IA-03` / `ia: IA-04` | Chuẩn chung / Form / Điều hướng / Phản hồi và trạng thái |

**Cách gắn label cho mỗi issue:**

- Gắn đủ: 1 `severity` + 1 `platform` + 1 `task` + ít nhất 1 `ia`. Label `bug` được template gắn sẵn.
- `task`:
  - Bug thấy ngay ở lần chạy checklist đầu tiên: `task: T1 checklist`.
  - Bug **chỉ xuất hiện trên một số nền tảng**: `task: T3 cross-platform`.
  - Bug phát hiện qua phiên usability: `task: T2 usability`.
- `ia`: Bắt buộc với T1, T3. Với T2, gắn nếu xác định được khía cạnh giao diện; không xác định được thì bỏ qua.
- Chỉ dùng các label có sẵn. Cần thêm label thì báo nhóm, không tự tạo.

**Chọn severity:** Đi lần lượt từng câu hỏi, gặp câu trả lời "Có" đầu tiên thì dừng.

1. Lỗi làm lộ hoặc mất dữ liệu, vượt quyền, hay chặn hẳn luồng chính? → `severity: critical`
2. Sai đặc tả quan trọng mà người dùng không có cách nào tránh (ví dụ không đọc được nội dung, không bấm được nút)? → `severity: high`
3. Sai đặc tả hoặc gây khó dùng, nhưng vẫn có cách đi vòng để làm xong việc? → `severity: medium`
4. Chỉ sai hiển thị, câu chữ, màu sắc, căn chỉnh, không ảnh hưởng việc hoàn thành? → `severity: low`

Severity của usability finding trong report cá nhân có thể dùng thang riêng (ví dụ Nielsen 0 đến 4); label trên Issues vẫn dùng 4 mức ở trên.

Ví dụ một issue đầy đủ: `bug`, `severity: low`, `platform: web`, `task: T1 checklist`, `ia: IA-01`

**Màu label** (để cả nhóm nhìn quen mắt):

| Label | Màu |
|---|---|
| `severity: critical` | `#B60205` |
| `severity: high` | `#D93F0B` |
| `severity: medium` | `#FBCA04` |
| `severity: low` | `#C2E0C6` |
| `platform: *` | `#1D76DB` |
| `task: *` | `#0E8A16` |
| `ia: *` | `#5319E7` |

### 4.4 Ảnh chụp

- Mỗi issue có ít nhất 1 ảnh thấy rõ lỗi.
- Ảnh của Task 3 phải thấy **tên trình duyệt / OS / thiết bị**, **URL localhost** và **lớp chữ đè** gồm MSSV, họ tên, email sinh viên của người báo.
- Ảnh của Task 2 lấy từ màn hình, **không** để lộ khuôn mặt, tên, SĐT hay thông tin cá nhân của người tham gia. Ghi mã phiên (P1 đến P7) thay cho tên.

### 4.5 Trạng thái

- **Open:** Mới báo.
- Nếu phát hiện báo nhầm (hiểu sai đặc tả, lỗi do môi trường hay do công cụ cloud): **Close as not planned** và ghi lý do.
- Không xoá issue.

---

## 5. Môi trường EShop dùng chung

- URL chạy local: Backend `http://localhost:3000`, Web `http://localhost:5173`, Admin `http://localhost:5174`; Mobile chạy bằng Expo Go.
- Tài khoản mặc định: Admin `admin@eshop.com` / `Admin123!`; User `test@eshop.com` / `Test1234!`
  (`setup_guide.md` của EShop ghi mật khẩu admin `admin123` là **sai**, mật khẩu đúng trong DB là `Admin123!`).
- Reset dữ liệu trước mỗi đợt test và **trước mỗi phiên usability**: `cd backend && node database.js`.
- Dữ liệu mẫu **không có đơn hàng**. Cần đơn hàng (lịch sử đơn, quản lý đơn) thì tự đặt qua giỏ hàng / thanh toán rồi đổi trạng thái ở Admin.
- Mã `SAVE10`, `BIGBUY` mỗi người chỉ dùng được 1 lần: Luồng có dùng mã thì reset trước mỗi phiên.
- Mobile: Sửa `API_URL` trong `frontend-mobile/App.js` thành IP LAN của máy mình (điện thoại và máy tính dùng chung Wi-Fi), hoặc cắm USB và dùng `adb reverse`.
- Cloud (BrowserStack / LambdaTest): Cần bật tunnel (BrowserStack Local / LambdaTest Tunnel). Trên Safari (macOS, iOS) BrowserStack đổi `localhost` thành `bs-local.com`, trong khi frontend web gọi API bằng `http://localhost:3000` ghi cố định, nên các trang cần gọi API có thể không tải được dữ liệu. Nên thử sớm trước khi chạy cả checklist.

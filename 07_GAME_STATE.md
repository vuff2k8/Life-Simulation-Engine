NOVEL OS Beta

Canon Database Specification (CDS)

Version: Beta v0.9

---

0. MỤC ĐÍCH

Canon Database là nguồn sự thật duy nhất (Single Source of Truth) của toàn bộ dự án.

Nếu có mâu thuẫn giữa:

- Runtime
- Trí nhớ AI
- Chương truyện
- Người chơi nhớ nhầm

=> Canon Database luôn được ưu tiên.

Không được tự sửa Canon nếu chưa có sự kiện trong truyện.

---

1. DATABASE STRUCTURE

Canon chỉ gồm các Module sau:

CORE

CORE_MAIN
CORE_WORLD
CORE_SYSTEM

---

CHARACTER

MC
NPC

---

WORLD

LOCATION

ORGANIZATION

ECONOMY

TECHNOLOGY

HISTORY

---

STORY

ARC

PLOT

EVENT

FORESHADOW

---

MEMORY

TIMELINE

RELATIONSHIP

ASSET

KNOWLEDGE

---

2. DATA FORMAT

Mỗi Object sử dụng cấu trúc thống nhất.

Bắt buộc:

- ID
- Name

Các trường còn lại chỉ thêm khi cần.

Ví dụ:

ID (Required)

Name (Required)

Status

Current State

Relationship

Knowledge

Asset

Last Update

---

3. MAIN CHARACTER

Ví dụ

ID

MC001

Status

Alive

Name

Tô Thành

Age

16

Occupation

Học sinh lớp 10

Personality

...

Goal

...

Current Emotion

...

Knowledge

...

Assets

...

Relationship IDs

...

Canon Level

5

---

4. NPC

Một NPC chỉ tồn tại nếu có giá trị.

Không lưu NPC chỉ xuất hiện một lần.

NPC phải có:

ID

Name

Role

Goal

Relationship

Status

Last Seen

---

5. LOCATION

Ví dụ

LOC003

Tên

Tiệm Internet

Loại

Business

Owner

...

Importance

...

History

...

---

6. TIMELINE

Không viết theo chương.

Viết theo thời gian.

Ví dụ

2004-08-15

Nhập học lớp 10.

2004-09-02

Kiểm tra Toán.

...

---

7. KNOWLEDGE

Theo dõi:

Domain

Level

Source

Understanding

Practice

Last Used

Ví dụ

Điện tử

Hiểu:

15%

Thực hành:

0%

---

8. RELATIONSHIP

Không dùng điểm.

Dùng trạng thái.

Ví dụ

Nam

Trust:

Medium

Respect:

Low

Distance:

Close

Conflict:

None

History

...

---

9. ASSET

Không chỉ tiền.

Bao gồm:

Tiền

Sách

Dụng cụ

Thiết bị

Nguồn thu

Khoản đầu tư

...

---

10. FORESHADOW

ID

Được cài ở đâu

Mục đích

Đã thu hồi chưa

Nếu đã dùng xong

Archive.

---

11. CHANGELOG

Mọi thay đổi Canon đều phải ghi.

Ví dụ

v00021

Nam trở thành bạn thân.

Reason

Chapter 24

Date

...

---

12. UPDATE RULE

Sau mỗi chương.

Không cập nhật toàn Database.

Chỉ cập nhật Object bị thay đổi.

---

13. DELETE RULE

Không xóa.

Chỉ Archive.

Mọi dữ liệu đều có thể cần dùng lại.

---

15. GOLDEN RULE

Runtime quyết định cách vận hành.

Canon quyết định sự thật.

Hai hệ thống tuyệt đối không được lẫn vai trò.

---

# Update Flow

Sau mỗi chương:

1. Có gì thay đổi?

↓

2. Chỉ cập nhật đúng object đó.

↓

3. Không sửa phần khác.

---

# Writing Style

Ngắn gọn, ưu tiên dữ liệu.

---

# Consistency Check

Nếu một thông tin đã thay đổi,

hãy cập nhật,

không giữ cả bản cũ lẫn bản mới.

Canon luôn phản ánh trạng thái mới nhất.


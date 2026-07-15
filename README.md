# Life Simulation Engine v1.0 Turbo Max

> **Powered by NovelOS Runtime**
>
> Một hệ thống mô phỏng đời sống (Life Simulation) dành cho AI, được thiết kế để viết tiểu thuyết dài tập theo hướng **Slice of Life**, **Trưởng thành**, **Đô thị**, với mục tiêu tạo ra một thế giới có thể tự vận hành thay vì tạo Plot theo cách truyền thống.

---

# Triết lý cốt lõi

Life Simulation Engine (LSE) không cố gắng trả lời:

> "Chương tiếp theo nên viết gì?"

Thay vào đó, hệ thống luôn đặt câu hỏi:

> "Trong thế giới này, hôm nay điều gì hợp lý nhất sẽ xảy ra?"

Mọi sự kiện đều được sinh ra từ:

- Thời gian
- Thế giới
- Con người
- Quan hệ
- Cơ hội
- Xác suất

Không phải từ nhu cầu của Plot.

---

# Mục tiêu dự án

- Xây dựng một thế giới có thể tự vận hành.
- Viết tiểu thuyết dài 500–1000+ chương mà vẫn nhất quán.
- Giảm tối đa cảm giác "AI đang viết".
- Mô phỏng con người thay vì mô phỏng cốt truyện.
- Tối ưu workflow để làm việc lâu dài với AI.

---

# Kiến trúc

```text
Identity Engine
        │
        ▼
World Engine
        │
        ▼
Story Engine
        │
        ▼
Variation Engine
        │
        ▼
Writing Engine
        │
        ▼
Game State
        │
        ▼
Chapter
```

Các Engine chỉ chịu trách nhiệm **xử lý**.

Mọi dữ liệu đều được lưu trong các Database riêng.

---

# Cấu trúc dự án

```text
01_IDENTITY_ENGINE.md

02_WORLD_ENGINE_V1.2.md

03_STORY_ENGINE_V1.2.md

04_VARIATION_ENGINE.md

05_WRITING_ENGINE_V1.2.md

06_PROJECT_BIBLE.md

07_AUTHOR_NOTES.md

08_GAME_STATE.md

09_ARC_BIBLE.md

10_CHAPTER_RECAP.md

11_EVENT_POOL.md

12_CHARACTER_DNA.md

13_RELATIONSHIP_ENGINE.md

14_LIFE_PROGRESSION.md

15_WORLD_STATE.md

16_AI_PIPELINE.md

17_BUFF_SYSTEM.md

README.md

CHANGELOG.md
```

---

# Vai trò từng file

## Engine

### Identity Engine

Định nghĩa AI đang vận hành trong một **Life Simulation**, không phải chatbot.

---

### World Engine

Mô phỏng:

- thời gian
- lịch học
- NPC
- Scheduler
- Simulation Loop
- Decision Flow

Không viết truyện.

---

### Story Engine

Lựa chọn:

- chương hôm nay kể gì
- trọng tâm là ai
- nhịp truyện
- Landmark
- Time Compression

Không viết văn.

---

### Variation Engine

Chống lặp:

- mở đầu
- kết thúc
- cảm xúc
- nhịp
- xung đột
- góc nhìn

---

### Writing Engine

Chuyển Simulation thành tiểu thuyết.

Chỉ chịu trách nhiệm:

- văn phong
- hội thoại
- cảm xúc
- miêu tả

Không thay đổi Canon.

---

## Database

### Project Bible

Nền tảng của thế giới.

Bao gồm:

- bối cảnh
- nhân vật chính
- mục tiêu dự án
- hướng phát triển dài hạn

---

### Author Notes

Triết lý sáng tác.

Không phải Rule Engine.

---

### Game State

Single Source of Truth.

Lưu:

- Canon
- Timeline
- Character
- Asset
- Knowledge
- Relationship

---

### Arc Bible

Theo dõi từng Arc.

---

### Chapter Recap

Tóm tắt từng chương.

---

### Event Pool

Kho sự kiện của thế giới.

Không phải Plot.

---

### Character DNA

DNA của mọi nhân vật.

---

### Relationship Engine

Quản lý mọi mối quan hệ.

---

### Life Progression

Quy luật trưởng thành.

Không phải kịch bản.

---

### World State

Lưu trạng thái hiện tại của thế giới.

Không lưu lịch sử.

---

### Buff System

Quản lý toàn bộ Buff và cơ chế phát triển của Buff.

Không lẫn với Project Bible.

---

# AI Pipeline

```text
Planning
      │
      ▼
Simulation
      │
      ▼
Writing
      │
      ▼
Update
      │
      ▼
Verify
```

## Planning

Đọc:

- Game State
- World State
- Event Pool
- Character DNA
- Relationship

Xác định:

- hôm nay
- NPC
- Event
- mục tiêu chương

---

## Simulation

Thực hiện:

- Time Tick
- World Tick
- NPC Tick
- Decision Flow
- Scheduler

---

## Writing

Sinh chương truyện.

---

## Update

Chỉ cập nhật:

- Game State
- World State
- Relationship
- Buff
- Recap

---

## Verify

Kiểm tra:

- Canon
- Timeline
- Character
- World
- Relationship

Nếu có lỗi.

Ghi BUG.

Không tự sửa.

---

# Quy tắc thiết kế

## Single Source of Truth

Một dữ liệu.

Chỉ tồn tại ở một nơi.

Ví dụ:

Character → Character DNA

Relationship → Relationship Engine

Canon → Game State

Event → Event Pool

---

## Separation of Responsibility

Engine chỉ xử lý.

Database chỉ lưu.

Không trộn hai vai trò.

---

## World Before Plot

Ưu tiên:

Thế giới

↓

Nhân vật

↓

Quan hệ

↓

Plot

↓

Drama

---

## Human First

Độc giả phải nhớ:

Con người.

Rồi mới nhớ:

Plot.

---

# Workflow sử dụng AI

## Viết chương

Nạp:

- Identity
- World
- Story
- Variation
- Writing
- Game State
- World State
- Character
- Relationship
- Arc
- Recap
- Event

↓

Planning

↓

Simulation

↓

Writing

↓

Update

↓

Verify

---

## Cập nhật

Chỉ nạp:

- Game State
- World State
- Chapter Recap
- Relationship
- Buff

---

## Refactor

Nạp toàn bộ Project.

Chỉ thực hiện khi nâng phiên bản.

---

# Workflow Model (Khuyến nghị)

## Model mạnh

Dùng cho:

- Writing

---

## Model nhanh

Dùng cho:

- Planning
- Update
- Verify

LSE không phụ thuộc vào bất kỳ AI nào.

Có thể thay:

- Gemini
- GPT
- Claude
- hoặc model khác

mà không cần sửa kiến trúc.

---

# Roadmap

## v1.x

- Hoàn thiện Engine
- Hoàn thiện Database
- Viết truyện
- Ghi BUG

---

## v2.x

NovelOS Runtime

- Python Runtime
- Context Compiler
- Auto Update
- Verify
- Token Optimization

---

## v3.x

Dashboard

- Character Manager
- World Editor
- Relationship Viewer
- Timeline
- Statistics

---

# Nguyên tắc mở rộng

Không thêm Engine mới nếu chưa có BUG thực tế.

Không thêm Rule nếu Rule cũ vẫn giải quyết được.

Mọi thay đổi phải làm ít nhất một trong các điều sau:

- giảm token
- tăng tính nhất quán
- tăng tính tự nhiên
- tăng hiệu suất
- giảm thao tác thủ công

Nếu không đạt.

Không thêm.

---

# Hiện trạng

**Project:** Life Simulation Engine v1.0 Turbo Max

**Status:** Beta

**Framework:** NovelOS Runtime

**Architecture:** Stable

**Current Focus:**

- Test thực chiến
- Tối ưu Runtime
- Xây Python Runtime
- Giảm Token
- Tìm BUG thực tế

---

# Golden Rule

Đừng cố tạo ra một cốt truyện hay.

Hãy tạo ra một thế giới đủ thật.

Khi thế giới thật sự sống,

câu chuyện sẽ tự xuất hiện.
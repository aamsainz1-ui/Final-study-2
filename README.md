# Financial Management System (ระบบจัดการการเงิน)

ระบบจัดการการเงินฉบับสมบูรณ์สำหรับธุรกิจ พัฒนาด้วย Next.js 15, TypeScript และ Tailwind CSS

## 🌟 คุณสมบัติหลัก

### 💼 การจัดการข้อมูล
- **ทีมและสมาชิก** จัดการโครงสร้างองค์กร
- **หมวดหมู่** จัดการประเภทรายรับ-รายจ่าย
- **ลูกค้า** จัดการข้อมูลลูกค้าและนับจำนวน
- **รายการธุรกรรม** บันทึกรายรับ-รายจ่าย

### 💰 การเงิน
- **เงินเดือน** จัดการการจ่ายเงินเดือนพนักงาน
- **โบนัส** จัดการโบนัสและค่าตอบแทนพิเศษ
- **ค่าคอมมิชชัน** คำนวณและจัดการค่าคอมมิชชัน
- **รายงาน** ดูรายงานสรุปการเงิน

### 👥 ผู้ใช้งาน
- **ระบบสมาชิก** ลงทะเบียนและเข้าสู่ระบบ
- **สิทธิ์การใช้งาน** แบ่งระดับผู้ใช้ (Admin, Owner, User)
- **ความปลอดภัย** ป้องกันการเข้าถึงข้อมูล

### 📁 จัดการไฟล์
- **File Manager** จัดการเอกสารและไฟล์ในระบบ
- **อัปโหลด/ดาวน์โหลด** จัดการไฟล์ต่างๆ

## 🛠️ เทคโนโลยีที่ใช้

### Frontend
- **Next.js 15** - React Framework พร้อม App Router
- **TypeScript** - Type-safe JavaScript
- **Tailwind CSS 4** - Utility-first CSS Framework
- **shadcn/ui** - Component Library
- **Framer Motion** - Animations
- **Zustand** - State Management
- **TanStack Query** - Server State Management

### Backend
- **Next.js API Routes** - RESTful API
- **Prisma** - Database ORM
- **SQLite** - Database
- **NextAuth.js** - Authentication
- **Socket.io** - Real-time Communication

### Development Tools
- **ESLint** - Code Linting
- **TypeScript** - Static Type Checking
- **npm** - Package Management

## 🚀 การติดตั้งและรันโปรเจค

### 1. Clone Repository
```bash
git clone https://github.com/YOUR_USERNAME/financial-management-system.git
cd financial-management-system
```

### 2. ติดตั้ง Dependencies
```bash
npm install
```

### 3. ตั้งค่า Database
```bash
npm run db:push
```

### 4. รัน Development Server
```bash
npm run dev
```

เปิดเบราว์เซอร์ที่ [http://localhost:3000](http://localhost:3000)

## 📋 คำสั่งที่ใช้ได้

```bash
# Development
npm run dev          # รัน development server
npm run build        # Build สำหรับ production
npm run start        # รัน production server
npm run lint         # ตรวจสอบคุณภาพโค้ด

# Database
npm run db:push      # อัปเดต database schema
npm run db:studio    # เปิด Prisma Studio
```

## 🏗️ โครงสร้างโปรเจค

```
src/
├── app/                 # Next.js App Router
│   ├── api/            # API Routes
│   ├── admin/          # Admin Pages
│   ├── login/          # Login Page
│   └── page.tsx        # Main Page
├── components/         # React Components
│   ├── ui/            # shadcn/ui Components
│   ├── dashboard.tsx  # Dashboard
│   ├── forms/         # Form Components
│   └── ...
├── lib/               # Utilities
│   ├── db.ts         # Database Client
│   ├── auth.ts       # Authentication
│   └── utils.ts      # Helper Functions
├── contexts/          # React Contexts
├── hooks/            # Custom Hooks
└── types/            # TypeScript Types
```

## 👤 ระดับผู้ใช้งาน

- **Owner** - เจ้าของระบบ สิทธิ์สูงสุด
- **Admin** - ผู้ดูแลระบบ
- **User** - ผู้ใช้งานทั่วไป

## 🔐 คุณสมบัติความปลอดภัย

- **Authentication** ระบบยืนยันตัวตน
- **Authorization** ควบคุมสิทธิ์การเข้าถึง
- **Protected Routes** ป้องกันการเข้าถึงโดยไม่ได้รับอนุญาต
- **Input Validation** ตรวจสอบข้อมูลที่ป้อนเข้ามา

## 📊 ฟังก์ชันหลัก

### 📈 Dashboard
- แสดงสรุปข้อมูลการเงิน
- กราฟและสถิติต่างๆ
- ภาพรวมธุรกิจ

### 💳 การจัดการรายรับ-รายจ่าย
- บันทึกรายการรับ-จ่าย
- จัดการหมวดหมู่
- ดูประวัติการทำรายการ

### 👥 การจัดการทีม
- สร้างและจัดการทีม
- เพิ่มสมาชิก
- กำหนดตำแหน่งและเงินเดือน

### 💰 การเงิน
- จัดการเงินเดือน
- คำนวณโบนัส
- จัดการค่าคอมมิชชัน

## 🌐 ภาษาที่รองรับ

- **ไทย** - ภาษาหลักของระบบ
- **อังกฤษ** - สำหรับคำศัพท์เทคนิค

## 📝 License

MIT License - สามารถนำไปใช้งานได้ฟรี

## 🤝 การมีส่วนร่วม

ยินดีรับการมีส่วนร่วมในการพัฒนาโปรเจค!

1. Fork โปรเจค
2. สร้าง Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit การเปลี่ยนแปลง (`git commit -m 'Add some AmazingFeature'`)
4. Push ไปยัง Branch (`git push origin feature/AmazingFeature`)
5. เปิด Pull Request

---

🚀 **พัฒนาด้วย ❤️ โดยใช้เทคโนโลยีล่าสุด**
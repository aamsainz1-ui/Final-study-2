# 📦 การอัปโหลดโปรเจค avenuep.org ขึ้น Server

## 📁 ไฟล์ที่ต้องการ
- **ไฟล์โปรเจค:** `avenuep-project.tar.gz` (225KB)
- **Script ติดตั้ง:** `deploy-to-server.sh`

## 🚀 ขั้นตอนการอัปโหลด

### 1. SSH เข้า Server
```bash
ssh root@118.139.179.219
```

### 2. อัปโหลดไฟล์ (จากเครื่อง local)
```bash
scp avenuep-project.tar.gz root@118.139.179.219:/root/
scp deploy-to-server.sh root@118.139.179.219:/root/
```

### 3. บน Server - แตกไฟล์และติดตั้ง
```bash
# แตกไฟล์
tar -xzf avenuep-project.tar.gz
cd my-project

# ทำให้ script รันได้
chmod +x ../deploy-to-server.sh

# รันการติดตั้ง
../deploy-to-server.sh
```

### 4. ตรวจสอบการทำงาน
```bash
# ตรวจสอบ service
pm2 status
pm2 logs avenuep

# ตรวจสอบ nginx
systemctl status nginx
```

## 🔧 สิ่งที่ Script ทำให้อัตโนมัติ
- ✅ ติดตั้ง Node.js, npm, PM2
- ✅ ติดตั้ง dependencies ของโปรเจค
- ✅ Build โปรเจค
- ✅ ตั้งค่า Nginx
- ✅ ติดตั้ง SSL Certificate
- ✅ เริ่มการทำงานด้วย PM2

## 🌐 เมื่อเสร็จแล้ว
- เว็บจะพร้อมใช้งานที่: `https://avenuep.org`
- SSL จะถูกติดตั้งอัตโนมัติ
- ระบบจะ restart อัตโนมัติถ้ามีปัญหา

## 🆘 ถ้ามีปัญหา
ตรวจสอบ logs:
```bash
pm2 logs avenuep
tail -f /var/log/nginx/error.log
```

---
**📝 หมายเหตุ:** ตรวจสอบให้แน่ใจว่า port 3000 ว่างอยู่บน server
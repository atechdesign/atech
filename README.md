# 👨🏻‍💻 Super Atech — AI Software Development Team

ชุด **Skill** สำหรับสร้างทีมพัฒนาซอฟต์แวร์ด้วย AI (Claude) ที่ทำงานร่วมกันแบบหลาย agent
ออกแบบมาเพื่อใช้กับ **Multica** เชื่อมต่อ **Claude AI** โดยแต่ละ role = 1 ไฟล์ skill

> **หลักการ:** instruction เขียนเป็นภาษาอังกฤษ (เพื่อความแม่นยำกับงานเทคนิค)
> แต่ทุก agent **สื่อสารกับผู้ใช้และทีมเป็นภาษาไทย** เป็นค่าเริ่มต้น

---

## 🧩 รายชื่อทีม (Roster)

| # | ไฟล์ | Role | หน้าที่หลักโดยย่อ |
|---|------|------|------------------|
| 00 | [00-tech-lead-orchestrator.md](00-tech-lead-orchestrator.md) | **Tech Lead / Orchestrator** | หัวหน้าทีม รับโจทย์ แตกงาน มอบหมาย รวมงาน ตัดสินใจขั้นสุดท้าย |
| 01 | [01-product-manager.md](01-product-manager.md) | **Product Manager** | กำหนด vision, roadmap, จัดลำดับความสำคัญ, เขียน user story |
| 02 | [02-business-analyst.md](02-business-analyst.md) | **Business Analyst** | วิเคราะห์ requirement, เขียน spec, จำลอง process |
| 03 | [03-software-architect.md](03-software-architect.md) | **Software Architect** | ออกแบบสถาปัตยกรรมระบบ, เลือกเทคโนโลยี, ตั้งมาตรฐาน |
| 04 | [04-ux-ui-designer.md](04-ux-ui-designer.md) | **UX/UI Designer** | ออกแบบประสบการณ์ผู้ใช้, wireframe, design system |
| 05 | [05-frontend-developer.md](05-frontend-developer.md) | **Frontend Developer** | พัฒนา UI ฝั่งหน้าบ้าน, เชื่อม API |
| 06 | [06-backend-developer.md](06-backend-developer.md) | **Backend Developer** | พัฒนา API, business logic, ฐานข้อมูล |
| 07 | [07-mobile-developer.md](07-mobile-developer.md) | **Mobile Developer** | พัฒนาแอป iOS/Android/cross-platform |
| 08 | [08-devops-engineer.md](08-devops-engineer.md) | **DevOps Engineer** | CI/CD, infrastructure, deployment, monitoring |
| 09 | [09-qa-engineer.md](09-qa-engineer.md) | **QA Engineer** | ทดสอบ, test automation, ควบคุมคุณภาพ |
| 10 | [10-security-engineer.md](10-security-engineer.md) | **Security Engineer** | ตรวจความปลอดภัย, threat modeling, code review ด้านความปลอดภัย |
| 11 | [11-data-engineer.md](11-data-engineer.md) | **Data Engineer** | data pipeline, ฐานข้อมูล, analytics |

---

## 🔄 Flow การทำงานของทีม (ภาพรวม)

```
ผู้ใช้ / ลูกค้า
      │  (โจทย์/ความต้องการ)
      ▼
┌─────────────────────────────┐
│ 00 Tech Lead / Orchestrator │ ◄── ศูนย์กลาง: แตกงาน + มอบหมาย + รวมงาน
└─────────────────────────────┘
      │
      ├─► 01 PM ──► 02 BA ──► 04 UX/UI        (Discovery & Design)
      │
      ├─► 03 Architect                         (System Design)
      │
      ├─► 05 Frontend ┐
      ├─► 06 Backend  ├─► (Build)
      ├─► 07 Mobile   ┘
      ├─► 11 Data Engineer
      │
      ├─► 09 QA ──► 10 Security                 (Verify)
      │
      └─► 08 DevOps                             (Ship & Operate)
```

> ทุก role รายงานกลับและประสานผ่าน **Tech Lead / Orchestrator** เพื่อให้งานสอดคล้องกัน

---

## ⚙️ วิธีนำไปใช้กับ Multica + Claude

แต่ละไฟล์ออกแบบให้เป็น **persona / skill แบบ standalone** ใช้ได้ 2 แนวทาง:

1. **เป็น System Prompt ต่อ 1 agent** — สร้าง agent 1 ตัวต่อ 1 role ใน Multica แล้ววางเนื้อหาไฟล์เป็น system prompt / instruction ของ agent นั้น
2. **เป็น Claude Skill** — ทุกไฟล์มี YAML frontmatter (`name`, `description`) ครบ สามารถนำไปวางใน `.claude/skills/<name>/SKILL.md` ได้โดยตรงหากต้องการใช้กับ Claude Code

**แนะนำการเริ่มต้น:**
1. ตั้ง **00 Tech Lead / Orchestrator** เป็น agent หลักที่รับโจทย์จากผู้ใช้
2. ให้ Orchestrator มอบหมายงานไปยัง role อื่น ๆ ตาม `description` ของแต่ละ skill
3. แต่ละ role ทำงานในขอบเขตของตน แล้วส่งผลลัพธ์ (deliverables) กลับมาที่ Orchestrator

---

## 📐 โครงสร้างมาตรฐานของทุกไฟล์ skill

ทุกไฟล์ใช้โครงเดียวกันเพื่อความสม่ำเสมอ:

- **Frontmatter** — `name`, `description` (ใช้เป็น trigger ให้ Orchestrator เลือก role)
- **Role & Mission** — ตัวตนและเป้าหมาย
- **Communication Protocol** — กติกาการสื่อสาร (ภาษาไทย)
- **Core Responsibilities** — หน้าที่หลัก
- **Expertise** — ทักษะ/ความเชี่ยวชาญ
- **How You Operate** — ขั้นตอนการทำงาน
- **Collaboration & Handoffs** — รับงานจากใคร / ส่งต่อให้ใคร
- **Deliverables** — สิ่งที่ส่งมอบ
- **Definition of Done** — เกณฑ์งานเสร็จ
- **Tools & Tech Stack** — เครื่องมือ
- **Guardrails** — ข้อห้าม/ขอบเขต
- **Example Tasks** — ตัวอย่างงาน

---

_Generated for **AIDC Tech / Super Atech** — ปรับแก้ tech stack และรายละเอียดให้ตรงกับโปรเจกต์จริงได้ตามต้องการ_

# 👨🏻‍💻 Super Atech — AI Software Development Team

ชุด **Skill** สำหรับสร้างทีมพัฒนาซอฟต์แวร์ด้วย AI (Claude) ที่ทำงานร่วมกันแบบหลาย agent
ออกแบบมาเพื่อใช้กับ **Multica** เชื่อมต่อ **Claude AI** โดยแต่ละ role = 1 ไฟล์ skill

> **หลักการ:** instruction เขียนเป็นภาษาอังกฤษ (เพื่อความแม่นยำกับงานเทคนิค)
> แต่ทุก agent **สื่อสารกับผู้ใช้และทีมเป็นภาษาไทย** เป็นค่าเริ่มต้น

---

## 🧩 รายชื่อทีม (Roster)

| # | Skill | Role | หน้าที่หลักโดยย่อ |
|---|------|------|------------------|
| 00 | [tech-lead-orchestrator](tech-lead-orchestrator/SKILL.md) | **Tech Lead / Orchestrator** | หัวหน้าทีม รับโจทย์ แตกงาน มอบหมาย รวมงาน ตัดสินใจขั้นสุดท้าย |
| 01 | [product-manager](product-manager/SKILL.md) | **Product Manager** | กำหนด vision, roadmap, จัดลำดับความสำคัญ, เขียน user story |
| 02 | [business-analyst](business-analyst/SKILL.md) | **Business Analyst** | วิเคราะห์ requirement, เขียน spec, จำลอง process |
| 03 | [software-architect](software-architect/SKILL.md) | **Software Architect** | ออกแบบสถาปัตยกรรมระบบ, เลือกเทคโนโลยี, ตั้งมาตรฐาน |
| 04 | [ux-ui-designer](ux-ui-designer/SKILL.md) | **UX/UI Designer** | ออกแบบประสบการณ์ผู้ใช้, wireframe, design system |
| 05 | [frontend-developer](frontend-developer/SKILL.md) | **Frontend Developer** | พัฒนา UI ฝั่งหน้าบ้าน, เชื่อม API |
| 06 | [backend-developer](backend-developer/SKILL.md) | **Backend Developer** | พัฒนา API, business logic, ฐานข้อมูล |
| 07 | [mobile-developer](mobile-developer/SKILL.md) | **Mobile Developer** | พัฒนาแอป iOS/Android/cross-platform |
| 08 | [devops-engineer](devops-engineer/SKILL.md) | **DevOps Engineer** | CI/CD, infrastructure, deployment, monitoring |
| 09 | [qa-engineer](qa-engineer/SKILL.md) | **QA Engineer** | ทดสอบ, test automation, ควบคุมคุณภาพ |
| 10 | [security-engineer](security-engineer/SKILL.md) | **Security Engineer** | ตรวจความปลอดภัย, threat modeling, code review ด้านความปลอดภัย |
| 11 | [data-engineer](data-engineer/SKILL.md) | **Data Engineer** | data pipeline, ฐานข้อมูล, analytics |
| 12 | [business-development](business-development/SKILL.md) | **Business Development & Sales** | ทำ proposal, pitch deck, ราคา, ตอบ RFP เพื่อขายงาน |

### 🎨 Marketing Team

| # | Skill | Role | หน้าที่หลักโดยย่อ |
|---|------|------|------------------|
| 13 | [marketing-director](marketing-director/SKILL.md) | **Marketing Director** (lead) | วางกลยุทธ์แคมเปญ แตกงาน มอบหมาย รวมงาน คุมแบรนด์ |
| 14 | [content-strategist](content-strategist/SKILL.md) | **Content Strategist** | content plan, copywriting ไทย/ลาว/อังกฤษ, SEO writing |
| 15 | [graphic-designer](graphic-designer/SKILL.md) | **Graphic Designer** | brand identity, social graphics, SVG/spec/prompt |
| 16 | [video-producer](video-producer/SKILL.md) | **Video Producer** | สคริปต์, storyboard, shot list, ซับไตเติล, edit plan |
| 17 | [three-d-artist](three-d-artist/SKILL.md) | **3D Artist** | Blender scripts, Three.js, product viz, materials/lighting |
| 18 | [social-media-manager](social-media-manager/SKILL.md) | **Social Media Manager** | content calendar, community playbook, engagement |
| 19 | [digital-marketing-specialist](digital-marketing-specialist/SKILL.md) | **Digital Marketing Specialist** | paid ads, SEO, tracking/UTM, ROI report |

### 💰 Finance Team

| # | Skill | Role | หน้าที่หลักโดยย่อ |
|---|------|------|------------------|
| 20 | [finance-manager](finance-manager/SKILL.md) | **Finance Manager** (lead) | งบประมาณ, budget vs actual, ค่าใช้จ่าย AI/token |
| 21 | [accountant](accountant/SKILL.md) | **Accountant** | บันทึกบัญชี, ใบเสนอราคา/invoice, ปิดงบรายเดือน |

### ⚖️ Legal Team

| # | Skill | Role | หน้าที่หลักโดยย่อ |
|---|------|------|------------------|
| 22 | [legal-counsel](legal-counsel/SKILL.md) | **Legal Counsel** (lead) | ร่าง/รีวิวสัญญา, เอกสาร tender, สรุปความเสี่ยง |
| 23 | [compliance-officer](compliance-officer/SKILL.md) | **Compliance Officer** | privacy policy, PDPA, checklist, ทะเบียน license |

### 👥 HR Team

| # | Skill | Role | หน้าที่หลักโดยย่อ |
|---|------|------|------------------|
| 24 | [hr-manager](hr-manager/SKILL.md) | **HR Manager** (lead) | roster agent, onboarding role ใหม่, performance review |
| 25 | [agent-performance-analyst](agent-performance-analyst/SKILL.md) | **Agent Performance Analyst** | วิเคราะห์ task/cost/efficiency ของ agent ทุกตัว |

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

## 📦 โครงสร้าง repo (1 skill = 1 โฟลเดอร์)

แต่ละ role เป็น skill มาตรฐาน — อยู่ในโฟลเดอร์ของตัวเองและมีไฟล์ `SKILL.md`:

```
atech/
├── tech-lead-orchestrator/SKILL.md
├── product-manager/SKILL.md
├── ...
└── data-engineer/SKILL.md
```

## ⚙️ วิธีนำไปใช้กับ Multica + Claude

### นำเข้าผ่าน "Import from URL" ของ Multica
นี่เป็น **multi-skill repository** ต้องชี้ไปที่ **โฟลเดอร์ของแต่ละ skill** (import ทีละตัว):

```
https://github.com/atechdesign/atech/tree/main/tech-lead-orchestrator
https://github.com/atechdesign/atech/tree/main/product-manager
https://github.com/atechdesign/atech/tree/main/business-analyst
... (ทำซ้ำสำหรับทุก role)
```

> ⚠️ อย่าใส่ URL ของ repo เปล่า ๆ (`.../atech.git`) เพราะ Multica จะหา `SKILL.md` ที่ root ไม่เจอ

### แนวทางอื่นที่ใช้ได้
- **เป็น System Prompt ต่อ 1 agent** — สร้าง agent 1 ตัวต่อ 1 role แล้ววางเนื้อหา `SKILL.md` เป็น system prompt
- **ใช้กับ Claude Code** — copy โฟลเดอร์ไปวางใน `.claude/skills/` ได้โดยตรง

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

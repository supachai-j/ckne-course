# CKNE Lab Manual

คอร์สเตรียมสอบ **CKNE (Certified Kubernetes Network Engineer)** แบบลงมือทำจริง
เรียงตาม official exam blueprint ทั้ง 5 domain

📖 **อ่านออนไลน์:** https://supachai-j.github.io/ckne-course/

## เนื้อหา

| Module | หัวข้อ | น้ำหนักข้อสอบ |
|---|---|---|
| 0 | Lab Environment Setup (kind + Cilium) | – |
| 1 | Core Infrastructure & CNI | 15% |
| 2 | Service Networking & DNS | 25% |
| 3 | Advanced Traffic Management | 20% |
| 4 | Network Security & Policy | 25% |
| 5 | Observability | 15% |

- **20 หัวข้อ** พร้อม concept + diagram
- **73 hands-on lab steps** รันบน cluster จริง (คำสั่งคัดลอกได้ + ผลลัพธ์ที่ควรเห็น + วิธีแก้เมื่อพัง)
- **65 ข้อสอบ** (quiz ท้ายบท 44 ข้อ + mock exam 21 ข้อ)
- บันทึกความคืบหน้าใน browser (localStorage)

## Lab environment

ทุกแล็บใช้ `kind` + **Cilium** เป็น CNI หลัก เพราะครอบคลุม blueprint ได้เกือบทั้งหมดในตัวเดียว:
CNI/IPAM, kube-proxy replacement (eBPF), NetworkPolicy แบบ L7/DNS-aware, Gateway API,
egress gateway, ClusterMesh, WireGuard encryption และ Hubble observability

เริ่มที่ Module 0 เพื่อสร้างคลัสเตอร์ก่อน แล้วแล็บโมดูลถัดไปจะต่อยอดจากคลัสเตอร์เดิม

## Local

เป็น static HTML ไฟล์เดียว ไม่มี build step:

```bash
python3 -m http.server 8000   # แล้วเปิด http://localhost:8000
```

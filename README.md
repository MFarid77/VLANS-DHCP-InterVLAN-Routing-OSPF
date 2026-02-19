# Cisco Network Project: VLANs + DHCP + Inter-VLAN Routing + OSPF

## Layihənin Təsviri
Bu layihə Cisco Packet Tracer-də hazırlanmış tam işlək şəbəkə laboratoriyasıdır. Layihənin məqsədi:

- VLAN-lar vasitəsilə şəbəkə seqmentlərinin ayrılması
- DHCP ilə hostlara avtomatik IP təyin edilməsi
- Inter-VLAN Routing ilə VLAN-lar arası rabitənin təmin edilməsi
- OSPF protokolu ilə dinamik yönləndirmə

Layihə real şəbəkə mühitinə yaxın ssenarilər əsasında hazırlanmışdır və şəbəkə administratorları, tələbələr və laboratoriya istifadəçiləri üçün ideal təcrübədir.

---

## Şəbəkə Topologiyası

- **Router:** 1 ədəd (Router-on-a-Stick konfiqurasiyası)
- **Switch:** 2-3 ədəd
- **PC:** 6-10 ədəd
- **VLAN-lar:**  
  - VLAN 10 – HR  
  - VLAN 20 – Sales  
  - VLAN 30 – IT
- **OSPF Area:** 0

> **Screenshot əlavə etmə:**  
> Layihəni başa düşmək və vizual təsvir üçün Packet Tracer topologiyasının **screenshotunu** `Diagrams/NetworkTopology.png` qovluğuna əlavə edin. README-də bunu göstərmək üçün:
> ```markdown
> ![Network Topology](Diagrams/NetworkTopology.png)
> ```

---

## Addım-addım Təlimat

### 1. VLAN-ların yaradılması
```bash
Switch> enable
Switch# configure terminal
Switch(config)# vlan 10
Switch(config-vlan)# name HR
Switch(config)# vlan 20
Switch(config-vlan)# name Sales
Switch(config)# vlan 30
Switch(config-vlan)# name IT
Switch(config)# exit

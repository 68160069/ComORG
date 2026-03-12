
## 4.5 คำสำคัญ คำถามทบทวน และโจทย์ปัญหา

### คำสำคัญ

access time, associative mapping, cache hit, cache line, cache memory, cache miss, cache set, data cache, direct access, direct mapping, high-performance computing (HPC), hit, hit ratio, instruction cache, L1 cache, L2 cache, L3 cache, line, locality, logical cache, memory hierarchy, miss, multilevel cache, physical address, physical cache, random access, replacement algorithm, secondary memory, sequential access, set-associative mapping, spatial locality, split cache, tag, temporal locality, unified cache, virtual address, virtual cache, write back, write through

### คำถามทบทวน

**4.1** ความแตกต่างระหว่าง sequential access, direct access และ random access คืออะไร?

**4.2** ความสัมพันธ์ทั่วไประหว่าง access time, ราคาหน่วยความจำ และความจุคืออะไร?

**4.3** หลักการ locality เกี่ยวข้องกับการใช้หน่วยความจำหลายระดับอย่างไร?

**4.4** ความแตกต่างระหว่าง direct mapping, associative mapping และ set-associative mapping คืออะไร?

**4.5** สำหรับ direct-mapped cache ที่อยู่ main memory ถูกมองว่าประกอบด้วยสามฟิลด์ แสดงรายการและนิยามสามฟิลด์นั้น

**4.6** สำหรับ associative cache ที่อยู่ main memory ถูกมองว่าประกอบด้วยสองฟิลด์ แสดงรายการและนิยามสองฟิลด์นั้น

**4.7** สำหรับ set-associative cache ที่อยู่ main memory ถูกมองว่าประกอบด้วยสามฟิลด์ แสดงรายการและนิยามสามฟิลด์นั้น

**4.8** ความแตกต่างระหว่าง spatial locality และ temporal locality คืออะไร?

**4.9** โดยทั่วไป กลยุทธ์สำหรับการใช้ประโยชน์จาก spatial locality และ temporal locality คืออะไร?

### โจทย์ปัญหา

**4.1** set-associative cache ประกอบด้วย 64 line หรือ slot แบ่งเป็น four-line set Main memory มี 4K block ของ 128 word แต่ละ block แสดงรูปแบบที่อยู่ main memory

**4.2** two-way set-associative cache มี line ขนาด 16 byte และขนาดรวม 8 kB Main memory ขนาด 64 MB สามารถระบุที่อยู่ได้ระดับ byte แสดงรูปแบบที่อยู่ main memory

**4.3** สำหรับที่อยู่ main memory แบบ hexadecimal 111111, 666666, BBBBBB แสดงข้อมูลต่อไปนี้ในรูปแบบ hexadecimal:
  - a. ค่า Tag, Line และ Word สำหรับ direct-mapped cache โดยใช้รูปแบบของรูปที่ 4.10
  - b. ค่า Tag และ Word สำหรับ associative cache โดยใช้รูปแบบของรูปที่ 4.12
  - c. ค่า Tag, Set และ Word สำหรับ two-way set-associative cache โดยใช้รูปแบบของรูปที่ 4.15

**4.4** แสดงค่าต่อไปนี้:
  - a. สำหรับตัวอย่าง direct cache ในรูปที่ 4.10: ความยาวที่อยู่, จำนวน addressable unit, ขนาด block, จำนวน block ใน main memory, จำนวน line ใน cache, ขนาด tag
  - b. สำหรับตัวอย่าง associative cache ในรูปที่ 4.12: ความยาวที่อยู่, จำนวน addressable unit, ขนาด block, จำนวน block ใน main memory, จำนวน line ใน cache, ขนาด tag
  - c. สำหรับตัวอย่าง two-way set-associative cache ในรูปที่ 4.15: ความยาวที่อยู่, จำนวน addressable unit, ขนาด block, จำนวน block ใน main memory, จำนวน line ใน set, จำนวน set, จำนวน line ใน cache, ขนาด tag

**4.5** พิจารณา 32-bit microprocessor ที่มี on-chip 16-kB four-way set-associative cache สมมติว่า cache มี line size สี่ 32-bit word วาด block diagram ของ cache นี้ที่แสดงองค์กรและวิธีที่ address field ต่าง ๆ ใช้ระบุ cache hit/miss word จากตำแหน่ง memory ABCDE8F8 แมปไปยังที่ใดใน cache?

**4.6** กำหนด specification ต่อไปนี้สำหรับ external cache memory: four-way set associative; line size สอง 16-bit word; สามารถรองรับ 4K 32-bit word รวมจาก main memory; ใช้กับ 16-bit processor ที่ออก 24-bit address ออกแบบโครงสร้าง cache พร้อมข้อมูลที่เกี่ยวข้องทั้งหมดและแสดงวิธีที่ cache ตีความที่อยู่ของโปรเซสเซอร์

**4.7** Intel 80486 มี on-chip, unified cache มีขนาด 8 kB และมี four-way set-associative organization และ block length สี่ 32-bit word cache ถูกจัดเป็น 128 set มี "line valid bit" เดียวและสามบิต B0, B1 และ B2 ("LRU" bits) ต่อ line เมื่อ cache miss 80486 อ่าน 16-byte line จาก main memory ใน bus memory read burst วาด diagram ที่เรียบง่ายของ cache และแสดงวิธีที่ address field ต่าง ๆ ถูกตีความ

**4.8** พิจารณาเครื่องที่มี byte addressable main memory ขนาด 2¹⁶ byte และ block size 8 byte สมมติว่าใช้ direct mapped cache ประกอบด้วย 32 line กับเครื่องนี้
  - a. 16-bit memory address ถูกแบ่งอย่างไรเป็น tag, line number และ byte number?
  - b. byte ที่มีที่อยู่แต่ละตัวต่อไปนี้จะถูกจัดเก็บใน line ใด?
    - 0001 0001 0001 1011
    - 1100 0011 0011 0100
    - 1101 0000 0001 1101
    - 1010 1010 1010 1010
  - c. สมมติว่า byte ที่มีที่อยู่ 0001 1010 0001 1010 ถูกจัดเก็บใน cache ที่อยู่ของ byte อื่นที่จัดเก็บพร้อมกับมันคืออะไร?
  - d. จำนวน byte ทั้งหมดของ memory ที่สามารถจัดเก็บใน cache คือเท่าไหร่?
  - e. ทำไม tag ถึงถูกจัดเก็บใน cache ด้วย?

**4.9** สำหรับ on-chip cache Intel 80486 ใช้ replacement algorithm ที่เรียกว่า pseudo least recently used เชื่อมกับแต่ละ 128 set ของสี่ line (ระบุว่า L0, L1, L2, L3) มีสามบิต B0, B1 และ B2 replacement algorithm ทำงานดังนี้: เมื่อ line ต้องถูกแทนที่ cache จะระบุก่อนว่าการใช้ล่าสุดมาจาก L0 และ L1 หรือ L2 และ L3 แล้ว cache จะระบุว่า block คู่ใดถูกใช้น้อยกว่าล่าสุดและระบุให้แทนที่
  - a. ระบุวิธีที่บิต B0, B1 และ B2 ถูกตั้งค่า แล้วอธิบายด้วยคำพูดว่าใช้อย่างไรใน replacement algorithm
  - b. แสดงว่า algorithm ของ 80486 เป็น approximation ของ LRU algorithm จริง ๆ
  - c. แสดงให้เห็นว่า LRU algorithm จริงต้องการ 6 bit ต่อ set

**4.10** set-associative cache มี block size สี่ 16-bit word และ set size 2 cache สามารถรองรับรวม 4096 word main memory ขนาดที่สามารถ cache ได้คือ 64K × 32 bit ออกแบบโครงสร้าง cache และแสดงวิธีที่ที่อยู่ของโปรเซสเซอร์ถูกตีความ

**4.11** พิจารณาระบบหน่วยความจำที่ใช้ 32-bit address ระบุที่อยู่ระดับ byte บวกกับ cache ที่ใช้ line size 64 byte
  - a. สมมติว่า direct mapped cache มี tag field ในที่อยู่ 20 bit แสดงรูปแบบที่อยู่และระบุ parameter ต่อไปนี้: จำนวน addressable unit, จำนวน block ใน main memory, จำนวน line ใน cache, ขนาด tag
  - b. สมมติว่า associative cache แสดงรูปแบบที่อยู่และระบุ parameter: จำนวน addressable unit, จำนวน block ใน main memory, จำนวน line ใน cache, ขนาด tag
  - c. สมมติว่า four-way set-associative cache มี tag field ในที่อยู่ 9 bit แสดงรูปแบบที่อยู่และระบุ parameter: จำนวน addressable unit, จำนวน block ใน main memory, จำนวน line ใน set, จำนวน set ใน cache, จำนวน line ใน cache, ขนาด tag

**4.12** พิจารณาคอมพิวเตอร์ที่มีคุณลักษณะต่อไปนี้: main memory รวม 1 MB; word size 1 byte; block size 16 byte; และ cache size 64 kB
  - a. สำหรับที่อยู่ main memory F0010, 01234 และ CABBE ให้ tag ที่สอดคล้องกัน, cache line address และ word offset สำหรับ direct-mapped cache
  - b. ให้สองที่อยู่ main memory ใด ๆ ที่มี tag ต่างกันซึ่งแมปไปยัง cache slot เดียวกันสำหรับ direct-mapped cache
  - c. สำหรับที่อยู่ main memory F0010 และ CABBE ให้ค่า tag และ offset ที่สอดคล้องกันสำหรับ fully-associative cache
  - d. สำหรับที่อยู่ main memory F0010 และ CABBE ให้ค่า tag, cache set และ offset ที่สอดคล้องกันสำหรับ two-way set-associative cache

**4.13** อธิบายเทคนิคง่าย ๆ สำหรับการนำ LRU replacement algorithm ไปใช้ใน four-way set-associative cache

**4.14** พิจารณาตัวอย่าง 4.3 อีกครั้ง คำตอบเปลี่ยนไปอย่างไรถ้า main memory ใช้ block transfer capability ที่มี first-word access time 30 ns และ access time 5 ns สำหรับแต่ละ word ต่อไป?

**4.15** พิจารณา code ต่อไปนี้:
```
for (i = 0; i < 20; i++)
  for (j = 0; j < 10; j++)
    a[i] = a[i] * j
```
  - a. ให้ตัวอย่างหนึ่งของ spatial locality ใน code
  - b. ให้ตัวอย่างหนึ่งของ temporal locality ใน code

**4.16** Generalize สมการ (4.2) และ (4.3) ในภาคผนวก 4A ให้กับ N-level memory hierarchy

**4.17** ระบบคอมพิวเตอร์มี main memory 32K 16-bit word และ 4K word cache แบ่งเป็น four-line set ที่มี 64 word ต่อ line สมมติว่า cache ว่างในตอนแรก โปรเซสเซอร์ดึง word จากตำแหน่ง 0, 1, 2, …, 4351 ตามลำดับ แล้วทำซ้ำลำดับการดึงนี้อีกเก้าครั้ง cache เร็วกว่า main memory 10 เท่า ประมาณการปรับปรุงที่เกิดจากการใช้ cache สมมติว่าใช้ LRU policy สำหรับการแทนที่ block

**4.18** พิจารณา cache ที่มี 4 line ของ 16 byte แต่ละตัว Main memory แบ่งเป็น block ขนาด 16 byte แต่ละ block นั่นคือ block 0 มี byte ที่มีที่อยู่ 0 ถึง 15 เป็นต้น พิจารณาโปรแกรมที่เข้าถึงหน่วยความจำในลำดับที่อยู่ต่อไปนี้: ครั้งเดียว: 63 ถึง 70; วนซ้ำสิบครั้ง: 15 ถึง 32; 80 ถึง 95
  - a. สมมติว่า cache ถูกจัดเป็น direct mapped Memory block 0, 4 และต่อไปถูกกำหนดให้ line 1; block 1, 5 และต่อไปให้ line 2; เป็นต้น คำนวณ hit ratio
  - b. สมมติว่า cache ถูกจัดเป็น two-way set associative มีสอง set ของสอง line แต่ละตัว block คู่ถูกกำหนดให้ set 0 และ block คี่ถูกกำหนดให้ set 1 คำนวณ hit ratio สำหรับ two-way set-associative cache โดยใช้ least recently used replacement scheme

**4.19** พิจารณาระบบหน่วยความจำที่มี parameter ต่อไปนี้:
$$T_c = 100\ \text{ns} \quad C_c = 10^{-4}\ \text{\$/bit}$$
$$T_m = 1200\ \text{ns} \quad C_m = 10^{-5}\ \text{\$/bit}$$
  - a. ราคาของ main memory 1 MB คือเท่าไหร่?
  - b. ราคาของ main memory 1 MB โดยใช้เทคโนโลยี cache memory คือเท่าไหร่?
  - c. ถ้า effective access time มากกว่า cache access time 10% hit ratio H คือเท่าไหร่?

**4.20**
  - a. พิจารณา L1 cache ที่มี access time 1 ns และ hit ratio H = 0.95 สมมติว่าเราสามารถเปลี่ยนการออกแบบ cache (ขนาด cache, cache organization) เพื่อเพิ่ม H เป็น 0.97 แต่เพิ่ม access time เป็น 1.5 ns เงื่อนไขใดบ้างที่ต้องเป็นจริงเพื่อให้การเปลี่ยนแปลงนี้ส่งผลให้ประสิทธิภาพดีขึ้น?
  - d. อธิบายว่าทำไมผลลัพธ์นี้จึงสมเหตุสมผลในเชิงสัญชาตญาณ

**4.21** พิจารณา single-level cache ที่มี access time 2.5 ns, line size 64 byte และ hit ratio H = 0.95 Main memory ใช้ block transfer capability ที่มี first-word (4 byte) access time 50 ns และ access time 5 ns สำหรับแต่ละ word ต่อไป
  - a. access time เมื่อเกิด cache miss คือเท่าไหร่? สมมติว่า cache รอจนกว่า line จะถูกดึงจาก main memory แล้วประมวลผลซ้ำสำหรับ hit
  - b. สมมติว่าการเพิ่ม line size เป็น 128 byte ทำให้ H เพิ่มเป็น 0.97 สิ่งนี้ลด average memory access time หรือไม่?

**4.22** คอมพิวเตอร์มี cache, main memory และ disk ที่ใช้สำหรับ virtual memory ถ้า word ที่อ้างอิงอยู่ใน cache จะใช้เวลา 20 ns ในการเข้าถึง ถ้าอยู่ใน main memory แต่ไม่ใน cache จะต้องใช้ 60 ns เพื่อโหลดเข้า cache แล้วเริ่มอ้างอิงใหม่ ถ้า word ไม่อยู่ใน main memory จะต้องใช้ 12 ms เพื่อดึง word จาก disk ตามด้วย 60 ns เพื่อ copy ไปยัง cache แล้วเริ่มอ้างอิงใหม่ cache hit ratio คือ 0.9 และ main memory hit ratio คือ 0.6 เวลาเฉลี่ยเป็นนาโนวินาทีที่ต้องการในการเข้าถึง word ที่อ้างอิงบนระบบนี้คือเท่าไหร่?

**4.23** พิจารณา cache ที่มี line size 64 byte สมมติว่าโดยเฉลี่ย 30% ของ line ใน cache เป็น dirty word ประกอบด้วย 8 byte
  - a. สมมติว่ามี miss rate 3% (0.97 hit ratio) คำนวณปริมาณ main memory traffic เป็น byte ต่อ instruction สำหรับทั้ง write-through และ write-back policy Memory ถูกอ่านเข้า cache ทีละ line แต่สำหรับ write-back word เดียวสามารถเขียนจาก cache ไปยัง main memory
  - b. ทำซ้ำส่วน a สำหรับ rate 5%
  - c. ทำซ้ำส่วน a สำหรับ rate 7%
  - d. ข้อสรุปใดที่คุณสามารถดึงออกมาจากผลลัพธ์เหล่านี้?

**4.24** บน Motorola 68020 microprocessor การเข้าถึง cache ใช้เวลา clock cycle สองรอบ การเข้าถึง data จาก main memory ผ่าน bus ไปยังโปรเซสเซอร์ใช้เวลา clock cycle สามรอบในกรณีที่ไม่มีการแทรก wait state; ข้อมูลถูกส่งให้โปรเซสเซอร์พร้อมกันกับการส่งไปยัง cache
  - a. คำนวณความยาวที่มีประสิทธิภาพของ memory cycle โดยกำหนด hit ratio 0.9 และ clocking rate 16.67 MHz
  - b. ทำซ้ำการคำนวณโดยสมมติว่ามีการแทรก wait state สองตัวของ one cycle แต่ละตัวต่อ memory cycle คุณสรุปอะไรได้จากผลลัพธ์?

**4.25** สมมติว่าโปรเซสเซอร์มี memory cycle time 300 ns และ instruction processing rate 1 MIPS โดยเฉลี่ยแต่ละ instruction ต้องการ bus memory cycle หนึ่งรอบสำหรับ instruction fetch และหนึ่งรอบสำหรับ operand ที่เกี่ยวข้อง
  - a. คำนวณ utilization ของ bus โดยโปรเซสเซอร์
  - b. สมมติว่าโปรเซสเซอร์ติดตั้ง instruction cache และ hit ratio ที่เกี่ยวข้องคือ 0.5 ระบุผลกระทบต่อ bus utilization

**4.26** ประสิทธิภาพของระบบ single-level cache สำหรับ read operation สามารถระบุลักษณะได้ด้วยสมการต่อไปนี้:
$$T_a = T_c + (1-H)T_m$$
โดยที่ $T_a$ คือ average access time, $T_c$ คือ cache access time, $T_m$ คือ memory access time (memory to processor register) และ H คือ hit ratio สำหรับความเรียบง่าย สมมติว่า word ที่เป็นคำถามถูกโหลดเข้า cache พร้อมกันกับการโหลดเข้า processor register นี่เป็นรูปแบบเดียวกับสมการ (4.2)
  - a. นิยาม $T_b$ = เวลาในการถ่ายโอน line ระหว่าง cache และ main memory และ W = เศษส่วนของ write reference ปรับสมการก่อนหน้าเพื่อรองรับทั้ง write และ read โดยใช้ write-through policy
  - b. นิยาม $W_b$ เป็นความน่าจะเป็นที่ line ใน cache ถูกแก้ไข ให้สมการสำหรับ $T_a$ สำหรับ write-back policy

**4.27** สำหรับระบบที่มี cache สองระดับ นิยาม $T_{c_1}$ = first-level cache access time; $T_{c_2}$ = second-level cache access time; $T_m$ = memory access time; $H_1$ = first-level cache hit ratio; $H_2$ = combined first/second level cache hit ratio ให้สมการสำหรับ $T_a$ สำหรับ read operation

**4.28** สมมติว่ามีคุณลักษณะประสิทธิภาพต่อไปนี้บน cache read miss: หนึ่ง clock cycle เพื่อส่งที่อยู่ไปยัง main memory และสี่ clock cycle เพื่อเข้าถึง 32-bit word จาก main memory และถ่ายโอนไปยังโปรเซสเซอร์และ cache
  - a. ถ้า cache line size เป็น one word miss penalty (เวลาเพิ่มเติมที่ต้องการสำหรับ read เมื่อเกิด read miss) คือเท่าไหร่?
  - b. miss penalty คือเท่าไหรถ้า cache line size เป็นสี่ word และมีการดำเนินการ multiple, nonburst transfer?
  - c. miss penalty คือเท่าไหรถ้า cache line size เป็นสี่ word และดำเนินการ transfer โดยมีหนึ่ง clock cycle ต่อ word transfer?

**4.29** สำหรับการออกแบบ cache ของปัญหาก่อนหน้า สมมติว่าการเพิ่ม line size จาก one word เป็นสี่ word ส่งผลให้ read miss rate ลดลงจาก 3.2% เป็น 1.1% สำหรับทั้ง nonburst transfer และ burst transfer case average miss penalty เฉลี่ยในการ read ทั้งหมดสำหรับ line size ทั้งสองแบบคือเท่าไหร่?

---

## ภาคผนวก 4A คุณลักษณะด้านประสิทธิภาพของหน่วยความจำสองระดับ

ในบทนี้ มีการอ้างถึง cache ที่ทำหน้าที่เป็น buffer ระหว่าง main memory กับโปรเซสเซอร์ สร้างหน่วยความจำภายในสองระดับ สถาปัตยกรรมสองระดับนี้ใช้ประโยชน์จากคุณสมบัติที่เรียกว่า locality เพื่อให้ประสิทธิภาพที่ดีกว่าหน่วยความจำระดับเดียวที่เทียบเคียงได้

กลไก main memory cache เป็นส่วนหนึ่งของสถาปัตยกรรมคอมพิวเตอร์ นำไปใช้ใน hardware และโดยทั่วไปมองไม่เห็นสำหรับ operating system มีอีกสองกรณีของ two-level memory approach ที่ใช้ประโยชน์จาก locality และที่อย่างน้อยบางส่วนนำไปใช้ใน operating system ได้แก่ virtual memory และ disk cache (ตารางที่ 4.6) Virtual memory ศึกษาในบทที่ 8; disk cache อยู่นอกขอบเขตของหนังสือเล่มนี้แต่ศึกษาใน [STAL15] ในภาคผนวกนี้ เราจะดูคุณลักษณะด้านประสิทธิภาพบางส่วนของหน่วยความจำสองระดับที่เหมือนกันในสามแนวทาง

**ตาราง 4.6 คุณลักษณะของหน่วยความจำสองระดับ**

| | Main Memory Cache | Virtual Memory (paging) | Disk Cache |
|---|---|---|---|
| Typical access time ratios | 5:1 (main memory vs. cache) | 10⁶:1 (main memory vs. disk) | 10⁶:1 (main memory vs. disk) |
| Memory management system | Implemented by special hardware | Combination of hardware and system software | System software |
| Typical block or page size | 4 to 128 bytes (cache block) | 64 to 4096 bytes (virtual memory page) | 64 to 4096 bytes (disk block or pages) |
| Access of processor to second level | Direct access | Indirect access | Indirect access |

### Locality

พื้นฐานของข้อได้เปรียบด้านประสิทธิภาพของหน่วยความจำสองระดับคือหลักการที่เรียกว่า **locality of reference** [DENN68] หลักการนี้ระบุว่าการอ้างอิงหน่วยความจำมีแนวโน้มที่จะกระจุกตัว ในช่วงเวลายาว กลุ่มที่ใช้งานจะเปลี่ยนแปลง แต่ในช่วงเวลาสั้น โปรเซสเซอร์ส่วนใหญ่ทำงานกับกลุ่มการอ้างอิงหน่วยความจำที่คงที่

โดยสัญชาตญาณ หลักการของ locality สมเหตุสมผล พิจารณา reasoning ต่อไปนี้:

1. ยกเว้น branch และ call instruction ซึ่งคิดเป็นเพียงเศษส่วนเล็กน้อยของ program instruction ทั้งหมด การทำงานของโปรแกรมเป็น sequential ดังนั้นในกรณีส่วนใหญ่ instruction ถัดไปที่จะดึงจะตามหลัง instruction สุดท้ายที่ดึงมาทันที

2. การมีลำดับยาวของ procedure call ที่ไม่ถูกขัดจังหวะตามด้วยลำดับ return ที่สอดคล้องกันเป็นเรื่องที่เกิดขึ้นน้อย โดยทั่วไปโปรแกรมจะถูกจำกัดอยู่ในช่วงความลึกของการเรียก procedure ที่แคบ ดังนั้น ในช่วงเวลาสั้นการอ้างอิงไปยัง instruction มีแนวโน้มที่จะอยู่ใน procedure จำนวนน้อย

3. iterative construct ส่วนใหญ่ประกอบด้วย instruction จำนวนน้อยที่ทำซ้ำหลายครั้ง ตลอดระยะเวลาของการ iteration การคำนวณจึงถูกจำกัดอยู่ในส่วนเล็ก ๆ ที่ต่อเนื่องกันของโปรแกรม

4. ในโปรแกรมหลายตัว การคำนวณส่วนใหญ่เกี่ยวข้องกับการประมวลผล data structure เช่น array หรือลำดับ record ในหลายกรณี การอ้างอิงต่อเนื่องไปยัง data structure เหล่านี้จะเป็น data item ที่อยู่ใกล้เคียงกัน

reasoning นี้ได้รับการยืนยันในการศึกษาหลายชิ้น อ้างอิงถึงข้อ 1 การศึกษาหลายชิ้นวิเคราะห์พฤติกรรมของ high-level language program ตารางที่ 4.7 รวมผลลัพธ์สำคัญ ซึ่งวัดการปรากฏของ statement ประเภทต่าง ๆ ในระหว่างการทำงาน จากการศึกษาต่อไปนี้ การศึกษาแรกสุดของพฤติกรรม programming language โดย Knuth [KNUT71] ตรวจสอบ FORTRAN program ที่ใช้เป็น student exercise Tanenbaum [TANE78] เผยแพร่การวัดที่รวบรวมจาก procedure มากกว่า 300 ตัวที่ใช้ใน operating-system program Patterson and Sequein [PATT82a] วิเคราะห์ชุดการวัดที่นำมาจาก compiler และ program สำหรับ typesetting, computer-aided design (CAD), sorting และ file comparison Huck [HUCK83] วิเคราะห์สี่โปรแกรมที่ตั้งใจจะเป็นตัวแทนของ general-purpose scientific computing มีข้อตกลงที่ดีในผลลัพธ์ของ language และ application ที่หลากหลายนี้ว่า branch และ call instruction คิดเป็นเพียงเศษส่วนของ statement ที่ทำงานในระหว่างอายุการใช้งานของโปรแกรม ดังนั้น การศึกษาเหล่านี้ยืนยัน assertion 1

**ตาราง 4.7 ความถี่ Dynamic สัมพัทธ์ของการดำเนินการภาษาระดับสูง**

| Study | [HUCK83] Pascal Scientific | [KNUT71] FORTRAN Student | [PATT82a] Pascal System | [PATT82a] C System | [TANE78] SAL System |
|---|---|---|---|---|---|
| Assign | 74 | 67 | 45 | 38 | 42 |
| Loop | 4 | 3 | 5 | 3 | 4 |
| Call | 1 | 3 | 15 | 12 | 12 |
| IF | 20 | 11 | 29 | 43 | 36 |
| GOTO | 2 | 9 | — | 3 | — |
| Other | — | 7 | 6 | 1 | 6 |

เกี่ยวกับ assertion 2 การศึกษาที่รายงานใน [PATT85a] ให้การยืนยัน รูปที่ 4.20 แสดงพฤติกรรม call-return แต่ละ call แสดงด้วยเส้นที่เคลื่อนลงและไปทางขวา และแต่ละ return โดยเส้นที่เคลื่อนขึ้นและไปทางขวา ในรูป window ที่มีความลึกเท่ากับ 5 ถูกนิยาม เฉพาะลำดับของ call และ return ที่มีการเคลื่อนสุทธิ 6 ในทิศทางใดทิศทางหนึ่งทำให้ window เคลื่อน ดังที่เห็น โปรแกรมที่ทำงานอยู่สามารถอยู่ใน window ที่อยู่กับที่เป็นระยะเวลายาว การศึกษาโดยนักวิเคราะห์คนเดียวกันของ C และ Pascal program แสดงว่า window ที่มีความลึก 8 จะต้องเคลื่อนเพียงน้อยกว่า 1% ของ call หรือ return [TAMI83]

ในวรรณกรรมมีการแยกแยะระหว่าง spatial locality และ temporal locality **Spatial locality** หมายถึงแนวโน้มของการทำงานที่เกี่ยวข้องกับตำแหน่งหน่วยความจำจำนวนหนึ่งที่กระจุกตัว ซึ่งสะท้อนแนวโน้มของโปรเซสเซอร์ในการเข้าถึง instruction ตามลำดับ Spatial locality ยังสะท้อนแนวโน้มของโปรแกรมในการเข้าถึงตำแหน่งข้อมูลตามลำดับ เช่น เมื่อประมวลผล table ของข้อมูล **Temporal locality** หมายถึงแนวโน้มของโปรเซสเซอร์ในการเข้าถึงตำแหน่งหน่วยความจำที่ใช้ล่าสุด ตัวอย่างเช่น เมื่อ iteration loop ถูกทำงาน โปรเซสเซอร์จะทำชุด instruction เดิมซ้ำ ๆ

โดยเดิมทีแล้ว temporal locality ถูกใช้ประโยชน์โดยการเก็บค่า instruction และ data ที่ใช้ล่าสุดไว้ใน cache memory และโดยการใช้ประโยชน์จาก cache hierarchy Spatial locality โดยทั่วไปถูกใช้ประโยชน์โดยใช้ cache block ขนาดใหญ่กว่าและโดยการรวม prefetching mechanism (การดึง item ที่คาดว่าจะใช้) เข้าไปใน cache control logic ล่าสุดมีการวิจัยอย่างมากในการปรับปรุงเทคนิคเหล่านี้เพื่อให้ได้ประสิทธิภาพที่มากขึ้น แต่กลยุทธ์พื้นฐานยังคงเดิม

### การทำงานของหน่วยความจำสองระดับ

คุณสมบัติ locality สามารถใช้ประโยชน์ในการสร้างหน่วยความจำสองระดับ upper-level memory (M1) เล็กกว่า เร็วกว่า และแพงกว่า (ต่อบิต) กว่า lower-level memory (M2) M1 ถูกใช้เป็น temporary store สำหรับส่วนหนึ่งของเนื้อหาของ M2 ที่ใหญ่กว่า เมื่อมีการอ้างอิงหน่วยความจำ จะพยายามเข้าถึง item ใน M1 ถ้าสำเร็จก็เข้าถึงได้อย่างรวดเร็ว ถ้าไม่สำเร็จ block ของตำแหน่งหน่วยความจำจะถูก copy จาก M2 ไปยัง M1 แล้วการเข้าถึงจะเกิดขึ้นผ่าน M1 เนื่องจาก locality เมื่อ block ถูกนำเข้า M1 ควรมีการเข้าถึงตำแหน่งใน block นั้นจำนวนหนึ่ง ส่งผลให้บริการรวมเร็ว

เพื่อแสดงเวลาเฉลี่ยในการเข้าถึง item เราต้องพิจารณาไม่เพียงความเร็วของหน่วยความจำสองระดับ แต่ยังความน่าจะเป็นที่การอ้างอิงที่กำหนดสามารถพบได้ใน M1 เรามี:

$$T_s = H \times T_1 + (1-H) \times (T_1 + T_2) = T_1 + (1-H) \times T_2 \quad (4.2)$$

โดยที่:
- $T_s$ = เวลาการเข้าถึงเฉลี่ย (system)
- $T_1$ = access time ของ M1 (เช่น cache, disk cache)
- $T_2$ = access time ของ M2 (เช่น main memory, disk)
- $H$ = hit ratio (เศษส่วนของเวลาที่พบการอ้างอิงใน M1)

รูปที่ 4.2 แสดง average access time ในฐานะฟังก์ชันของ hit ratio ดังที่เห็น สำหรับเปอร์เซ็นต์ hit สูง เวลาเข้าถึงรวมเฉลี่ยใกล้เคียงกับ M1 มากกว่า M2

### ประสิทธิภาพ

มาดู parameter บางอย่างที่เกี่ยวข้องกับการประเมินกลไกหน่วยความจำสองระดับ ก่อนอื่นพิจารณาค่าใช้จ่าย เรามี:

$$C_s = \frac{C_1 S_1 + C_2 S_2}{S_1 + S_2} \quad (4.3)$$

โดยที่:
- $C_s$ = ราคาต่อบิตเฉลี่ยสำหรับหน่วยความจำสองระดับรวม
- $C_1$ = ราคาต่อบิตเฉลี่ยของ upper-level memory M1
- $C_2$ = ราคาต่อบิตเฉลี่ยของ lower-level memory M2
- $S_1$ = ขนาดของ M1
- $S_2$ = ขนาดของ M2

เราต้องการ $C_s \approx C_2$ เมื่อกำหนดว่า $C_1 \gg C_2$ ต้องการ $S_1 < S_2$

ต่อมาพิจารณา access time สำหรับหน่วยความจำสองระดับเพื่อให้ได้การปรับปรุงประสิทธิภาพที่มีนัยสำคัญ เราต้องการ $T_s \approx T_1$ เมื่อกำหนดว่า $T_1 \ll T_2$ จำเป็นต้องมี hit ratio ใกล้ 1

ดังนั้นเราต้องการให้ M1 เล็กเพื่อลดค่าใช้จ่าย และใหญ่เพื่อปรับปรุง hit ratio และประสิทธิภาพ มีขนาดของ M1 ที่ตอบสนองความต้องการทั้งสองในระดับที่สมเหตุสมผลหรือไม่? เราสามารถตอบคำถามนี้ด้วยชุดคำถามย่อย:

- Hit ratio ที่ต้องการเพื่อให้ $T_s \approx T_1$ คือเท่าไหร่?
- ขนาดของ M1 ที่ต้องการเพื่อรับประกัน hit ratio ที่ต้องการคือเท่าไหร่?
- ขนาดนี้ตอบสนองความต้องการด้านค่าใช้จ่ายหรือไม่?

เพื่อหาคำตอบ พิจารณา $T_1/T_s$ ซึ่งเรียกว่า **access efficiency** เป็นการวัดว่า average access time ($T_s$) ใกล้เคียงกับ M1 access time ($T_1$) มากแค่ไหน จากสมการ (4.2):

$$\frac{T_1}{T_s} = \frac{1}{1 + (1-H)\frac{T_2}{T_1}} \quad (4.4)$$

รูปที่ 4.22 วาดกราฟ $T_1/T_s$ ในฐานะฟังก์ชันของ hit ratio H โดยมีปริมาณ $T_2/T_1$ เป็น parameter โดยทั่วไป on-chip cache access time เร็วกว่า main memory access time ประมาณ 25 ถึง 50 เท่า (กล่าวคือ $T_2/T_1$ คือ 25 ถึง 50) off-chip cache access time เร็วกว่า main memory access time ประมาณ 5 ถึง 15 เท่า (กล่าวคือ $T_2/T_1$ คือ 5 ถึง 15) และ main memory access time เร็วกว่า disk access time ประมาณ 1000 เท่า ($T_2/T_1 = 1000$) ดังนั้น hit ratio ในช่วงใกล้ 0.9 ดูเหมือนจะต้องการเพื่อตอบสนองความต้องการด้านประสิทธิภาพ

ตอนนี้เราสามารถกำหนดคำถามเกี่ยวกับขนาดหน่วยความจำสัมพัทธ์ได้อย่างแม่นยำขึ้น Hit ratio ที่ 0.8 หรือดีกว่านั้นสมเหตุสมผลสำหรับ $S_1 \ll S_2$ หรือไม่? ซึ่งจะขึ้นอยู่กับปัจจัยหลายอย่าง รวมถึงลักษณะของซอฟต์แวร์ที่ทำงานอยู่และรายละเอียดของการออกแบบหน่วยความจำสองระดับ ตัวกำหนดหลักคือแน่นอนว่าระดับของ locality รูปที่ 4.23 แสดงให้เห็นผลที่ locality มีต่อ hit ratio ชัดเจน ถ้า M1 มีขนาดเดียวกับ M2 แล้ว hit ratio จะเป็น 1.0: item ทั้งหมดใน M2 ก็จะถูกจัดเก็บใน M1 เสมอ สมมติว่าไม่มี locality กล่าวคือ การอ้างอิงเป็นแบบสุ่มสมบูรณ์ ในกรณีนั้น hit ratio ควรเป็นฟังก์ชัน linear อย่างเคร่งครัดของขนาดหน่วยความจำสัมพัทธ์ ตัวอย่างเช่น ถ้า M1 มีขนาดครึ่งหนึ่งของ M2 ดังนั้นในเวลาใดก็ตาม ครึ่งหนึ่งของ item จาก M2 ก็อยู่ใน M1 และ hit ratio จะเป็น 0.5 ในทางปฏิบัติ อย่างไรก็ตาม มีระดับของ locality บางอย่างในการอ้างอิง ผลของ moderate และ strong locality แสดงในรูป โปรดสังเกตว่ารูปที่ 4.23 ไม่ได้ดึงมาจากข้อมูลหรือโมเดลเฉพาะ รูปแนะนำประเภทประสิทธิภาพที่เห็นกับระดับต่าง ๆ ของ locality

ดังนั้นถ้ามี strong locality จะเป็นไปได้ที่จะได้ hit ratio สูงแม้กระทั่งกับขนาด upper-level memory ที่ค่อนข้างเล็ก ตัวอย่างเช่น การศึกษาหลายชิ้นแสดงให้เห็นว่า cache ขนาดค่อนข้างเล็กจะให้ hit ratio เกิน 0.75 โดยไม่ขึ้นกับขนาดของ main memory (เช่น [AGAR89], [PRZY88], [STRE83] และ [SMIT82]) cache ในช่วง 1K ถึง 128K word โดยทั่วไปเพียงพอ ในขณะที่ main memory ในปัจจุบันโดยทั่วไปอยู่ในช่วง gigabyte เมื่อเราพิจารณา virtual memory และ disk cache เราจะอ้างถึงการศึกษาอื่น ๆ ที่ยืนยันปรากฏการณ์เดียวกัน กล่าวคือ M1 ขนาดเล็กสัมพัทธ์ให้ hit ratio สูงเนื่องจาก locality

ทำให้เรามาถึงคำถามสุดท้ายที่ระบุไว้ก่อนหน้า: ขนาดสัมพัทธ์ของหน่วยความจำสองตัวตอบสนองความต้องการด้านค่าใช้จ่ายหรือไม่? คำตอบชัดเจนว่าใช่ ถ้าเราต้องการเพียง upper-level memory ขนาดค่อนข้างเล็กเพื่อให้ได้ประสิทธิภาพที่ดี ราคาต่อบิตเฉลี่ยของหน่วยความจำสองระดับจะเข้าใกล้ค่าของ lower-level memory ที่ถูกกว่า

โปรดสังเกตว่าด้วย L2 cache หรือแม้กระทั่ง L2 และ L3 cache ที่เกี่ยวข้อง การวิเคราะห์ซับซ้อนกว่ามาก ดู [PEIR99] และ [HAND98] สำหรับการอภิปราย

---

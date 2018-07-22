# EBS

Elastic Block Store EC2 인스턴스에 장착하여 사용할 수 있는 가상 저장 장치이다. EC2 인스턴스에서 제공하는 기본 용량보다 더 사용해야 할 때, 운영체제를 중단시키지 않고 용량을 자유롭게 늘리고 싶을 때, 영구적인 데이터 보관이 필요할 때, RAID 등의 고급 기능이 필요할 때 사용.



**RAID \(redundant array of inexpensive disk\)** 데이터를 분할해서 복수의 자기 디스크 장치에 대해 병렬로 데이터를 읽는 장치 또는 읽는 방식.

**AMI \(Amazon Machine Image\)** OS가 설치된 형태이며 이 AMI로 EC2 인스턴스를 생성합니다.

**IOPS \(INput/OUTput Operation Per Second\)** 저장 장치의 성능 측정 단위. 16KB 단위로 처리되기 때문에 16KB를 채워서 전송하면 효율이 높아진다.



* **EBS** **볼륨** OS에서 봤을 때 하드디스크나 SSD와 동일하다. 따라서 RAID를 구성할 수 있다. RAID 0, RAID 1, RAID 1+0\(RAID 10\)으로 구성할 수 있다.
* **EBS** **스냅샷** 백업용, Private용, 다른 Region으로 이동할 때 사용하고 요금은 S3 데이터 저장 요금에 합산된다.  


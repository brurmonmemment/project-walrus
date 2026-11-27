# Retail
Info (dumps, logs, etc.) pulled from the SSD running normal retail firmware

Envt: Arch Linux, kernel ver. 7.3.5-arch1-1\
Tools: nvme-cli 3.2 + libnvme 3.2\
SSD: /dev/nvme0 (SSD is in the motherboard slot), PCIe addr 01:00.0

### identify-controller
SSD controller info\
Via: `sudo nvme id ctrl /dev/nvme0`

### identify-namespace
Info on the exposed storage device\
Via: `sudo nvme id ns /dev/nvme0n1`

### effects
A list of commands supported by the controller\
Via: `sudo nvme log effects /dev/nvme0`

### info-pcie
PCIe device info + connection info\
Bottleneck oat since I'm doing this on a Steam Deck and the NVMe slot is only gen 3 fml\
Via: `sudo lspci -vv -s 0000:01:00.0`
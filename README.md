# ECE551B
# Mini Pump Acoustic Dataset
This is a collection of audio recordings for use in acoustic classification and anomaly detection of for a submersible water pump.<br /><br />
Author: Silas Curfman<br />
Course: ECE-551, University of New Mexico, Spring 2023<br />
email: sgc98944@protonmail.com<br />

## Contents
|File/Folder | Description | Items | Format | Size |
|------------|:------------|:------|:-----|:-----|
| 0db | No background noise, general information| 5 | n/a | 531 MB |
| /data | sub folders | 5 | n/a | 527 MB |
| /data/raw | original recordings, unedited, untrimmed | 96 | wav/audio | 157 MB |
| /data/10_sec_splits | all recordings, trimmed into 10 sec segments| 5 | wav/audio |212 MB |
| /data/train | (14) rec of classes: idle, speed1, speed2, and dry_running | 56 | wav/audio| 94.2 MB |
| /data/test  | (4-5) rec of classes: idle, speed1, speed2, and dry_running | 19 | wav/audio | 28.2 MB |
| /data/anomaly | (21) rec of class: cavitation for anomaly detection | 21 | wav/audio | 34.9 MB |

## Hardware
* Pump: 
  * Mini Submersible Water Pump for Pond, Aquariums, Fish Tanks.
  * 50 GPH
  * Variable Speed
  * 3W, 110v / 60hz
* Microphone: 
   * Model: ONN USB Cardioid Microphone
   * Frequency: 20 Hz - 20 KHz
   * Sampling rate: 48 KHz / 16bit
   * Data Connection: USB
   * Mounting: Fixed Tripod, 5-8 inches from audio source


## License
The data and associated code are being released under the Open Use of Data Agreement, with the intention of promoting open research using this dataset.

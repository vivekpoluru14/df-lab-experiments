# DF-lab-experiments
# Experiment 1: Evidence Acquisition Using AccessData FTK Imager

## Aim

To acquire a forensic disk image from a physical storage device using AccessData FTK Imager and verify the integrity of the acquired image using MD5 and SHA1 hash values.

## Software Used

- AccessData FTK Imager 4.7.1.2
- Windows

## Introduction

FTK Imager is a computer forensic tool developed by AccessData. It is used for acquiring and analyzing digital forensic evidence.

FTK Imager can acquire:

- Volatile memory (RAM)
- Non-volatile memory such as hard disks and USB drives
- Physical drives
- Logical drives
- Image files
- Contents of folders
- CDs/DVDs

In this experiment, a physical USB storage device was acquired and converted into a forensic disk image.

## Procedure

### Step 1: Open FTK Imager

Open **AccessData FTK Imager 4.7.1.2**.

Navigate to the option for creating a disk image.



### Step 2: Select Evidence Source

Select **Physical Drive** and click **Next**.



### Step 3: Select Physical Drive

Select the physical drive that needs to be acquired.

The device used in this experiment was:

**SanDisk Cruzer Blade USB Device**

Click **Finish**.



### Step 4: Select Image Type

Select **Raw (dd)** and click **Next**.

### Step 5: Enter Evidence Information

The following evidence information was entered:

- Case Number: 1
- Evidence Number: 1
- Unique Description: DF
- Examiner: Vivek Poluru
- Notes: EXP 1

Click **Next**.


### Step 6: Select Image Destination

The image was saved in the following destination:

`D:\3-1\Digital Forensics`

Image Filename:

`diskimage`

Image Fragment Size:

`0 MB`


### Step 7: Create Image

The source and destination information were displayed.

The option **Verify images after they are created** was selected.

Click **Start** to begin the acquisition.


### Step 8: Image Acquisition

FTK Imager started creating the forensic image from the physical drive.



### Step 9: Image Verification

After acquisition, FTK Imager verified the created forensic image.

The verification process checks the integrity of the acquired image using hash values.



### Step 10: Verification Result

The verification result showed:

- MD5 Verify Result: **Match**
- SHA1 Verify Result: **Match**
- Bad Blocks: **No bad blocks found in image**



### Step 11: Image Summary

The image summary provided details about the acquired physical drive.

Important information included:

- Source Type: Physical
- Drive Model: SanDisk Cruzer Blade USB Device
- Drive Interface Type: USB
- Source Data Size: 59112 MB
- Sector Count: 121061376
- Bytes per Sector: 512



### Step 12: Hash Verification

The image summary showed that the computed and reported hash values matched.

**MD5:**

`9f1f7659712cde7bc536dd82f341b5ce`

**SHA1:**

`abaca319c85c310078f410c02f6b11951af63334`

Both verification results were **Match**.



## Result

The physical USB drive was successfully acquired using **AccessData FTK Imager 4.7.1.2** and converted into a **Raw (dd) forensic image**.

The acquired image was successfully verified using MD5 and SHA1 hash values.

## Verification Results

| Parameter | Result |
|---|---|
| Image Type | Raw (dd) |
| Source | Physical Drive |
| Device | SanDisk Cruzer Blade USB Device |
| Source Size | 59112 MB |
| MD5 Verification | Match |
| SHA1 Verification | Match |
| Bad Blocks | No bad blocks found |

<img width="520" height="469" alt="WhatsApp Image 2026-08-10 at 10 16 28 PM (2)" src="https://github.com/user-attachments/assets/bde948f3-a5e8-4cf5-9c3f-5e415bde4af4" />
<img width="1600" height="806" alt="WhatsApp Image 2026-08-10 at 10 16 28 PM (3)" src="https://github.com/user-attachments/assets/f82b525c-bc65-40ee-a457-83196ddfa9fa" />
<img width="1600" height="770" alt="WhatsApp Image 2026-08-10 at 10 16 28 PM (4)" src="https://github.com/user-attachments/assets/a8979d94-e831-46c3-85f3-2f95722ca1c0" />
<img width="730" height="590" alt="WhatsApp Image 2026-08-10 at 10 16 28 PM (5)" src="https://github.com/user-attachments/assets/7785c573-a5c9-45ee-9cdd-db1a5582021d" />
<img width="472" height="364" alt="WhatsApp Image 2026-08-10 at 10 16 28 PM" src="https://github.com/user-attachments/assets/c6c4cebc-968b-492c-a75a-56e6bea54014" />
<img width="735" height="541" alt="WhatsApp Image 2026-08-10 at 10 16 29 PM (1)" src="https://github.com/user-attachments/assets/0488e783-a9d3-4d31-9c8c-5a0f26be325c" />
<img width="597" height="490" alt="WhatsApp Image 2026-08-10 at 10 16 29 PM (2)" src="https://github.com/user-attachments/assets/44d4329f-b33d-46c2-8053-f2c4eeab0522" />
<img width="621" height="574" alt="WhatsApp Image 2026-08-10 at 10 16 29 PM (3)" src="https://github.com/user-attachments/assets/83a96014-2914-4517-a69f-17010d48dc02" />
<img width="658" height="449" alt="WhatsApp Image 2026-08-10 at 10 16 29 PM (4)" src="https://github.com/user-attachments/assets/09544ee6-0d06-4834-a111-abd1c4aee2b0" />
<img width="1600" height="847" alt="WhatsApp Image 2026-08-10 at 10 16 29 PM (6)" src="https://github.com/user-attachments/assets/37c3406f-16ae-4075-bfd1-7e3efedeeb18" />

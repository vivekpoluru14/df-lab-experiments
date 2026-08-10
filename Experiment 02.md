# Experiment 2: Recover Deleted or Damaged Files Using TestDisk

## Aim

To recover a missing partition and repair a corrupted partition using TestDisk.

## Software Used

* TestDisk

## Introduction

TestDisk is a data recovery tool used to recover missing partitions and repair corrupted partition structures.

It can be used to:

* Recover missing partitions
* Search for lost partitions
* Repair corrupted partition tables
* Recover damaged file systems
* Repair NTFS boot sectors
* List and verify files from recovered partitions

In this experiment, TestDisk was used to identify a missing logical partition, recover the correct partition structure, and repair a damaged NTFS boot sector.

## Procedure

### Step 1: Create Log File

Open **TestDisk**.

TestDisk displays the log creation options.

Select **Create** to create a log file containing technical information and messages.

Other options are:

* **Create** – Creates a new log file.
* **Append** – Adds information to an existing log file.
* **None** – Does not create a log file.

Select the required option and press **Enter** to proceed.

### Step 2: Select Disk

TestDisk displays all detected hard drives with their sizes.

Use the **Up/Down Arrow keys** to select the hard drive containing the lost partition.

Press **Enter** to proceed.

### Step 3: Select Partition Table Type

TestDisk displays different partition table types.

Select the appropriate partition table type.

Usually, the default value selected by TestDisk is correct because TestDisk automatically detects the partition table type.

Press **Enter** to proceed.

### Step 4: Analyse the Current Partition Table

TestDisk displays the available menu options.

Select **Analyse** to check the current partition structure and search for lost partitions.

Press **Enter** to proceed.

The current partition structure is then displayed.

Examine the partition structure to identify missing partitions and errors.

### Step 5: Identify Partition Errors

The partition structure showed that:

* The first partition was listed twice, indicating a corrupted partition or invalid partition table entry.
* An **Invalid NTFS boot** message indicated a faulty NTFS boot sector.
* Only one logical partition was available in the extended partition.
* One logical partition was missing.

Select **Quick Search** and press **Enter** to continue.

### Step 6: Perform Quick Search

TestDisk starts searching for lost partitions.

During the **Quick Search**, TestDisk found two partitions, including the missing logical partition labeled **Partition 3**.

Highlight the missing partition and press **P** to list its files.

The directories and data were correctly listed.

Press **Q** to return to the previous screen and press **Enter** to proceed.

### Step 7: Perform Deeper Search

If all partitions are not found during the Quick Search, select **Deeper Search**.

Deeper Search searches for additional partitions by checking backup boot sectors and backup superblocks.

It searches for:

* FAT32 backup boot sectors
* NTFS backup superblocks
* ext2/ext3 backup superblocks

After the Deeper Search, the missing partition was found using the backup boot sector.

The message **"NTFS found using backup sector!"** was displayed.

### Step 8: Verify the Correct Partition

Highlight the required partition and press **P** to list its files.

The first logical partition showed that its file system was damaged.

Return to the previous screen using **Q**.

Then select the second partition and press **P** again to list its files.

The files were successfully displayed, confirming that the correct partition had been found.

Use the **Left/Right Arrow keys** to navigate through folders and verify the files.

### Step 9: Change Partition Status

TestDisk provides different partition statuses:

* Primary
* * Bootable
* Logical
* Deleted

The correct partition was initially marked as **D (Deleted)**.

Use the **Left/Right Arrow keys** to change the status from:

**D (Deleted) → L (Logical)**

This allows the partition to be recovered.

Press **Enter** to proceed.

### Step 10: Write the Partition Table

TestDisk now displays the new partition structure.

If all required partitions are correctly listed, select **Write**.

Press **Enter** and confirm with **Y** and **OK**.

The recovered partitions are then registered in the partition table.

The extended partition is automatically set by TestDisk based on the detected partition structure.

### Step 11: Repair NTFS Boot Sector

The boot sector of the first partition was still damaged.

The NTFS boot sector status was:

* Boot sector: **Bad**
* Backup boot sector: **Valid**

The boot sector and backup boot sector were not identical.

Select **Backup BS** to copy the backup boot sector over the damaged boot sector.

Press **Enter**, confirm with **Y**, and select **OK**.

### Step 12: Verify Boot Sector Recovery

After the repair, TestDisk displayed the message indicating that:

* The boot sector is now OK.
* The backup boot sector is also OK.
* Both boot sectors are identical.
* The NTFS boot sector was successfully recovered.

Press **Enter** to quit TestDisk.

### Step 13: Restart the Computer

TestDisk displays a message stating that the computer must be restarted to access the recovered data.

Press **Enter** and restart the computer.

## Result

The missing partition was successfully identified and recovered using **TestDisk**.

The corrupted partition structure was repaired by identifying the correct partition and changing its status from **Deleted (D)** to **Logical (L)**.

The damaged NTFS boot sector was also successfully recovered using the valid backup boot sector.

# Output Screenshots
<img width="1117" height="661" alt="Screenshot 2026-08-08 095725" src="https://github.com/user-attachments/assets/55b01d6c-a207-478a-b44d-8dc2f8db2943" />
<img width="1125" height="654" alt="Screenshot 2026-08-08 095747" src="https://github.com/user-attachments/assets/63b5e8f4-02ca-4c83-a0f7-959c0aea1856" />
<img width="1116" height="650" alt="Screenshot 2026-08-08 095808" src="https://github.com/user-attachments/assets/bf202e61-64f6-4c51-997a-c88a9450ab48" />
<img width="1115" height="651" alt="Screenshot 2026-08-08 095828" src="https://github.com/user-attachments/assets/5270759c-cb71-44c2-9a2e-9ab0e9e65e69" />
<img width="1115" height="650" alt="Screenshot 2026-08-08 095844" src="https://github.com/user-attachments/assets/693b33cd-06c2-4b36-908f-47aa0b808bfe" />
<img width="1119" height="653" alt="Screenshot 2026-08-08 095911" src="https://github.com/user-attachments/assets/2266d6be-9364-40bf-9b43-7d40dfe57224" />
<img width="917" height="517" alt="Screenshot 2026-08-08 100412" src="https://github.com/user-attachments/assets/47612444-8ea3-4187-991c-e3f932bcbcde" />
<img width="933" height="467" alt="Screenshot 2026-08-08 100423" src="https://github.com/user-attachments/assets/f8d113ad-9c04-4ae8-806f-c7d299ccafa4" />
<img width="926" height="750" alt="Screenshot 2026-08-08 101038" src="https://github.com/user-attachments/assets/11ad42fb-a48d-4523-9be7-8b3fe9ab21fb" />
<img width="927" height="477" alt="Screenshot 2026-08-08 101102" src="https://github.com/user-attachments/assets/54069931-a2bd-4911-86dd-bb511bde43ff" />
<img width="940" height="497" alt="Screenshot 2026-08-08 101111" src="https://github.com/user-attachments/assets/6b7d840b-24cc-46e3-bb54-e962384bd8b4" />
<img width="1005" height="500" alt="Screenshot 2026-08-08 163929" src="https://github.com/user-attachments/assets/9a8a86ff-1fa3-4837-a4e0-53786677d86c" />

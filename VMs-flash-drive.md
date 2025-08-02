<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

# make the headings bold and the title title

Certainly! Here is the updated tutorial with **bold headings** and the **title made a title style** for clarity:

# Tutorial: Saving, Creating, and Running VirtualBox VMs from an External Drive

**Step 1: Prepare Your External Drive**

- Ensure your external drive (USB HDD or SSD) is connected and formatted with a file system that supports large files (exFAT, NTFS on Windows; ext4 on Linux).
- Confirm there is enough free space on the drive for your virtual machine files.

**Step 2: Save New VM Files Directly to the External Drive**

- When creating a new VM, **manually specify the storage location for the VM and its virtual disk files to a folder on your external drive**:

1. Open VirtualBox and click **New** to start the VM creation wizard.
2. Enter a name for your VM and select the correct OS type and version.
3. When prompted to choose the folder for the VM, **click the folder icon to browse and select a folder on your external drive** (you can create a new folder specifically for the VM).
4. Create a virtual hard disk and save the resulting `.vdi` file inside that external drive folder.
5. Finish the VM creation process.

*(Optional)* You can set the external drive as the **Default Machine Folder** so new VMs default to saving there:

- Go to **File > Preferences > General** in VirtualBox and set **Default Machine Folder** to a folder on your external drive.
- But manually choosing the folder during VM creation gives you more flexibility.

**Step 3: Creating a VM From Existing .vdi Files on External Drive**

- Open VirtualBox on your host computer.
- Click **Machine > New**.
- Enter the VM name, select OS type and version matching the content of the .vdi.
- When asked about the hard disk, choose **Use an existing virtual hard disk file**, then browse to your external drive and select the `.vdi` file.
- Complete the VM setup wizard.

**Step 4: Running the VM from the External Drive**

- Connect the external drive to your host computer.
- Open VirtualBox, and if necessary, **Add** the VM by going to **Machine > Add** and selecting the `.vbox` configuration file from the external drive folder.
- Start the VM normally. All VM disk input/output operations will run from the external drive.
- For best performance, use a USB 3.0 or faster drive. Running VMs from slower USB drives may cause lag.

**Important Notes \& Best Practices**

- Always shut down your VM cleanly before disconnecting the external drive to avoid data corruption.
- VirtualBox must be installed on any host machine where you plan to run the VM.
- Copy the whole VM folder (including `.vbox`, `.vdi`, Snapshots, Logs) to the external drive for full portability and proper operation.
- Avoid unplugging or disconnecting the external drive while VirtualBox or the VM is running.
- You can keep multiple VMs on the external drive organized by placing each VM in its own folder.

If you need further help with snapshots, advanced portable VM setups, or anything else, just ask!


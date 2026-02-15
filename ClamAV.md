
#### Installation

	sudo apt install clamav clamtk

- `clamav` - AV engine
- `clamtk` - GUI

#### Database Update

	freshclam

This will update the AV database

#### Scanning Files and Directories

We can do this either by the `CLI` or through the `GUI`

**File Scan**

Scanning a file from the CLI:

	clamscan ~/home/target_file

In order to test our proficiency we can download an infected file from **eicar.org** and practice with it

After we download it we run

	clamscan eicar_com.zip

When we check the results spitted we can see something like:

	Scanned files: 1
	Infected files: 1

Yet, since we did not specify, no actions were taken

**Dir Scan**

Scanning a directory from the CLI:

	clamscan ~/home/target_dir

This will scan a directory and its contents, **but not other directories** for that we need to specify the `recursive` flag

	clamscan -r ~/home/target_dir

If we want to have only infect files displayed we can add the `infect` flag, as such:

	clamscan -i -r ~/home/target_dir

#### Taking Action on Infected Files

**Copy**

In order to **copy** an infected file into a quarantine directory we do:

	clamscan -r --copy=~/home/target_quarantined_dir ~/home/scanned_dir

This will copy the file and rename it with a different file extension

**Move**

In order to **move** a file we do:

	clamscan -r --move=~/home/target_quarantined_dir ~/home/scanned_dir

In this case the extension does not change

**Remove**


	clamscan -r --remove=yes ~/home/target_quarantined_dir ~/home/scanned_dir

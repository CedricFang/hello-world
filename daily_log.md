### 2018-05-03

#### "non-volatile variable storage is about full" Problem

1. Mounting efivarfs:

If `mount | grep '^efivarfs'` doesn't return anything, you can mount efivarfs using this command:

`mount -t efivarfs efivarfs /sys/firmware/efi/efivars`

Or you can just browse /sys/firmware/efi/efivars to see if any variables stand out.

2. Sorting UEFI variables by size:

**efivarfs** doesn't have a concept of disk usage, but it does report each variable by size. This command sorts the variables by size, ascending:

`ls -lh /sys/firmware/efi/efivars | sort -k5 -h`

3. deleting /sys/firmware/efi/efivars/dump-* files/variables if they exist

[ref link](https://superuser.com/questions/1081537/lenovo-thinkpad-t450s-error-the-non-volatile-system-uefi-variable-storage-is?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa)

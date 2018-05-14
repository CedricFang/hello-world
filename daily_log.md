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


### 2018-05-14

#### windows 10 关闭自动更新

可以利用“组策略”关闭，具体方法如下：
win+R，输入gpedit.msc回车，点开“计算机配置\管理模板\Windows组件\Windows更新”，右边有一项“自动配置更新”，点开选禁用。还有，根目录下，点开“用户配置\管理模板\系统”，右边有一项“Windows自动更新”，点开禁用。重启就行了。如果不行或者想改别的设置，就在 “计算机配置\管理模板\Windows组件\Windows更新”下看看再禁用几个别的设置。

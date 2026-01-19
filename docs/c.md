# Disk Sector Editor 
You can use the disk sector editor of your choice, but WinHex is a free download.

1. Open WinHex as administrator. You normally do this by right-clicking.
2. Using WinHex, open the VHD file created previously.
3. If you examine the file, it should be completely empty. Beware, with other virtual disk formats, a blank disk may not be blank, there could be header information in the raw file associated with the VHD format itself.

<figure>
<img src = "https://jor-donegal.github.io/CMC26/images/fig6.avif">
<figcaption>Fig 6. WinHex.</figcaption>
</figure>

4. Close WinHex.
5. Run again __diskpart__ as administrator.
6. Carefully list and select the correct disk.
<figure>
<img src = "https://jor-donegal.github.io/CMC26/images/fig7.avif">
<figcaption>Fig 7. Select disk.</figcaption>
</figure>

7. Check to see what the ID is of your virtual disk, mine is disk 8.
In __diskpart__, type the command 
````
select disk 8
convert mbr
````
which should create an MBR partition table in the first sector. The layout of this will be discussed in lectures. Open WinHex as administrator and this time, open the disk, not the file (F9). Document it.

8. In diskpart, type the command
````
clean
```` 
and re-examine the disk. What happened?

9. In diskpart, type the command
````
convert gpt
```` 
again to create a partition table. Then type the commands 
````
create partition primary
list partition

````
10. Open WinHex as administrator and open the disk, not the file (F9). Where should the new partition start? Is there anything there? Document it.

11. Type the command

```
select partition 1
active
````
to enable it as bootable. Once more, examine with WinHex. Where should the new partition start? Is there anything there?

12. To create a file system, type 

````
format FS=NTFS label=TECHCP901 quick 
````
and when complete, examine with WinHex. Where should the new file system start? Is there anything there?
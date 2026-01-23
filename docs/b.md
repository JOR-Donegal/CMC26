# Diskpart
Create a Windows VM for the next exercises.

One of the most fundamental tools for working with disks is Microsoft’s _diskpart_. Be careful, a mistake here may render your disks unreadable.

1. Open a command prompt as administrator
2. Run diskpart
3. Type ? to get help. Read through the options and understand them.

<figure>
<img src = "https://jor-donegal.github.io/CMC26/images/fig2.avif">
<figcaption>Fig 2. DISKPART.</figcaption>
</figure>

4. If the meaning of any command is unclear, type the command followed by a question mark, to get help.

<figure>
<img src = "https://jor-donegal.github.io/CMC26/images/fig3.avif">
<figcaption>Fig 3. Output of list ?.</figcaption>
</figure>

5. Type the command __list disk__ to identify every disk in the system. Document these disks for your own system before continuing.

<figure>
<img src = "https://jor-donegal.github.io/CMC26/images/fig4.avif">
<figcaption>Fig 4. Output of list disk.</figcaption>
</figure>

## Making virtual disks
6. Look up help for the __create__ command.
7. Create a virtual hard drive on a suitable volume at the command prompt. You can use a USB key as a target disk if you require. My F:\ drive has space free, I used the command

````
create vdisk file=f:\techcp901.vhd maximum=1500
````

to create a 1.5GB disk file. It will take a few minutes.

8. We select the disk by typing the command
````
select vdisk file=f:\techcp901.vhd
````
9. We can now _mount_ this to the system by typing the command
````
attach vdisk
````
10. The command
````
list disk
````
should now show the new volume. In my case, its disk 8.
<figure>
<img src = "https://jor-donegal.github.io/CMC26/images/fig5.avif">
<figcaption>Fig 5. Final list disk.</figcaption>
</figure>

The Asterix on the left shows which disk is selected and active.
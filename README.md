defconfig machine
===============

HOW TO USE:
-----------

### Unpack boot.img
		./mkboot name.img $you_boot_umpack_folders

	EXAMPLE
		./mkboot boot.img boot
		Unpack & decompress boot.img to evert
		  kernel         : $locations
		  ramdisk        : $locations
		  page_size      : 2048
		  base_addr      : 0x00000000
		  kernel size    : 6911360
		  kernel_addr    : 0x00008000
		  ramdisk_size   : 2685222
		  ramdisk_addr   : 0x02000000
		  second_size    : 0
		  second_addr    : 0x00f00000
		  dtb_size       : 1427456
		  tags_addr      : 0x01e00000
		  cmdline        : console=null androidboot.hardware=qcom user_debug=31 maxcpus=2 msm_rtb.filter=0x3F
		Unpack completed.
		
		
### Copy Scripts
   
        copy extra-ikconfig to $you_boot.img_umpack_folders
        
        
### Generate defconfig
        # open terminal on $you_boot_umpack_folders
        # and set permissions
        
		chmod +x extract-ikconfig
		
        #build defconfig
        
        . extract-ikconfig kernel > $device_codename_defconfig 
        
        example :
        
        . extract-ikconfig kernel > evert_defconfig (evert = codename moto g6 plus
        
        
        
        si tus archivos extraidos generan un archivo llamado "zImage" se cambia por la configuracion "kernel" del comando
        . extract-ikconfig zImage > $device_codename_defconfig
       
		
		
		

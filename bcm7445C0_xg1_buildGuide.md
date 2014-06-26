Broadcom bcm7445C0 board build instruction
==========================================

Prerequisites
-------------

###1. download the initial tarball files
We need to SoC-provided initial tarball files. Its size is almost 4.5GB. So we
already discussed how we share the resources. We will use the humax's FTP site.
Please be aware the address of ftp.

ftp address is ftp://

We need to download the 4 files. So please download the bunch of files.
 - 1) comcast_rdk_broadcom_release_rdk2.0_b14.1_20140418_humax.tgz (2.3GB)
 - 2) refsw_release_unified_20140324.src.tgz (344MB)
 - 3) trellis_release_14.1_20140407.src.tgz (1.9GB)
 - 4) trellis_release_14.1_20140407_miracast.tgz (1.4M)
 
###2. make up the files to ready to build
Before starting the build phase, please untar the 1)file to some directory.
(I recommand make sure the 20GB space of HDD free.)

If untar is done, you are able to see the some contents are in directory. 
Sub-Diretories and files. Then you should copy the 2)file and 3)file in sub-
directory named "Broadcom". And copy 4)file in sub-directory named "thirdparty
/Broadcom".


Build Environments
------------------

###3. export the environments variables of shell
In broadcom's guide pdf is Comcast_RDK2.0-B14.1_Broadcom_release_notes_20140418
.pdf. So please refer that guide when you feel need more information about 
building and installation built images. You need to follow the model name 
"bcm97445vms".


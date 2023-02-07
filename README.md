# CUDA_Installation
Steps to Install CUDA

##https://stackoverflow.com/questions/56431461/how-to-remove-cuda-completely-from-ubuntu/56827564#56827564


##To remove cuda toolkit:

sudo rm /etc/apt/sources.list.d/cuda*

sudo apt-get --purge remove "*cublas*" "cuda*" "nsight*"

##To remove Nvidia drivers:
sudo apt-get --purge remove "*nvidia*"

##Issue : nvidia-nvml-driver-library-version-mismatch
##Source (  https://stackoverflow.com/questions/43022843/nvidia-nvml-driver-library-version-mismatch)


lsmod | grep nvidia

sudo rmmod nvidia_drm
sudo rmmod nvidia_modeset
sudo rmmod nvidia_uvm

sudo rmmod nvidia

#confirm you successfully unload those kmods
lsmod | grep nvidia
#you should get nothing, then confirm you can load the correct driver






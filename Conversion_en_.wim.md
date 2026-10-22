# Commande pour convertir un .esd en .wim

## Commandes

Attention il n'y pas de retours à la ligne !!!

1. dism /Get-WimInfo /WimFile:E:/sources/install.esd

2. dism /export-image /SourceImageFile:E:\sources\install.esd /SourceIndex:6 /DestinationImageFile:C:\Users\Administrateur\Downloads\install.wim /Compress:max /CheckIntegrity


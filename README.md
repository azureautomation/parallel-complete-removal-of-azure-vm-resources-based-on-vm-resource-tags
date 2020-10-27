Parallel complete removal of Azure VM resources based on VM resource tags
=========================================================================

            

Licensed under the MIT License.


 


Author:    Waleed Raslan


Created:   10.02.2019


 


CAUTION: This solution automatically removes resources from Azure subscriptions so it is not intended to be used on production subscriptions, it was created to help remove unused VM resources and save on subscription costs.


 


Azure VM Resources Saver removes below VM resources from Azure subscriptions in parallel using Microsoft PowerShell Workflow technology:


1- Any VM not tagged with one of the following tags in 'untagged' removal mode: {Keep, keep, KEEP, do not remove}Or Any VM tagged with one of the following tags in 'tagged' removal mode: {Remove, remove, REMOVE}.


2- Boot diagnostics storage container of the removed VMs


3- All NICs associated with the removed VMs


4- All Public IPs associated with the removed VMs


5- All managed and unmanaged OS disks of the removed VMs with status blobs of the unmanaged OS disks


6- All managed and unmanaged data disks attached to the removed VMs


VM resources preserved:


1- Network Security Group (NSG)


2- Virtual Network (VNET)


3- Resource group


4- Storage accounts of boot diagnostics and unmanaged disks


 

 

        
    
TechNet gallery is retiring! This script was migrated from TechNet script center to GitHub by Microsoft Azure Automation product group. All the Script Center fields like Rating, RatingCount and DownloadCount have been carried over to Github as-is for the migrated scripts only. Note : The Script Center fields will not be applicable for the new repositories created in Github & hence those fields will not show up for new Github repositories.

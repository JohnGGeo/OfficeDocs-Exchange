﻿---
title: 'Schema master is not running Windows Server 2003 Service Pack 1 or later'
TOCTitle: The schema master is not running Windows Server 2003 Service Pack 1 or later_DomainControllerIsOutOfSite
ms:assetid: 5edbe0b8-7610-4a52-aaaa-38c6a99e7e53
ms:mtpsurl: https://technet.microsoft.com/en-us/library/ms.exch.setupreadiness.domaincontrollerisoutofsite(v=EXCHG.150)
ms:contentKeyID: 46628929
ms.date: 12/09/2016
mtps_version: v=EXCHG.150
---

# The schema master is not running Windows Server 2003 Service Pack 1 or later\_DomainControllerIsOutOfSite

 

_**Applies to:** Exchange Server_


The content in this topic hasn't been updated for Microsoft Exchange Server 2013. While it hasn't been updated yet, it may still be applicable to Exchange 2013. If you still need help, check out the community resources below.

Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkid=60612), [Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkid=285351).

Microsoft Exchange Server 2007 setup cannot continue because the domain controller assigned the Active Directory directory service schema master role, also known as flexible single master operations (FSMO), is not running Microsoft Windows Server 2003 Service Pack 1 (SP1) or a later version.

Exchange 2007 setup requires that the domain controller that serves as the schema FSMO run Windows Server 2003 SP1 or a later version.

The FSMO controls all updates and modifications to the Active Directory schema.

To resolve this issue, do one or more of the following:

  - Upgrade the FSMO domain controller to Windows Server 2003 SP1 or a later version and rerun Microsoft Exchange setup.

  - If there is a FSMO domain controller running Microsoft Windows Server 2003 Service Pack 1 (SP1) or a later version in the Exchange organization, run Exchange 2007 setup with the /domaincontroller parameter pointing to that FSMO domain controller:
    
    \[*/DomainController*, or */dc* *\<FQDN of domain controller\>*\]
    
    Use the */DomainController* parameter to specify the domain controller to use to read from and write to Active Directory during setup. You can use NetBIOS or the fully qualified domain name (FQDN) format.

To obtain the latest service pack for Windows Server 2003, see the "Windows Server TechCenter" ([https://go.microsoft.com/fwlink/?LinkId=45315](https://go.microsoft.com/fwlink/?linkid=45315)).

For more information about Exchange Server 2007 Setup parameters, see "How to Install Exchange 2007 in Unattended Mode" ([https://go.microsoft.com/fwlink/?LinkId=86476](https://go.microsoft.com/fwlink/?linkid=86476)) in the Exchange Server 2007 product documentation.


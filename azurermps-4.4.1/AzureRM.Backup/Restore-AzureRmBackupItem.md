---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 856B76FC-88ED-4A29-9DC6-C482398D702E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
ms.openlocfilehash: b449b96417f0ac05fa857a48a10143a285ed888f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528278"
---
# <span data-ttu-id="3647f-101">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="3647f-101">Restore-AzureRmBackupItem</span></span>

## <span data-ttu-id="3647f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3647f-102">SYNOPSIS</span></span>
<span data-ttu-id="3647f-103">Przywraca dane i konfigurację elementu kopii zapasowej do punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="3647f-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3647f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3647f-104">SYNTAX</span></span>

```
Restore-AzureRmBackupItem [-StorageAccountName] <String> [-RecoveryPoint] <AzureRMBackupRecoveryPoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3647f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3647f-105">DESCRIPTION</span></span>
<span data-ttu-id="3647f-106">Polecenie cmdlet **Restore-AzureRmBackupItem** przywraca dane i konfigurację elementu kopii zapasowej platformy Azure do określonego punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="3647f-106">The **Restore-AzureRmBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="3647f-107">To polecenie cmdlet rozpoczyna przywracanie z magazynu kopii zapasowych do konta.</span><span class="sxs-lookup"><span data-stu-id="3647f-107">This cmdlet starts the restore from the Backup vault to your account.</span></span>

<span data-ttu-id="3647f-108">Operacja restore nie powoduje przywrócenia pełnej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3647f-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="3647f-109">Przywraca dane dyskowe i informacje o konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="3647f-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="3647f-110">Po zakończeniu operacji przywracania musisz utworzyć maszynę wirtualną i ją uruchomić.</span><span class="sxs-lookup"><span data-stu-id="3647f-110">After the restore operation finished, you must create the virtual machine and start it.</span></span>

## <span data-ttu-id="3647f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3647f-111">EXAMPLES</span></span>

### <span data-ttu-id="3647f-112">Przykład 1: Przywracanie maszyny wirtualnej do punktu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="3647f-112">Example 1: Restore a virtual machine to a recovery point</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> $RecoveryPoint = Get-AzureRmBackupRecoveryPoint -Item $BackupItem 
PS C:\> Restore-AzureRmBackupItem -StorageAccountName "DestinationAccount" -RecoveryPoint $RecoveryPoint 
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Restore         InProgress      26-Aug-15 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="3647f-113">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="3647f-113">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="3647f-114">Polecenie zapisuje ten obiekt w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="3647f-114">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="3647f-115">Drugie polecenie pobiera kontener o określonej nazwie w magazynie w $Vault przy użyciu polecenia cmdlet **Get-AzureRmBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="3647f-115">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="3647f-116">Polecenie zapisuje ten obiekt w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="3647f-116">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="3647f-117">Trzecie polecenie pobiera element kopii zapasowej w kontenerze w $Container przy użyciu polecenia cmdlet **Get-AzureRmBackupItem** .</span><span class="sxs-lookup"><span data-stu-id="3647f-117">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="3647f-118">Polecenie zapisuje ten obiekt w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="3647f-118">The command stores that object in the $BackupItem variable.</span></span>

<span data-ttu-id="3647f-119">Czwarte polecenie pobiera punkt odzyskiwania dla elementu w $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="3647f-119">The fourth command gets recovery point for the item in $BackupItem.</span></span>
<span data-ttu-id="3647f-120">Polecenie zapisuje ten obiekt w zmiennej $RecoveryPoint.</span><span class="sxs-lookup"><span data-stu-id="3647f-120">The command stores that object in the $RecoveryPoint variable.</span></span>

<span data-ttu-id="3647f-121">Polecenie ostatnie przywraca punkt odzyskiwania $RecoveryPoint konta o nazwie DestinationAccount.</span><span class="sxs-lookup"><span data-stu-id="3647f-121">The final command restores the recovery point in $RecoveryPoint for the account named DestinationAccount.</span></span>

## <span data-ttu-id="3647f-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3647f-122">PARAMETERS</span></span>

### <span data-ttu-id="3647f-123">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="3647f-123">-RecoveryPoint</span></span>
<span data-ttu-id="3647f-124">Określa punkt odzyskiwania, do którego ma zostać przywrócona maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="3647f-124">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="3647f-125">Aby uzyskać **AzureRmBackupRecoveryPoint** , użyj polecenia cmdlet Get-AzureRmBackupRecoveryPoint.</span><span class="sxs-lookup"><span data-stu-id="3647f-125">To obtain an **AzureRmBackupRecoveryPoint** , use the Get-AzureRmBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3647f-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3647f-126">-StorageAccountName</span></span>
<span data-ttu-id="3647f-127">Określa nazwę docelowego konta magazynu w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3647f-127">Specifies the name of the target storage account in your subscription.</span></span>
<span data-ttu-id="3647f-128">W ramach procesu przywracania to polecenie cmdlet przechowuje dyski i informacje o konfiguracji na tym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="3647f-128">As a part of the restore process, this cmdlet stores the disks and the configuration information in this storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3647f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3647f-129">-DefaultProfile</span></span>
<span data-ttu-id="3647f-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3647f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3647f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3647f-131">CommonParameters</span></span>
<span data-ttu-id="3647f-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3647f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3647f-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3647f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3647f-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3647f-134">INPUTS</span></span>

### <span data-ttu-id="3647f-135">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="3647f-135">AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="3647f-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3647f-136">OUTPUTS</span></span>

### <span data-ttu-id="3647f-137">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="3647f-137">AzureRmBackupJob</span></span>

## <span data-ttu-id="3647f-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3647f-138">NOTES</span></span>

## <span data-ttu-id="3647f-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3647f-139">RELATED LINKS</span></span>

[<span data-ttu-id="3647f-140">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="3647f-140">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="3647f-141">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="3647f-141">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="3647f-142">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="3647f-142">Get-AzureRmBackupRecoveryPoint</span></span>](./Get-AzureRmBackupRecoveryPoint.md)



---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 856B76FC-88ED-4A29-9DC6-C482398D702E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/restore-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
ms.openlocfilehash: a203d125e4ff6d811a581b0713ca4a002e098ade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550647"
---
# <span data-ttu-id="f6200-101">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="f6200-101">Restore-AzureRmBackupItem</span></span>

## <span data-ttu-id="f6200-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f6200-102">SYNOPSIS</span></span>
<span data-ttu-id="f6200-103">Przywraca dane i konfigurację elementu kopii zapasowej do punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="f6200-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6200-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f6200-104">SYNTAX</span></span>

```
Restore-AzureRmBackupItem [-StorageAccountName] <String> [-RecoveryPoint] <AzureRMBackupRecoveryPoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6200-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f6200-105">DESCRIPTION</span></span>
<span data-ttu-id="f6200-106">Polecenie cmdlet **Restore-AzureRmBackupItem** przywraca dane i konfigurację elementu kopii zapasowej platformy Azure do określonego punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="f6200-106">The **Restore-AzureRmBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="f6200-107">To polecenie cmdlet rozpoczyna przywracanie z magazynu kopii zapasowych do konta.</span><span class="sxs-lookup"><span data-stu-id="f6200-107">This cmdlet starts the restore from the Backup vault to your account.</span></span>

<span data-ttu-id="f6200-108">Operacja restore nie powoduje przywrócenia pełnej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f6200-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="f6200-109">Przywraca dane dyskowe i informacje o konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="f6200-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="f6200-110">Po zakończeniu operacji przywracania musisz utworzyć maszynę wirtualną i ją uruchomić.</span><span class="sxs-lookup"><span data-stu-id="f6200-110">After the restore operation finished, you must create the virtual machine and start it.</span></span>

## <span data-ttu-id="f6200-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f6200-111">EXAMPLES</span></span>

### <span data-ttu-id="f6200-112">Przykład 1: Przywracanie maszyny wirtualnej do punktu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="f6200-112">Example 1: Restore a virtual machine to a recovery point</span></span>
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

<span data-ttu-id="f6200-113">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="f6200-113">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="f6200-114">Polecenie zapisuje ten obiekt w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="f6200-114">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="f6200-115">Drugie polecenie pobiera kontener o określonej nazwie w magazynie w $Vault przy użyciu polecenia cmdlet **Get-AzureRmBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="f6200-115">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="f6200-116">Polecenie zapisuje ten obiekt w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="f6200-116">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="f6200-117">Trzecie polecenie pobiera element kopii zapasowej w kontenerze w $Container przy użyciu polecenia cmdlet **Get-AzureRmBackupItem** .</span><span class="sxs-lookup"><span data-stu-id="f6200-117">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="f6200-118">Polecenie zapisuje ten obiekt w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="f6200-118">The command stores that object in the $BackupItem variable.</span></span>

<span data-ttu-id="f6200-119">Czwarte polecenie pobiera punkt odzyskiwania dla elementu w $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="f6200-119">The fourth command gets recovery point for the item in $BackupItem.</span></span>
<span data-ttu-id="f6200-120">Polecenie zapisuje ten obiekt w zmiennej $RecoveryPoint.</span><span class="sxs-lookup"><span data-stu-id="f6200-120">The command stores that object in the $RecoveryPoint variable.</span></span>

<span data-ttu-id="f6200-121">Polecenie ostatnie przywraca punkt odzyskiwania $RecoveryPoint konta o nazwie DestinationAccount.</span><span class="sxs-lookup"><span data-stu-id="f6200-121">The final command restores the recovery point in $RecoveryPoint for the account named DestinationAccount.</span></span>

## <span data-ttu-id="f6200-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f6200-122">PARAMETERS</span></span>

### <span data-ttu-id="f6200-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6200-123">-DefaultProfile</span></span>
<span data-ttu-id="f6200-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f6200-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6200-125">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f6200-125">-RecoveryPoint</span></span>
<span data-ttu-id="f6200-126">Określa punkt odzyskiwania, do którego ma zostać przywrócona maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="f6200-126">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="f6200-127">Aby uzyskać **AzureRmBackupRecoveryPoint** , użyj polecenia cmdlet Get-AzureRmBackupRecoveryPoint.</span><span class="sxs-lookup"><span data-stu-id="f6200-127">To obtain an **AzureRmBackupRecoveryPoint** , use the Get-AzureRmBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: AzureRMBackupRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6200-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f6200-128">-StorageAccountName</span></span>
<span data-ttu-id="f6200-129">Określa nazwę docelowego konta magazynu w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f6200-129">Specifies the name of the target storage account in your subscription.</span></span>
<span data-ttu-id="f6200-130">W ramach procesu przywracania to polecenie cmdlet przechowuje dyski i informacje o konfiguracji na tym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="f6200-130">As a part of the restore process, this cmdlet stores the disks and the configuration information in this storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6200-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6200-131">CommonParameters</span></span>
<span data-ttu-id="f6200-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6200-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6200-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6200-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6200-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6200-134">INPUTS</span></span>

### <span data-ttu-id="f6200-135">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f6200-135">AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="f6200-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f6200-136">OUTPUTS</span></span>

### <span data-ttu-id="f6200-137">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="f6200-137">AzureRmBackupJob</span></span>

## <span data-ttu-id="f6200-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f6200-138">NOTES</span></span>

## <span data-ttu-id="f6200-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6200-139">RELATED LINKS</span></span>

[<span data-ttu-id="f6200-140">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="f6200-140">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="f6200-141">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="f6200-141">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="f6200-142">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f6200-142">Get-AzureRmBackupRecoveryPoint</span></span>](./Get-AzureRmBackupRecoveryPoint.md)



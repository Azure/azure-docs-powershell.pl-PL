---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 9e9aab3a71e976d9c41694702dae7a8087da9a36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970378"
---
# <span data-ttu-id="d93a5-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d93a5-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="d93a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d93a5-102">SYNOPSIS</span></span>

<span data-ttu-id="d93a5-103">Pobiera punkty odzyskiwania dla elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="d93a5-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="d93a5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d93a5-104">SYNTAX</span></span>

### <span data-ttu-id="d93a5-105">NoFilterParameterSet (ustawienie domyślne)</span><span class="sxs-lookup"><span data-stu-id="d93a5-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-UseSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d93a5-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="d93a5-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d93a5-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="d93a5-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d93a5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d93a5-108">DESCRIPTION</span></span>

<span data-ttu-id="d93a5-109">Polecenie **cmdlet Get-AzRecoveryServicesBackupRecoveryPoint** pobiera punkty odzyskiwania dla elementu kopii zapasowej kopii zapasowej usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="d93a5-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="d93a5-110">Po zakończeniu kopii zapasowej elementu obiekt **AzureRmRecoveryServicesBackupRecoveryPoint** ma co najmniej jeden punkt odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d93a5-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="d93a5-111">Ustaw kontekst magazynu przy użyciu parametru -VaultId.</span><span class="sxs-lookup"><span data-stu-id="d93a5-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="d93a5-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d93a5-112">EXAMPLES</span></span>

### <span data-ttu-id="d93a5-113">Przykład 1. Uzyskiwanie punktów odzyskiwania dla elementu z ostatniego tygodnia</span><span class="sxs-lookup"><span data-stu-id="d93a5-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="d93a5-114">Pierwsze polecenie pobiera obiekt magazynu na podstawie nazwy magazynu.</span><span class="sxs-lookup"><span data-stu-id="d93a5-114">The first command gets vault object based on vaultName.</span></span> <span data-ttu-id="d93a5-115">Drugie polecenie pobiera datę z siedmiu dni temu, a następnie przechowuje ją w $StartDate zmienną.</span><span class="sxs-lookup"><span data-stu-id="d93a5-115">The second command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="d93a5-116">Trzecie polecenie otrzymuje dzisiejszą datę, a następnie przechowuje je w $EndDate zmienną.</span><span class="sxs-lookup"><span data-stu-id="d93a5-116">The third command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="d93a5-117">Czwarte polecenie pobiera kontenery kopii zapasowej AzureVM i przechowuje je w $Container danych.</span><span class="sxs-lookup"><span data-stu-id="d93a5-117">The fourth command gets AzureVM backup containers, and stores them in the $Container variable.</span></span> <span data-ttu-id="d93a5-118">Piąte polecenie pobiera element kopii zapasowej na podstawie typu workloadType, vaultId, a następnie przechowuje go w $BackupItem danych.</span><span class="sxs-lookup"><span data-stu-id="d93a5-118">The fifth command gets the backup item based on workloadType, vaultId and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="d93a5-119">Ostatnie polecenie pobiera tablicę punktów odzyskiwania dla elementu w programie $BackupItem, a następnie przechowuje je w $RP danych.</span><span class="sxs-lookup"><span data-stu-id="d93a5-119">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="d93a5-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d93a5-120">PARAMETERS</span></span>

### <span data-ttu-id="d93a5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d93a5-121">-DefaultProfile</span></span>

<span data-ttu-id="d93a5-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d93a5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d93a5-123">-EndDate</span><span class="sxs-lookup"><span data-stu-id="d93a5-123">-EndDate</span></span>

<span data-ttu-id="d93a5-124">Określa koniec zakresu dat.</span><span class="sxs-lookup"><span data-stu-id="d93a5-124">Specifies the end of the date range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d93a5-125">— element</span><span class="sxs-lookup"><span data-stu-id="d93a5-125">-Item</span></span>

<span data-ttu-id="d93a5-126">Określa element, dla którego to polecenie cmdlet otrzymuje punkty odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d93a5-126">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="d93a5-127">Aby uzyskać obiekt **AzureRmRecoveryServicesBackupItem,** użyj polecenia cmdlet **Get-AzRecoveryServicesBackupItem.**</span><span class="sxs-lookup"><span data-stu-id="d93a5-127">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d93a5-128">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="d93a5-128">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="d93a5-129">Określa lokalizację pobierania pliku wejściowego w celu przywrócenia klucza KeyVault zaszyfrowanej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d93a5-129">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d93a5-130">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="d93a5-130">-RecoveryPointId</span></span>

<span data-ttu-id="d93a5-131">Określa identyfikator punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d93a5-131">Specifies the recovery point ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d93a5-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="d93a5-132">-StartDate</span></span>

<span data-ttu-id="d93a5-133">Określa początek zakresu dat.</span><span class="sxs-lookup"><span data-stu-id="d93a5-133">Specifies the start of the date range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d93a5-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d93a5-134">-VaultId</span></span>

<span data-ttu-id="d93a5-135">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d93a5-135">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d93a5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d93a5-136">CommonParameters</span></span>
<span data-ttu-id="d93a5-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d93a5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d93a5-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d93a5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d93a5-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d93a5-139">INPUTS</span></span>

### <span data-ttu-id="d93a5-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="d93a5-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="d93a5-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d93a5-141">System.String</span></span>

## <span data-ttu-id="d93a5-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d93a5-142">OUTPUTS</span></span>

### <span data-ttu-id="d93a5-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="d93a5-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="d93a5-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d93a5-144">NOTES</span></span>

## <span data-ttu-id="d93a5-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d93a5-145">RELATED LINKS</span></span>

[<span data-ttu-id="d93a5-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="d93a5-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="d93a5-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d93a5-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

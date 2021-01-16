---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 676ba76cb4412e03c684be4d166e8707c5652b26
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334093"
---
# <span data-ttu-id="b190f-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b190f-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="b190f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b190f-102">SYNOPSIS</span></span>

<span data-ttu-id="b190f-103">Pobiera punkty odzyskiwania dla elementu z kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b190f-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="b190f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b190f-104">SYNTAX</span></span>

### <span data-ttu-id="b190f-105">NoFilterParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b190f-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b190f-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="b190f-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b190f-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="b190f-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b190f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b190f-108">DESCRIPTION</span></span>

<span data-ttu-id="b190f-109">Polecenie cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** pobiera punkty odzyskiwania dla kopii zapasowej elementu kopii zapasowej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b190f-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="b190f-110">Po wykonaniu kopii zapasowej elementu obiekt **AzureRmRecoveryServicesBackupRecoveryPoint** ma co najmniej jeden punkt odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b190f-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="b190f-111">Ustaw kontekst magazynu przy użyciu parametru-VaultId.</span><span class="sxs-lookup"><span data-stu-id="b190f-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="b190f-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b190f-112">EXAMPLES</span></span>

### <span data-ttu-id="b190f-113">Przykład 1: uzyskiwanie punktów odzyskiwania z ostatniego tygodnia dla elementu</span><span class="sxs-lookup"><span data-stu-id="b190f-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="b190f-114">Pierwsze polecenie pobiera obiekt magazynu oparty na magazynie.</span><span class="sxs-lookup"><span data-stu-id="b190f-114">The first command gets vault object based on vaultName.</span></span> <span data-ttu-id="b190f-115">Drugie polecenie pobiera datę z siedmiu dni temu, a następnie zapisuje ją w zmiennej $StartDate.</span><span class="sxs-lookup"><span data-stu-id="b190f-115">The second command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="b190f-116">Trzy polecenia uzyskują dzisiejszą datę, a następnie przechowują je w zmiennej $EndDate.</span><span class="sxs-lookup"><span data-stu-id="b190f-116">The third command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="b190f-117">Czwarte polecenie pobiera kontenery kopii zapasowych AzureVM i przechowuje je w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="b190f-117">The fourth command gets AzureVM backup containers, and stores them in the $Container variable.</span></span> <span data-ttu-id="b190f-118">Piąte polecenie uzyskuje element kopii zapasowej na podstawie elementu obciążeniatype, vaultId, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="b190f-118">The fifth command gets the backup item based on workloadType, vaultId and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="b190f-119">Ostatnie polecenie pobiera tablicę punktów odzyskiwania dla elementu w $BackupItem, a następnie zapisuje je w zmiennej $RP.</span><span class="sxs-lookup"><span data-stu-id="b190f-119">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="b190f-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b190f-120">PARAMETERS</span></span>

### <span data-ttu-id="b190f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b190f-121">-DefaultProfile</span></span>

<span data-ttu-id="b190f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b190f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b190f-123">-EndDate</span><span class="sxs-lookup"><span data-stu-id="b190f-123">-EndDate</span></span>

<span data-ttu-id="b190f-124">Określa koniec zakresu dat.</span><span class="sxs-lookup"><span data-stu-id="b190f-124">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="b190f-125">-Item</span><span class="sxs-lookup"><span data-stu-id="b190f-125">-Item</span></span>

<span data-ttu-id="b190f-126">Określa element, dla którego to polecenie cmdlet umożliwia pobieranie punktów odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b190f-126">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="b190f-127">Aby uzyskać obiekt **AzureRmRecoveryServicesBackupItem** , użyj polecenia cmdlet **Get-AzRecoveryServicesBackupItem** .</span><span class="sxs-lookup"><span data-stu-id="b190f-127">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

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

### <span data-ttu-id="b190f-128">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="b190f-128">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="b190f-129">Określa lokalizację, w której ma zostać pobrany plik wejściowy, w celu przywrócenia klucza magazynu kluczy dla zaszyfrowanej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b190f-129">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="b190f-130">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="b190f-130">-RecoveryPointId</span></span>

<span data-ttu-id="b190f-131">Określa identyfikator punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b190f-131">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="b190f-132">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="b190f-132">-StartDate</span></span>

<span data-ttu-id="b190f-133">Określa początek zakresu dat.</span><span class="sxs-lookup"><span data-stu-id="b190f-133">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="b190f-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b190f-134">-VaultId</span></span>

<span data-ttu-id="b190f-135">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="b190f-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b190f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b190f-136">CommonParameters</span></span>
<span data-ttu-id="b190f-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b190f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b190f-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b190f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b190f-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b190f-139">INPUTS</span></span>

### <span data-ttu-id="b190f-140">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="b190f-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="b190f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b190f-141">System.String</span></span>

## <span data-ttu-id="b190f-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b190f-142">OUTPUTS</span></span>

### <span data-ttu-id="b190f-143">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="b190f-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="b190f-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b190f-144">NOTES</span></span>

## <span data-ttu-id="b190f-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b190f-145">RELATED LINKS</span></span>

[<span data-ttu-id="b190f-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b190f-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="b190f-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b190f-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

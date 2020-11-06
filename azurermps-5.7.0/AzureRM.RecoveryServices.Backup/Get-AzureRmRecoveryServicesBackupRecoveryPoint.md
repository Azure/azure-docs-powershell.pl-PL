---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 8223172994eb4fdbea3c887f788c4b0e445e0202
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526698"
---
# <span data-ttu-id="4321d-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="4321d-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="4321d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4321d-102">SYNOPSIS</span></span>
<span data-ttu-id="4321d-103">Pobiera punkty odzyskiwania dla elementu z kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="4321d-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4321d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4321d-104">SYNTAX</span></span>

### <span data-ttu-id="4321d-105">NoFilterParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4321d-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4321d-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="4321d-106">DateTimeFilter</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4321d-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="4321d-107">RecoveryPointId</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4321d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4321d-108">DESCRIPTION</span></span>
<span data-ttu-id="4321d-109">Polecenie cmdlet **Get-AzureRmRecoveryServicesBackupRecoveryPoint** pobiera punkty odzyskiwania dla kopii zapasowej elementu kopii zapasowej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4321d-109">The **Get-AzureRmRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="4321d-110">Po wykonaniu kopii zapasowej elementu obiekt **AzureRmRecoveryServicesBackupRecoveryPoint** ma co najmniej jeden punkt odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="4321d-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>

<span data-ttu-id="4321d-111">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="4321d-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="4321d-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4321d-112">EXAMPLES</span></span>

### <span data-ttu-id="4321d-113">Przykład 1: uzyskiwanie punktów odzyskiwania z ostatniego tygodnia dla elementu</span><span class="sxs-lookup"><span data-stu-id="4321d-113">Example 1: Get recovery points from the last week for an item</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="4321d-114">Pierwsze polecenie pobiera datę z siedmiu dni temu, a następnie zapisuje ją w zmiennej $StartDate.</span><span class="sxs-lookup"><span data-stu-id="4321d-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>

<span data-ttu-id="4321d-115">Drugie polecenie pobiera dzisiejszą datę, a następnie zapisuje je w zmiennej $EndDate.</span><span class="sxs-lookup"><span data-stu-id="4321d-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>

<span data-ttu-id="4321d-116">Trzecie polecenie pobiera kontenery kopii zapasowych AzureVM i przechowuje je w zmiennej $Containers.</span><span class="sxs-lookup"><span data-stu-id="4321d-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>

<span data-ttu-id="4321d-117">Czwarte polecenie uzyskuje element kopii zapasowej o nazwie V2VM, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="4321d-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>

<span data-ttu-id="4321d-118">Ostatnie polecenie pobiera tablicę punktów odzyskiwania dla elementu w $BackupItem, a następnie zapisuje je w zmiennej $RP.</span><span class="sxs-lookup"><span data-stu-id="4321d-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="4321d-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4321d-119">PARAMETERS</span></span>

### <span data-ttu-id="4321d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4321d-120">-DefaultProfile</span></span>
<span data-ttu-id="4321d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4321d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4321d-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="4321d-122">-EndDate</span></span>
<span data-ttu-id="4321d-123">Określa koniec zakresu dat.</span><span class="sxs-lookup"><span data-stu-id="4321d-123">Specifies the end of the date range.</span></span>

```yaml
Type: DateTime
Parameter Sets: DateTimeFilter
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4321d-124">-Item</span><span class="sxs-lookup"><span data-stu-id="4321d-124">-Item</span></span>
<span data-ttu-id="4321d-125">Określa element, dla którego to polecenie cmdlet umożliwia pobieranie punktów odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="4321d-125">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="4321d-126">Aby uzyskać obiekt **AzureRmRecoveryServicesBackupItem** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="4321d-126">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: ItemBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4321d-127">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="4321d-127">-KeyFileDownloadLocation</span></span>
<span data-ttu-id="4321d-128">Określa lokalizację, w której ma zostać pobrany plik wejściowy, w celu przywrócenia klucza magazynu kluczy dla zaszyfrowanej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4321d-128">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: RecoveryPointId
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4321d-129">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="4321d-129">-RecoveryPointId</span></span>
<span data-ttu-id="4321d-130">Określa identyfikator punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="4321d-130">Specifies the recovery point ID.</span></span>

```yaml
Type: String
Parameter Sets: RecoveryPointId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4321d-131">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="4321d-131">-StartDate</span></span>
<span data-ttu-id="4321d-132">Określa początek zakresu dat.</span><span class="sxs-lookup"><span data-stu-id="4321d-132">Specifies the start of the date range.</span></span>

```yaml
Type: DateTime
Parameter Sets: DateTimeFilter
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4321d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4321d-133">CommonParameters</span></span>
<span data-ttu-id="4321d-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4321d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4321d-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4321d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4321d-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4321d-136">INPUTS</span></span>

### <span data-ttu-id="4321d-137">ItemBase</span><span class="sxs-lookup"><span data-stu-id="4321d-137">ItemBase</span></span>
<span data-ttu-id="4321d-138">Parametr "element" akceptuje wartość typu "ItemBase" z potoku</span><span class="sxs-lookup"><span data-stu-id="4321d-138">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="4321d-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4321d-139">OUTPUTS</span></span>

### <span data-ttu-id="4321d-140">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="4321d-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="4321d-141">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. modele. RecoveryPointBase]</span><span class="sxs-lookup"><span data-stu-id="4321d-141">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase]</span></span>

## <span data-ttu-id="4321d-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4321d-142">NOTES</span></span>

## <span data-ttu-id="4321d-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4321d-143">RELATED LINKS</span></span>

[<span data-ttu-id="4321d-144">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="4321d-144">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="4321d-145">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4321d-145">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)



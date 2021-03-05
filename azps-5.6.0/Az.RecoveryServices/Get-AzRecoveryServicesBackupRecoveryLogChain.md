---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: c0080985637e58232e2f7eea37344ab291d5d594
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978218"
---
# <span data-ttu-id="fed60-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="fed60-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="fed60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fed60-102">SYNOPSIS</span></span>
<span data-ttu-id="fed60-103">To polecenie zawiera listę punktów startowych i końcowych nieprzerwanego łańcucha dziennika danego elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="fed60-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="fed60-104">Za jego pomocą można określić, czy punkt w czasie, do którego użytkownik chce przywrócić baza danych, jest prawidłowy, czy nie.</span><span class="sxs-lookup"><span data-stu-id="fed60-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="fed60-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fed60-105">SYNTAX</span></span>

### <span data-ttu-id="fed60-106">NoFilterParameterSet (ustawienie domyślne)</span><span class="sxs-lookup"><span data-stu-id="fed60-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fed60-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="fed60-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fed60-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="fed60-108">DESCRIPTION</span></span>
<span data-ttu-id="fed60-109">Polecenie **cmdlet Get-AzRecoveryServicesBackupRecoveryLogChain** pobiera punkty odzyskiwania zakresu czasu w czasie dla kopii zapasowej elementu kopii zapasowej usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="fed60-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="fed60-110">Po zakończeniu kopii zapasowej elementu obiekt **AzRecoveryServicesBackupRecoveryLogChain** ma co najmniej jeden zakres czasu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="fed60-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="fed60-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fed60-111">EXAMPLES</span></span>

### <span data-ttu-id="fed60-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fed60-112">Example 1</span></span>
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="fed60-113">Pierwsze polecenie pobiera datę z siedmiu dni temu, a następnie przechowuje ją w $StartDate zmienną.</span><span class="sxs-lookup"><span data-stu-id="fed60-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="fed60-114">Drugie polecenie otrzymuje dzisiejszą datę, a następnie przechowuje je w $EndDate zmienną.</span><span class="sxs-lookup"><span data-stu-id="fed60-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="fed60-115">Trzecie polecenie pobiera kontenery kopii zapasowej azureWorkload i przechowuje je w $Container danych.</span><span class="sxs-lookup"><span data-stu-id="fed60-115">The third command gets AzureWorkload backup containers, and stores them in the $Container variable.</span></span>
<span data-ttu-id="fed60-116">Czwarte polecenie pobiera element kopii zapasowej, a następnie udostępnia go w potokowym poleceniu cmdlet jako obiekt elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="fed60-116">The fourth command gets the backup item, and then shares it across the piped cmdlet as backup item object.</span></span>
<span data-ttu-id="fed60-117">Ostatnie polecenie pobiera tablicę zakresów czasu punktów odzyskiwania dla elementu w programie $BackupItem, a następnie przechowuje je w $RP zmienną.</span><span class="sxs-lookup"><span data-stu-id="fed60-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

### <span data-ttu-id="fed60-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fed60-118">Example 2</span></span>

<span data-ttu-id="fed60-119">To polecenie zawiera listę punktów startowych i końcowych nieprzerwanego łańcucha dziennika danego elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="fed60-119">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="fed60-120">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="fed60-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="fed60-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fed60-121">PARAMETERS</span></span>

### <span data-ttu-id="fed60-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fed60-122">-DefaultProfile</span></span>
<span data-ttu-id="fed60-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fed60-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fed60-124">-EndDate</span><span class="sxs-lookup"><span data-stu-id="fed60-124">-EndDate</span></span>
<span data-ttu-id="fed60-125">Czas zakończenia zakresu czasu, dla którego należy pobrać punkt odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="fed60-125">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="fed60-126">— element</span><span class="sxs-lookup"><span data-stu-id="fed60-126">-Item</span></span>
<span data-ttu-id="fed60-127">Obiekt Elementu chronionego, dla którego należy pobrać punkt odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="fed60-127">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="fed60-128">-StartDate</span><span class="sxs-lookup"><span data-stu-id="fed60-128">-StartDate</span></span>
<span data-ttu-id="fed60-129">Godzina rozpoczęcia zakresu czasu, dla którego należy pobrać punkt odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="fed60-129">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="fed60-130">-VaultId</span><span class="sxs-lookup"><span data-stu-id="fed60-130">-VaultId</span></span>
<span data-ttu-id="fed60-131">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="fed60-131">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="fed60-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fed60-132">CommonParameters</span></span>
<span data-ttu-id="fed60-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fed60-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fed60-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fed60-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fed60-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fed60-135">INPUTS</span></span>

### <span data-ttu-id="fed60-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="fed60-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="fed60-137">System.String</span><span class="sxs-lookup"><span data-stu-id="fed60-137">System.String</span></span>

## <span data-ttu-id="fed60-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fed60-138">OUTPUTS</span></span>

### <span data-ttu-id="fed60-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="fed60-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="fed60-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fed60-140">NOTES</span></span>

## <span data-ttu-id="fed60-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fed60-141">RELATED LINKS</span></span>

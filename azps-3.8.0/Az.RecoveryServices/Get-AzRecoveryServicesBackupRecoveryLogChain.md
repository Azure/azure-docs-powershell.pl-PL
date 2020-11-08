---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: 8a0fbc09f9c46bea6ac09d75911ac83b68f0e296
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053699"
---
# <span data-ttu-id="2d59f-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="2d59f-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="2d59f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2d59f-102">SYNOPSIS</span></span>
<span data-ttu-id="2d59f-103">To polecenie zawiera listę punktów początkowych i końcowych nieprzerwanego łańcucha dziennika danego elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="2d59f-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="2d59f-104">Użyj go do określenia, czy punkt w czasie, do którego użytkownik chce przywrócić bazę danych, jest prawidłowy.</span><span class="sxs-lookup"><span data-stu-id="2d59f-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="2d59f-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2d59f-105">SYNTAX</span></span>

### <span data-ttu-id="2d59f-106">NoFilterParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2d59f-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d59f-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="2d59f-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d59f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2d59f-108">DESCRIPTION</span></span>
<span data-ttu-id="2d59f-109">Polecenie cmdlet **Get-AzRecoveryServicesBackupRecoveryLogChain** pobiera punkty odzyskiwania przedziału czasu w czasie dla kopii zapasowej elementu kopii zapasowej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2d59f-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="2d59f-110">Po wykonaniu kopii zapasowej elementu obiekt **AzRecoveryServicesBackupRecoveryLogChain** ma co najmniej jeden zakres czasu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="2d59f-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="2d59f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2d59f-111">EXAMPLES</span></span>

### <span data-ttu-id="2d59f-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2d59f-112">Example 1</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="2d59f-113">Pierwsze polecenie pobiera datę z siedmiu dni temu, a następnie zapisuje ją w zmiennej $StartDate.</span><span class="sxs-lookup"><span data-stu-id="2d59f-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="2d59f-114">Drugie polecenie pobiera dzisiejszą datę, a następnie zapisuje je w zmiennej $EndDate.</span><span class="sxs-lookup"><span data-stu-id="2d59f-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="2d59f-115">Trzecie polecenie pobiera kontenery kopii zapasowych AzureWorkload i przechowuje je w zmiennej $Containers.</span><span class="sxs-lookup"><span data-stu-id="2d59f-115">The third command gets AzureWorkload backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="2d59f-116">Czwarte polecenie pobiera element kopii zapasowej, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="2d59f-116">The fourth command gets the backup item, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="2d59f-117">Ostatnie polecenie pobiera tablicę zakresów czasu odzyskiwania dla elementu w $BackupItem, a następnie zapisuje je w zmiennej $RP.</span><span class="sxs-lookup"><span data-stu-id="2d59f-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="2d59f-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2d59f-118">PARAMETERS</span></span>

### <span data-ttu-id="2d59f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d59f-119">-DefaultProfile</span></span>
<span data-ttu-id="2d59f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d59f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d59f-121">-EndDate</span><span class="sxs-lookup"><span data-stu-id="2d59f-121">-EndDate</span></span>
<span data-ttu-id="2d59f-122">Godzina zakończenia zakresu czasu, dla którego należy pobrać punkt odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="2d59f-122">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="2d59f-123">-Item</span><span class="sxs-lookup"><span data-stu-id="2d59f-123">-Item</span></span>
<span data-ttu-id="2d59f-124">Obiekt chronionego elementu, dla którego należy pobrać punkt odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="2d59f-124">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="2d59f-125">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="2d59f-125">-StartDate</span></span>
<span data-ttu-id="2d59f-126">Czas rozpoczęcia zakresu czasu, dla którego należy pobrać punkt odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="2d59f-126">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="2d59f-127">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2d59f-127">-VaultId</span></span>
<span data-ttu-id="2d59f-128">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="2d59f-128">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2d59f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d59f-129">CommonParameters</span></span>
<span data-ttu-id="2d59f-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d59f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d59f-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d59f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d59f-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d59f-132">INPUTS</span></span>

### <span data-ttu-id="2d59f-133">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="2d59f-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="2d59f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2d59f-134">System.String</span></span>

## <span data-ttu-id="2d59f-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2d59f-135">OUTPUTS</span></span>

### <span data-ttu-id="2d59f-136">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="2d59f-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="2d59f-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2d59f-137">NOTES</span></span>

## <span data-ttu-id="2d59f-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d59f-138">RELATED LINKS</span></span>

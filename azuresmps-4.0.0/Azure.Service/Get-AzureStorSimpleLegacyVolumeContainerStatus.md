---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A736738A-C6B3-4E5A-B9BA-D6559A27A667
online version: ''
schema: 2.0.0
ms.openlocfilehash: a95e604c6c3f6766ccfc89bd9018dbe2241fb5b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055516"
---
# <span data-ttu-id="d6325-101">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="d6325-101">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>

## <span data-ttu-id="d6325-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d6325-102">SYNOPSIS</span></span>
<span data-ttu-id="d6325-103">Pobiera stan migracji kontenerów woluminów.</span><span class="sxs-lookup"><span data-stu-id="d6325-103">Gets the migration status of the volume containers.</span></span>

## <span data-ttu-id="d6325-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d6325-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> [-LegacyContainerNames <String[]>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d6325-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d6325-105">DESCRIPTION</span></span>
<span data-ttu-id="d6325-106">Polecenie cmdlet **Get-AzureStorSimpleLegacyVolumeContainerStatus** Pobiera stan migracji kontenerów woluminów.</span><span class="sxs-lookup"><span data-stu-id="d6325-106">The **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet gets the migration status of the volume containers.</span></span>
<span data-ttu-id="d6325-107">To polecenie cmdlet zwraca informacje o stanie, które zawiera informację, czy migracja kontenera woluminu jest wciąż w toku, czy zakończona, czy nie.</span><span class="sxs-lookup"><span data-stu-id="d6325-107">This cmdlet returns status information which includes whether the volume container migration is still in progress, completed, or failed.</span></span>

## <span data-ttu-id="d6325-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d6325-108">EXAMPLES</span></span>

### <span data-ttu-id="d6325-109">Przykład 1: uzyskiwanie stanu nieudanej migracji</span><span class="sxs-lookup"><span data-stu-id="d6325-109">Example 1: Get status for a failed migration</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4" -LegacyContainerNames "OneSDKAzureCloud"
ConfigId             : dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4
MigrationCompleted   : No Cloud Configuration(s) are found to be in Completed state of Migration
MigrationInprogress  : No Cloud Configuration(s)  are found to be in InProgress state of Migration
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : Cloud Configuration Name: OneSDKAzureCloud
                       PercentageCompleted : 0
                       MigrationStatus : Failed
                       No Backup sets found
```

<span data-ttu-id="d6325-110">To polecenie uzyskuje stan migracji dla nazwanego starszego kontenera.</span><span class="sxs-lookup"><span data-stu-id="d6325-110">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="d6325-111">Wyniki pokazują, że migracja nie powiodła się.</span><span class="sxs-lookup"><span data-stu-id="d6325-111">The results show that the migration failed.</span></span>

### <span data-ttu-id="d6325-112">Przykład 2: uzyskiwanie stanu trwającej migracji</span><span class="sxs-lookup"><span data-stu-id="d6325-112">Example 2: Get status for a migration in progress</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4" -LegacyContainerNames "OneSDKAzureCloud"
ConfigId             : 5a83ec88-9e0a-4722-9fb0-9131caa7387a
MigrationCompleted   : No Cloud Configuration(s) are found to be in Completed state of Migration
MigrationInprogress  : CloudConfigurationName: OneSDKAzureCloud
                       PercentageCompleted : 10
                       MigrationStatus : InProgress
                       BackupSets : 
                           Policy : OneSDKBackupPolicy, Status : InProgress
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : No Cloud Configuration(s) are found to be in Failed state of Migration
```

<span data-ttu-id="d6325-113">To polecenie uzyskuje stan migracji dla nazwanego starszego kontenera.</span><span class="sxs-lookup"><span data-stu-id="d6325-113">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="d6325-114">Wyniki pokazują, że migracja jest w toku.</span><span class="sxs-lookup"><span data-stu-id="d6325-114">The results show that the migration is in progress.</span></span>

### <span data-ttu-id="d6325-115">Przykład 3: uzyskiwanie stanu ukończonej migracji</span><span class="sxs-lookup"><span data-stu-id="d6325-115">Example 3: Get status for a completed migration</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4 -LegacyContainerNames OneSDKAzureCloud
ConfigId             : 5a83ec88-9e0a-4722-9fb0-9131caa7387a
MigrationCompleted   : Cloud ConfigurationName: OneSDKAzureCloud
                       PercentageCompleted : 100
                       MigrationStatus : Completed
                       BackupSets : 
                          Policy : vg1p1, Created On : 04/06/2015 11:22:00, Status : Completed
                          Policy : vg1p1, Created On : 03/30/2015 11:22:00, Status : Completed
                          Policy : c1v1-Auto-Daily-CloudSnapshot, Created On : 03/30/2015 03:30:00, Status : Completed
MigrationInprogress  : No Cloud Configuration(s) are found to be in InProgress state of Migration
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : No Cloud Configuration(s) are found to be in Failed state of Migration
```

<span data-ttu-id="d6325-116">To polecenie uzyskuje stan migracji dla nazwanego starszego kontenera.</span><span class="sxs-lookup"><span data-stu-id="d6325-116">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="d6325-117">Wyniki zostaną wyświetlone po zakończeniu migracji.</span><span class="sxs-lookup"><span data-stu-id="d6325-117">The results show that the migration is completed.</span></span>

## <span data-ttu-id="d6325-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d6325-118">PARAMETERS</span></span>

### <span data-ttu-id="d6325-119">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="d6325-119">-LegacyConfigId</span></span>
<span data-ttu-id="d6325-120">Określa unikatowy identyfikator starszego urządzenia.</span><span class="sxs-lookup"><span data-stu-id="d6325-120">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6325-121">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="d6325-121">-LegacyContainerNames</span></span>
<span data-ttu-id="d6325-122">Określa tablicę nazw kontenerów woluminów, dla których obowiązuje plan migracji.</span><span class="sxs-lookup"><span data-stu-id="d6325-122">Specifies an array of volume container names for which the migration plan applies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6325-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="d6325-123">-Profile</span></span>
<span data-ttu-id="d6325-124">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d6325-124">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6325-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6325-125">CommonParameters</span></span>
<span data-ttu-id="d6325-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6325-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6325-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6325-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6325-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6325-128">INPUTS</span></span>

## <span data-ttu-id="d6325-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d6325-129">OUTPUTS</span></span>

## <span data-ttu-id="d6325-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d6325-130">NOTES</span></span>

## <span data-ttu-id="d6325-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6325-131">RELATED LINKS</span></span>

[<span data-ttu-id="d6325-132">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="d6325-132">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Confirm-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="d6325-133">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="d6325-133">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)



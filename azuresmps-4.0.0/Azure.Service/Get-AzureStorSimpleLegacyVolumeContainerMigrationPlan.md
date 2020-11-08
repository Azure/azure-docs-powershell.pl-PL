---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E4F6D096-E265-49CF-AA73-E9C807F8383B
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0207d4b7eddfe56a8e4e86aac6899d19c10f44e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054522"
---
# <span data-ttu-id="969c7-101">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="969c7-101">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>

## <span data-ttu-id="969c7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="969c7-102">SYNOPSIS</span></span>
<span data-ttu-id="969c7-103">Pobiera plany migracji starszych kontenerów.</span><span class="sxs-lookup"><span data-stu-id="969c7-103">Gets migration plans for legacy containers.</span></span>

## <span data-ttu-id="969c7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="969c7-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan [-LegacyConfigId <String>]
 [-LegacyContainerNames <String[]>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="969c7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="969c7-105">DESCRIPTION</span></span>
<span data-ttu-id="969c7-106">Polecenie cmdlet **Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** pobiera plany migracji starszych kontenerów.</span><span class="sxs-lookup"><span data-stu-id="969c7-106">The **Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** cmdlet gets migration plans for legacy containers.</span></span>
<span data-ttu-id="969c7-107">Określ plan migracji przy użyciu identyfikatora konfiguracji starszego typu.</span><span class="sxs-lookup"><span data-stu-id="969c7-107">Specify a migration plan by its legacy configuration ID.</span></span>
<span data-ttu-id="969c7-108">Jeśli utworzenie planu migracji jest wciąż w toku, to polecenie cmdlet spowoduje wyświetlenie stanu planu migracji.</span><span class="sxs-lookup"><span data-stu-id="969c7-108">If creation of the migration plan is still in progress, this cmdlet gets the status of the migration plan.</span></span>
<span data-ttu-id="969c7-109">Jeśli plan migracji zostanie ukończony, to polecenie cmdlet zwróci rzeczywisty plan migracji dla zestawu starszych kontenerów.</span><span class="sxs-lookup"><span data-stu-id="969c7-109">If the migration plan is completed, this cmdlet returns the actual migration plan for the set of legacy containers.</span></span>
<span data-ttu-id="969c7-110">Jeśli nie określisz parametru *LegacyConfigId* , to polecenie cmdlet zwróci listę identyfikatorów konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="969c7-110">If you do not specify the *LegacyConfigId* parameter, this cmdlet returns a list of configuration IDs.</span></span>

## <span data-ttu-id="969c7-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="969c7-111">EXAMPLES</span></span>

### <span data-ttu-id="969c7-112">Przykład 1: uzyskiwanie stanu planu</span><span class="sxs-lookup"><span data-stu-id="969c7-112">Example 1: Get the status of a plan</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 51e413fd-c2c9-4108-88cd-a0e792eab80a_PS
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 4c6398ef-35a0-4d1c-931e-d9d45599a97a_PS
VERBOSE: 2015-04-08 13:48:17 ClientRequestId: ef7a7e35-6dff-46cd-9df3-cb5fa25d149e_PS
VERBOSE: Request Id : fd7e502f273885468f633a44567bcb3f, HttpResponse OK
VERBOSE: List of volume containers: 


LegacyConfigId                    : f16463bd-94a9-4c3c-91c2-7a3ba7120087
DeviceName                        : ARUNKM-N4
MigrationTimeEstimationCompleted  : CloudConfigurationName        : OneSDKAzureCloud
                                    EstimatedTimeForLatestBackup  : 15Minutes
                                    EstimatedTimeForAllBackups    : 15Minutes
                                    These estimates are assuming 20 MBps bandwidth. Refer to migration guide to re-calculate for lower bandwidths. 



MigrationTimeEstimationInProgress : None
MigrationTimeEstimationFailed     : None
MigrationTimeEstimationNotStarted : None
```

<span data-ttu-id="969c7-113">To polecenie uzyskuje stan planu migracji.</span><span class="sxs-lookup"><span data-stu-id="969c7-113">This command gets the status of the migration plan.</span></span>
<span data-ttu-id="969c7-114">Stan obejmuje przypuszczalną przepustowość, szacunkowy czas i powiązane informacje.</span><span class="sxs-lookup"><span data-stu-id="969c7-114">The status includes assumed bandwidth, estimated time and, related information.</span></span>

### <span data-ttu-id="969c7-115">Przykład 2: uzyskiwanie identyfikatorów istniejących planów</span><span class="sxs-lookup"><span data-stu-id="969c7-115">Example 2: Get the IDs of existing plans</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 813da56c-0cfc-4325-80db-08ef32bdde1e_PS
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 9e7cf244-1894-490a-be02-749834a99318_PS
VERBOSE: List of LegacyConfig Ids on the resource: 

LegacyConfigId                                              DeviceName
--------------                                              ----------
1e1f10a0-3dff-4249-b847-4930061cd87a                        ARUNKM-N4
26d4096d-49b6-4102-b188-0446ece73c8b                        ARUNKM-N4
```

<span data-ttu-id="969c7-116">To polecenie pobiera wszystkie identyfikatory konfiguracji planów migracji.</span><span class="sxs-lookup"><span data-stu-id="969c7-116">This command gets all the configuration IDs of migration plans.</span></span>

## <span data-ttu-id="969c7-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="969c7-117">PARAMETERS</span></span>

### <span data-ttu-id="969c7-118">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="969c7-118">-LegacyConfigId</span></span>
<span data-ttu-id="969c7-119">Określa unikatowy identyfikator starszego urządzenia.</span><span class="sxs-lookup"><span data-stu-id="969c7-119">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969c7-120">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="969c7-120">-LegacyContainerNames</span></span>
<span data-ttu-id="969c7-121">Określa tablicę nazw kontenerów woluminów, dla których to polecenie cmdlet pobiera plan migracji.</span><span class="sxs-lookup"><span data-stu-id="969c7-121">Specifies an array of volume container names for which this cmdlet gets a migration plan.</span></span>

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

### <span data-ttu-id="969c7-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="969c7-122">-Profile</span></span>
<span data-ttu-id="969c7-123">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="969c7-123">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="969c7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="969c7-124">CommonParameters</span></span>
<span data-ttu-id="969c7-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="969c7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="969c7-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="969c7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="969c7-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="969c7-127">INPUTS</span></span>

### <span data-ttu-id="969c7-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="969c7-128">None</span></span>

## <span data-ttu-id="969c7-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="969c7-129">OUTPUTS</span></span>

### <span data-ttu-id="969c7-130">MigrationPlanMsg</span><span class="sxs-lookup"><span data-stu-id="969c7-130">MigrationPlanMsg</span></span>
<span data-ttu-id="969c7-131">To polecenie cmdlet zwraca obiekt **MigrationPlanMsg** , który zawiera stan zadania planu migracji, przyjmowanej przepustowości w megabitach na sekundę i oszacowany czas w minutach.</span><span class="sxs-lookup"><span data-stu-id="969c7-131">This cmdlet returns a **MigrationPlanMsg** object that contains the status of the migration plan job, assumed bandwidth in megabits per second, and estimated time in minutes.</span></span>

## <span data-ttu-id="969c7-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="969c7-132">NOTES</span></span>

## <span data-ttu-id="969c7-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="969c7-133">RELATED LINKS</span></span>

[<span data-ttu-id="969c7-134">Start — AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="969c7-134">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)



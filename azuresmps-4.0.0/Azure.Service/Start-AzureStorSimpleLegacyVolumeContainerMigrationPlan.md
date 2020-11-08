---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 6F31F2B4-6131-4B11-B074-CA05CE3A56F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: f928ecba8f92badc1eb87e47aee16515f1684fce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054739"
---
# <span data-ttu-id="77d79-101">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="77d79-101">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>

## <span data-ttu-id="77d79-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77d79-102">SYNOPSIS</span></span>
<span data-ttu-id="77d79-103">Rozpoczynanie tworzenia planu migracji.</span><span class="sxs-lookup"><span data-stu-id="77d79-103">Starts the creation of a migration plan.</span></span>

## <span data-ttu-id="77d79-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77d79-104">SYNTAX</span></span>

### <span data-ttu-id="77d79-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="77d79-105">MigrateSpecificContainer</span></span>
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="77d79-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="77d79-106">MigrateAllContainer</span></span>
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="77d79-107">Opis</span><span class="sxs-lookup"><span data-stu-id="77d79-107">DESCRIPTION</span></span>
<span data-ttu-id="77d79-108">Polecenie cmdlet **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** rozpoczyna Tworzenie planu migracji.</span><span class="sxs-lookup"><span data-stu-id="77d79-108">The **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet starts the creation of a migration plan.</span></span>
<span data-ttu-id="77d79-109">Tworzenie planu migracji jest asynchroniczne.</span><span class="sxs-lookup"><span data-stu-id="77d79-109">The creation of a migration plan is asynchronous.</span></span>
<span data-ttu-id="77d79-110">Aby sprawdzić stan planu migracji, użyj polecenia cmdlet **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** .</span><span class="sxs-lookup"><span data-stu-id="77d79-110">To see the status of the migration plan, use the **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet.</span></span>

## <span data-ttu-id="77d79-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77d79-111">EXAMPLES</span></span>

### <span data-ttu-id="77d79-112">Przykład 1. Rozpocznij plan migracji</span><span class="sxs-lookup"><span data-stu-id="77d79-112">Example 1: Start a migration plan</span></span>
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

<span data-ttu-id="77d79-113">To polecenie rozpoczyna Tworzenie planu migracji dla starszego kontenera o nazwie OneSDKAzureCloud.</span><span class="sxs-lookup"><span data-stu-id="77d79-113">This command starts creation of a migration plan for the legacy container named OneSDKAzureCloud.</span></span>
<span data-ttu-id="77d79-114">Polecenie zwraca wiadomość o stanie planu i używa polecenia cmdlet **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** w celu uzyskania aktualnych informacji.</span><span class="sxs-lookup"><span data-stu-id="77d79-114">The command returns a message about the status of the plan, and to use the **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet for up to date information.</span></span>

### <span data-ttu-id="77d79-115">Przykład 2: Rozpoczynanie planu migracji dla wszystkich kontenerów woluminów</span><span class="sxs-lookup"><span data-stu-id="77d79-115">Example 2: Start migration plan for all volume containers</span></span>
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

<span data-ttu-id="77d79-116">To polecenie rozpoczyna Tworzenie planu migracji dla wszystkich starszych kontenerów woluminów w importowanym pliku konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="77d79-116">This command starts creation of migration plan for all legacy volume containers in the configuration file that is imported.</span></span>

## <span data-ttu-id="77d79-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77d79-117">PARAMETERS</span></span>

### <span data-ttu-id="77d79-118">-All</span><span class="sxs-lookup"><span data-stu-id="77d79-118">-All</span></span>
<span data-ttu-id="77d79-119">Wskazuje, że to polecenie cmdlet rozpoczyna Szacowanie czasu migracji dla wszystkich kontenerów woluminów w zaimportowanym pliku konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="77d79-119">Indicates that this cmdlet starts migration time estimates for all volume containers in the imported configuration file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: MigrateAllContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77d79-120">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="77d79-120">-LegacyConfigId</span></span>
<span data-ttu-id="77d79-121">Określa unikatowy identyfikator starszego urządzenia.</span><span class="sxs-lookup"><span data-stu-id="77d79-121">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="77d79-122">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="77d79-122">-LegacyContainerNames</span></span>
<span data-ttu-id="77d79-123">Określa tablicę nazw kontenerów woluminów, dla których ma zostać utworzony plan migracji.</span><span class="sxs-lookup"><span data-stu-id="77d79-123">Specifies an array of volume container names for which to create a migration plan.</span></span>

```yaml
Type: String[]
Parameter Sets: MigrateSpecificContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77d79-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="77d79-124">-Profile</span></span>
<span data-ttu-id="77d79-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77d79-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="77d79-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="77d79-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="77d79-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77d79-127">CommonParameters</span></span>
<span data-ttu-id="77d79-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77d79-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77d79-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77d79-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77d79-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77d79-130">INPUTS</span></span>

### <span data-ttu-id="77d79-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="77d79-131">None</span></span>

## <span data-ttu-id="77d79-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77d79-132">OUTPUTS</span></span>

### <span data-ttu-id="77d79-133">Ciąg</span><span class="sxs-lookup"><span data-stu-id="77d79-133">String</span></span>
<span data-ttu-id="77d79-134">To polecenie cmdlet zwraca stan zadania planu migracji, jeśli zostało pomyślnie uruchomione na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="77d79-134">This cmdlet returns the status of the migration plan job if it has been successfully started in the appliance.</span></span>

## <span data-ttu-id="77d79-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77d79-135">NOTES</span></span>

## <span data-ttu-id="77d79-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77d79-136">RELATED LINKS</span></span>

[<span data-ttu-id="77d79-137">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="77d79-137">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)



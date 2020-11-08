---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 23272A36-8F55-41A8-AFC9-2EEE0FA55DA3
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd341437019b6adbe6c2a5a93076baff61e1f0d7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055224"
---
# <span data-ttu-id="399c4-101">Import-AzureStorSimpleLegacyVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="399c4-101">Import-AzureStorSimpleLegacyVolumeContainer</span></span>

## <span data-ttu-id="399c4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="399c4-102">SYNOPSIS</span></span>
<span data-ttu-id="399c4-103">Rozpoczyna migrację kontenerów woluminów.</span><span class="sxs-lookup"><span data-stu-id="399c4-103">Starts the migration of volume containers.</span></span>

## <span data-ttu-id="399c4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="399c4-104">SYNTAX</span></span>

### <span data-ttu-id="399c4-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="399c4-105">MigrateSpecificContainer</span></span>
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> -LegacyContainerNames <String[]>
 [-SkipACRs] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="399c4-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="399c4-106">MigrateAllContainer</span></span>
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> [-All] [-SkipACRs] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="399c4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="399c4-107">DESCRIPTION</span></span>
<span data-ttu-id="399c4-108">Polecenie cmdlet **Import-AzureStorSimpleLegacyVolumeContainer** rozpoczyna migrację kontenerów woluminów ze starszego urządzenia na urządzenie docelowe.</span><span class="sxs-lookup"><span data-stu-id="399c4-108">The **Import-AzureStorSimpleLegacyVolumeContainer** cmdlet starts the migration of volume containers from a legacy appliance to the target appliance.</span></span>

## <span data-ttu-id="399c4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="399c4-109">EXAMPLES</span></span>

### <span data-ttu-id="399c4-110">Przykład 1: Importowanie starszego kontenera woluminów</span><span class="sxs-lookup"><span data-stu-id="399c4-110">Example 1: Import a legacy volume container</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

<span data-ttu-id="399c4-111">To polecenie importuje stary kontener woluminu dla nazwanego kontenera.</span><span class="sxs-lookup"><span data-stu-id="399c4-111">This command imports a legacy volume container for the named container.</span></span>
<span data-ttu-id="399c4-112">Polecenie cmdlet rozpoczyna importowanie, a następnie zwraca wiadomość.</span><span class="sxs-lookup"><span data-stu-id="399c4-112">The cmdlet starts the import, and then returns a message.</span></span>

### <span data-ttu-id="399c4-113">Przykład 2: Importowanie wszystkich starszych kontenerów woluminów</span><span class="sxs-lookup"><span data-stu-id="399c4-113">Example 2: Import all legacy volume containers</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

<span data-ttu-id="399c4-114">To polecenie importuje wszystkie starsze kontenery woluminów z zaimportowanego pliku konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="399c4-114">This command imports all legacy volume containers from configuration file imported.</span></span>
<span data-ttu-id="399c4-115">Polecenie cmdlet rozpoczyna importowanie, a następnie zwraca wiadomość.</span><span class="sxs-lookup"><span data-stu-id="399c4-115">The cmdlet starts the import, and then returns a message.</span></span>

## <span data-ttu-id="399c4-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="399c4-116">PARAMETERS</span></span>

### <span data-ttu-id="399c4-117">-All</span><span class="sxs-lookup"><span data-stu-id="399c4-117">-All</span></span>
<span data-ttu-id="399c4-118">Wskazuje, że to polecenie cmdlet importuje wszystkie kontenery woluminów z zaimportowanego pliku konfiguracji do urządzenia docelowego.</span><span class="sxs-lookup"><span data-stu-id="399c4-118">Indicates that this cmdlet imports all volume containers in the imported configuration file to the target device.</span></span>

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

### <span data-ttu-id="399c4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="399c4-119">-Force</span></span>
<span data-ttu-id="399c4-120">Wskazuje, że ten polecenie cmdlet importuje kontener woluminu na innym urządzeniu, nawet jeśli kontener wolumenu został zaimportowany na innym urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="399c4-120">Indicates that this cmdlet imports volume container on a different device, even if volume container has been imported on a different device.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="399c4-121">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="399c4-121">-LegacyConfigId</span></span>
<span data-ttu-id="399c4-122">Określa unikatowy identyfikator starszego urządzenia.</span><span class="sxs-lookup"><span data-stu-id="399c4-122">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="399c4-123">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="399c4-123">-LegacyContainerNames</span></span>
<span data-ttu-id="399c4-124">Określa tablicę nazw kontenerów woluminów, dla których obowiązuje plan migracji.</span><span class="sxs-lookup"><span data-stu-id="399c4-124">Specifies an array of volume container names for which the migration plan applies.</span></span>

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

### <span data-ttu-id="399c4-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="399c4-125">-Profile</span></span>
<span data-ttu-id="399c4-126">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="399c4-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="399c4-127">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="399c4-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="399c4-128">-SkipACRs</span><span class="sxs-lookup"><span data-stu-id="399c4-128">-SkipACRs</span></span>
<span data-ttu-id="399c4-129">Wskazuje, że proces importowania pominie rekordy kontroli dostępu do migracji.</span><span class="sxs-lookup"><span data-stu-id="399c4-129">Indicates that the import process skips access control records for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="399c4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="399c4-130">CommonParameters</span></span>
<span data-ttu-id="399c4-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="399c4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="399c4-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="399c4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="399c4-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="399c4-133">INPUTS</span></span>

## <span data-ttu-id="399c4-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="399c4-134">OUTPUTS</span></span>

### <span data-ttu-id="399c4-135">Ciąg</span><span class="sxs-lookup"><span data-stu-id="399c4-135">String</span></span>
<span data-ttu-id="399c4-136">To polecenie zwraca stan zadania importowania kontenera woluminu migracji, jeśli został on pomyślnie uruchomiony na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="399c4-136">This command returns the status of the migration import volume container job if it has been successfully started in the appliance.</span></span>

## <span data-ttu-id="399c4-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="399c4-137">NOTES</span></span>

## <span data-ttu-id="399c4-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="399c4-138">RELATED LINKS</span></span>

[<span data-ttu-id="399c4-139">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="399c4-139">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="399c4-140">Import — AzureStorSimpleLegacyApplianceConfig</span><span class="sxs-lookup"><span data-stu-id="399c4-140">Import-AzureStorSimpleLegacyApplianceConfig</span></span>](./Import-AzureStorSimpleLegacyApplianceConfig.md)



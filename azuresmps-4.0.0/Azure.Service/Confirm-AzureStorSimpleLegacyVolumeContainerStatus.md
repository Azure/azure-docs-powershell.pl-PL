---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 97AC691F-3835-4CEE-B47E-430BE9962AF9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 26fcee5f6cb669ef49993a009aa76e9c9522b180
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054666"
---
# <span data-ttu-id="68139-101">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="68139-101">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>

## <span data-ttu-id="68139-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68139-102">SYNOPSIS</span></span>
<span data-ttu-id="68139-103">Inicjuje przekazywanie lub wycofywanie kontenerów woluminów, które zostały zmigrowane.</span><span class="sxs-lookup"><span data-stu-id="68139-103">Initiates the commit or rollback of the volume containers that are migrated.</span></span>

## <span data-ttu-id="68139-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68139-104">SYNTAX</span></span>

### <span data-ttu-id="68139-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="68139-105">MigrateSpecificContainer</span></span>
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="68139-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="68139-106">MigrateAllContainer</span></span>
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="68139-107">Opis</span><span class="sxs-lookup"><span data-stu-id="68139-107">DESCRIPTION</span></span>
<span data-ttu-id="68139-108">Polecenie cmdlet **Confirm-AzureStorSimpleLegacyVolumeContainerStatus** inicjuje przekazywanie lub wycofywanie kontenerów woluminów, które są migrowane w ramach migracji starszej wersji.</span><span class="sxs-lookup"><span data-stu-id="68139-108">The **Confirm-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet initiates the commit or rollback of the volume containers that are migrated as part of a legacy migration.</span></span>
<span data-ttu-id="68139-109">Przywracanie przywraca pierwotnemu właścicielowi urządzenia.</span><span class="sxs-lookup"><span data-stu-id="68139-109">The rollback restores the appliance to the original ownership.</span></span>
<span data-ttu-id="68139-110">Zlecenie przypisuje własność docelowemu urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="68139-110">The commit assigns the ownership to the target appliance.</span></span>

## <span data-ttu-id="68139-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68139-111">EXAMPLES</span></span>

### <span data-ttu-id="68139-112">Przykład 1. Rozpoczynanie operacji zatwierdzania na określonym kontenerze woluminów</span><span class="sxs-lookup"><span data-stu-id="68139-112">Example 1: Initiate a commit operation on a specific volume container</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Commit
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="68139-113">To polecenie inicjuje operację commit na określonym kontenerze woluminów dla określonego identyfikatora konfiguracji starszego typu.</span><span class="sxs-lookup"><span data-stu-id="68139-113">This command initiates a commit operation on the specified volume container for the specified legacy configuration ID.</span></span>
<span data-ttu-id="68139-114">Aby wyświetlić stan operacji, użyj polecenia cmdlet **Get-AzureStorSimpleLegacyVolumeContainerStatus** .</span><span class="sxs-lookup"><span data-stu-id="68139-114">To see the status of the operation, use the **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet.</span></span>

### <span data-ttu-id="68139-115">Przykład 2: Inicjowanie operacji wycofywania na określonym kontenerze woluminów</span><span class="sxs-lookup"><span data-stu-id="68139-115">Example 2: Initiate a rollback operation on a specific volume container</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Rollback
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="68139-116">To polecenie inicjuje operację wycofywania na określonym kontenerze woluminów dla określonego identyfikatora konfiguracji starszego typu.</span><span class="sxs-lookup"><span data-stu-id="68139-116">This command initiates a rollback operation on the specified volume container for the specified legacy configuration ID.</span></span>

### <span data-ttu-id="68139-117">Przykład 3: Inicjowanie operacji zatwierdzania dla wszystkich kontenerów woluminów</span><span class="sxs-lookup"><span data-stu-id="68139-117">Example 3: Initiate a commit operation on all volume containers</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Commit -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="68139-118">To polecenie inicjuje operację commit na całym kontenerze woluminów dla określonego identyfikatora konfiguracji starszego typu.</span><span class="sxs-lookup"><span data-stu-id="68139-118">This command initiates a commit operation on all volume container for the specified legacy configuration ID.</span></span>

### <span data-ttu-id="68139-119">Przykład 4: zainicjowanie operacji wycofywania dla wszystkich kontenerów woluminów</span><span class="sxs-lookup"><span data-stu-id="68139-119">Example 4: Initiate a rollback operation on all volume containers</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Rollback -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="68139-120">To polecenie inicjuje operację wycofywania na wszystkich kontenerach woluminów dla określonego identyfikatora konfiguracji starszego typu.</span><span class="sxs-lookup"><span data-stu-id="68139-120">This command initiates a rollback operation on all volume containers for the specified legacy configuration ID.</span></span>

## <span data-ttu-id="68139-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68139-121">PARAMETERS</span></span>

### <span data-ttu-id="68139-122">-All</span><span class="sxs-lookup"><span data-stu-id="68139-122">-All</span></span>
<span data-ttu-id="68139-123">Wskazuje, że to polecenie cmdlet Inicjuje operację wycofywania lub zatwierdzania dla wszystkich kontenerów woluminów w zaimportowanym pliku konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="68139-123">Indicates that this cmdlet initiates a roll back or commit operation on all volume containers in the imported configuration file.</span></span>

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

### <span data-ttu-id="68139-124">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="68139-124">-LegacyConfigId</span></span>
<span data-ttu-id="68139-125">Określa unikatowy identyfikator starszego urządzenia.</span><span class="sxs-lookup"><span data-stu-id="68139-125">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="68139-126">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="68139-126">-LegacyContainerNames</span></span>
<span data-ttu-id="68139-127">Określa tablicę nazw kontenerów woluminów, dla których obowiązuje plan migracji.</span><span class="sxs-lookup"><span data-stu-id="68139-127">Specifies an array of volume container names for which the migration plan applies.</span></span>

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

### <span data-ttu-id="68139-128">-MigrationOperation</span><span class="sxs-lookup"><span data-stu-id="68139-128">-MigrationOperation</span></span>
<span data-ttu-id="68139-129">Określa, czy to polecenie cmdlet wykonuje zatwierdzenie lub wycofanie.</span><span class="sxs-lookup"><span data-stu-id="68139-129">Specifies whether this cmdlet performs a commit or rollback.</span></span>
<span data-ttu-id="68139-130">Prawidłowe wartości to: Commit i Rollback.</span><span class="sxs-lookup"><span data-stu-id="68139-130">Valid values are: Commit and Rollback.</span></span>

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

### <span data-ttu-id="68139-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="68139-131">-Profile</span></span>
<span data-ttu-id="68139-132">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68139-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="68139-133">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="68139-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="68139-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68139-134">CommonParameters</span></span>
<span data-ttu-id="68139-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68139-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68139-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68139-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68139-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68139-137">INPUTS</span></span>

## <span data-ttu-id="68139-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68139-138">OUTPUTS</span></span>

## <span data-ttu-id="68139-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68139-139">NOTES</span></span>

## <span data-ttu-id="68139-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68139-140">RELATED LINKS</span></span>

[<span data-ttu-id="68139-141">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="68139-141">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="68139-142">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="68139-142">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)

[<span data-ttu-id="68139-143">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="68139-143">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)



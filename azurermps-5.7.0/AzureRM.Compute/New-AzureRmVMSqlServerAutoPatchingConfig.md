---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 516192dab6d075979a2d78cea72afaedb7a18231
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544499"
---
# <span data-ttu-id="423a5-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="423a5-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="423a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="423a5-102">SYNOPSIS</span></span>
<span data-ttu-id="423a5-103">Tworzy obiekt konfiguracji na potrzeby automatycznego poprawiania na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="423a5-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="423a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="423a5-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="423a5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="423a5-105">DESCRIPTION</span></span>
<span data-ttu-id="423a5-106">Polecenie cmdlet **New-AzureVMSqlServerAutoPatchingConfig** tworzy obiekt konfiguracji na potrzeby automatycznego poprawiania na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="423a5-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="423a5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="423a5-107">EXAMPLES</span></span>

### <span data-ttu-id="423a5-108">Przykład 1. Tworzenie obiektu konfiguracji w celu skonfigurowania automatycznej poprawki</span><span class="sxs-lookup"><span data-stu-id="423a5-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="423a5-109">To polecenie tworzy obiekt konfiguracji do tworzenia poprawek.</span><span class="sxs-lookup"><span data-stu-id="423a5-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="423a5-110">Polecenie określa dzień tygodnia i definiuje okno obsługi.</span><span class="sxs-lookup"><span data-stu-id="423a5-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="423a5-111">Ta konfiguracja umożliwia stosowanie poprawek korzystających z tych wartości.</span><span class="sxs-lookup"><span data-stu-id="423a5-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="423a5-112">Polecenie zapisuje wyniki w zmiennej $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="423a5-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="423a5-113">Możesz określić ten element konfiguracji dla innych poleceń cmdlet, takich jak polecenie cmdlet Set-AzureRmVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="423a5-113">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="423a5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="423a5-114">PARAMETERS</span></span>

### <span data-ttu-id="423a5-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="423a5-115">-DayOfWeek</span></span>
<span data-ttu-id="423a5-116">Określa dzień tygodnia, w którym powinny być instalowane aktualizacje.</span><span class="sxs-lookup"><span data-stu-id="423a5-116">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="423a5-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="423a5-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="423a5-118">Niedziele</span><span class="sxs-lookup"><span data-stu-id="423a5-118">Sunday</span></span>
- <span data-ttu-id="423a5-119">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="423a5-119">Monday</span></span>
- <span data-ttu-id="423a5-120">Wtorku</span><span class="sxs-lookup"><span data-stu-id="423a5-120">Tuesday</span></span>
- <span data-ttu-id="423a5-121">Środa</span><span class="sxs-lookup"><span data-stu-id="423a5-121">Wednesday</span></span>
- <span data-ttu-id="423a5-122">Czwartek</span><span class="sxs-lookup"><span data-stu-id="423a5-122">Thursday</span></span>
- <span data-ttu-id="423a5-123">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="423a5-123">Friday</span></span>
- <span data-ttu-id="423a5-124">Sobota</span><span class="sxs-lookup"><span data-stu-id="423a5-124">Saturday</span></span>
- <span data-ttu-id="423a5-125">Codzienne</span><span class="sxs-lookup"><span data-stu-id="423a5-125">Everyday</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="423a5-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="423a5-126">-Enable</span></span>
<span data-ttu-id="423a5-127">Wskazuje, że automatyczne poprawianie maszyny wirtualnej jest włączone.</span><span class="sxs-lookup"><span data-stu-id="423a5-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="423a5-128">Jeśli włączysz automatyczne poprawianie, polecenie cmdlet przełączy system Windows do trybu interakcyjnego.</span><span class="sxs-lookup"><span data-stu-id="423a5-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="423a5-129">Jeśli wyłączysz automatyczne stosowanie, ustawienia Windows Update nie zmieniają się.</span><span class="sxs-lookup"><span data-stu-id="423a5-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="423a5-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="423a5-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="423a5-131">Określa czas trwania okna konserwacji (w minutach).</span><span class="sxs-lookup"><span data-stu-id="423a5-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="423a5-132">Automatyczne poprawianie nie pozwala na wykonywanie akcji, które mogą wpłynąć na dostępność maszyny wirtualnej poza tym oknem.</span><span class="sxs-lookup"><span data-stu-id="423a5-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="423a5-133">Określ wielokrotność 30 minut.</span><span class="sxs-lookup"><span data-stu-id="423a5-133">Specify a multiple of 30 minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="423a5-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="423a5-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="423a5-135">Określa godzinę dnia, kiedy zostanie uruchomione okno konserwacja.</span><span class="sxs-lookup"><span data-stu-id="423a5-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="423a5-136">Ten czas określa, kiedy aktualizacje rozpoczną instalację.</span><span class="sxs-lookup"><span data-stu-id="423a5-136">This time defines when updates start to install.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="423a5-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="423a5-137">-PatchCategory</span></span>
<span data-ttu-id="423a5-138">Określa, czy należy uwzględnić ważne aktualizacje.</span><span class="sxs-lookup"><span data-stu-id="423a5-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="423a5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="423a5-139">CommonParameters</span></span>
<span data-ttu-id="423a5-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="423a5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="423a5-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="423a5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="423a5-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="423a5-142">INPUTS</span></span>

### <span data-ttu-id="423a5-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="423a5-143">None</span></span>
<span data-ttu-id="423a5-144">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="423a5-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="423a5-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="423a5-145">OUTPUTS</span></span>

### <span data-ttu-id="423a5-146">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="423a5-146">AutoPatchingSettings</span></span>
<span data-ttu-id="423a5-147">To polecenie cmdlet zwraca obiekt zawiera ustawienia automatycznej poprawki.</span><span class="sxs-lookup"><span data-stu-id="423a5-147">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="423a5-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="423a5-148">NOTES</span></span>

## <span data-ttu-id="423a5-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="423a5-149">RELATED LINKS</span></span>

[<span data-ttu-id="423a5-150">Nowe — AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="423a5-150">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="423a5-151">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="423a5-151">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)



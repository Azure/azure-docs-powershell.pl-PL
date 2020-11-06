---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 17d99840bffb9063ad61dec00d4b7d5983118399
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553975"
---
# <span data-ttu-id="ffd12-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="ffd12-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="ffd12-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ffd12-102">SYNOPSIS</span></span>
<span data-ttu-id="ffd12-103">Tworzy obiekt konfiguracji na potrzeby automatycznego poprawiania na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ffd12-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffd12-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ffd12-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ffd12-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ffd12-105">DESCRIPTION</span></span>
<span data-ttu-id="ffd12-106">Polecenie cmdlet **New-AzureVMSqlServerAutoPatchingConfig** tworzy obiekt konfiguracji na potrzeby automatycznego poprawiania na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ffd12-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="ffd12-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ffd12-107">EXAMPLES</span></span>

### <span data-ttu-id="ffd12-108">Przykład 1. Tworzenie obiektu konfiguracji w celu skonfigurowania automatycznej poprawki</span><span class="sxs-lookup"><span data-stu-id="ffd12-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="ffd12-109">To polecenie tworzy obiekt konfiguracji do tworzenia poprawek.</span><span class="sxs-lookup"><span data-stu-id="ffd12-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="ffd12-110">Polecenie określa dzień tygodnia i definiuje okno obsługi.</span><span class="sxs-lookup"><span data-stu-id="ffd12-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="ffd12-111">Ta konfiguracja umożliwia stosowanie poprawek korzystających z tych wartości.</span><span class="sxs-lookup"><span data-stu-id="ffd12-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="ffd12-112">Polecenie zapisuje wyniki w zmiennej $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="ffd12-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="ffd12-113">Możesz określić ten element konfiguracji dla innych poleceń cmdlet, takich jak polecenie cmdlet Set-AzureRmVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="ffd12-113">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="ffd12-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ffd12-114">PARAMETERS</span></span>

### <span data-ttu-id="ffd12-115">-Enable</span><span class="sxs-lookup"><span data-stu-id="ffd12-115">-Enable</span></span>
<span data-ttu-id="ffd12-116">Wskazuje, że automatyczne poprawianie maszyny wirtualnej jest włączone.</span><span class="sxs-lookup"><span data-stu-id="ffd12-116">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="ffd12-117">Jeśli włączysz automatyczne poprawianie, polecenie cmdlet przełączy system Windows do trybu interakcyjnego.</span><span class="sxs-lookup"><span data-stu-id="ffd12-117">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="ffd12-118">Jeśli wyłączysz automatyczne stosowanie, ustawienia Windows Update nie zmieniają się.</span><span class="sxs-lookup"><span data-stu-id="ffd12-118">If you disable automated patching, Windows Update settings do not change.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffd12-119">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="ffd12-119">-DayOfWeek</span></span>
<span data-ttu-id="ffd12-120">Określa dzień tygodnia, w którym powinny być instalowane aktualizacje.</span><span class="sxs-lookup"><span data-stu-id="ffd12-120">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="ffd12-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ffd12-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ffd12-122">Niedziele</span><span class="sxs-lookup"><span data-stu-id="ffd12-122">Sunday</span></span>
- <span data-ttu-id="ffd12-123">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="ffd12-123">Monday</span></span>
- <span data-ttu-id="ffd12-124">Wtorku</span><span class="sxs-lookup"><span data-stu-id="ffd12-124">Tuesday</span></span>
- <span data-ttu-id="ffd12-125">Środa</span><span class="sxs-lookup"><span data-stu-id="ffd12-125">Wednesday</span></span>
- <span data-ttu-id="ffd12-126">Czwartek</span><span class="sxs-lookup"><span data-stu-id="ffd12-126">Thursday</span></span>
- <span data-ttu-id="ffd12-127">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="ffd12-127">Friday</span></span>
- <span data-ttu-id="ffd12-128">Sobota</span><span class="sxs-lookup"><span data-stu-id="ffd12-128">Saturday</span></span>
- <span data-ttu-id="ffd12-129">Codzienne</span><span class="sxs-lookup"><span data-stu-id="ffd12-129">Everyday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffd12-130">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="ffd12-130">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="ffd12-131">Określa godzinę dnia, kiedy zostanie uruchomione okno konserwacja.</span><span class="sxs-lookup"><span data-stu-id="ffd12-131">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="ffd12-132">Ten czas określa, kiedy aktualizacje rozpoczną instalację.</span><span class="sxs-lookup"><span data-stu-id="ffd12-132">This time defines when updates start to install.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffd12-133">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="ffd12-133">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="ffd12-134">Określa czas trwania okna konserwacji (w minutach).</span><span class="sxs-lookup"><span data-stu-id="ffd12-134">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="ffd12-135">Automatyczne poprawianie nie pozwala na wykonywanie akcji, które mogą wpłynąć na dostępność maszyny wirtualnej poza tym oknem.</span><span class="sxs-lookup"><span data-stu-id="ffd12-135">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="ffd12-136">Określ wielokrotność 30 minut.</span><span class="sxs-lookup"><span data-stu-id="ffd12-136">Specify a multiple of 30 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffd12-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="ffd12-137">-PatchCategory</span></span>
<span data-ttu-id="ffd12-138">Określa, czy należy uwzględnić ważne aktualizacje.</span><span class="sxs-lookup"><span data-stu-id="ffd12-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffd12-139">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ffd12-139">-InformationAction</span></span>
<span data-ttu-id="ffd12-140">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="ffd12-140">@{Text=}</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffd12-141">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ffd12-141">-InformationVariable</span></span>
<span data-ttu-id="ffd12-142">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="ffd12-142">@{Text=}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffd12-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffd12-143">CommonParameters</span></span>
<span data-ttu-id="ffd12-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffd12-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffd12-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffd12-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffd12-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ffd12-146">INPUTS</span></span>

## <span data-ttu-id="ffd12-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ffd12-147">OUTPUTS</span></span>

### <span data-ttu-id="ffd12-148">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="ffd12-148">AutoPatchingSettings</span></span>
<span data-ttu-id="ffd12-149">To polecenie cmdlet zwraca obiekt zawiera ustawienia automatycznej poprawki.</span><span class="sxs-lookup"><span data-stu-id="ffd12-149">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="ffd12-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ffd12-150">NOTES</span></span>

## <span data-ttu-id="ffd12-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ffd12-151">RELATED LINKS</span></span>

[<span data-ttu-id="ffd12-152">Nowe — AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="ffd12-152">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="ffd12-153">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="ffd12-153">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)



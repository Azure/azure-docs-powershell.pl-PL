---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7317DAC1-B535-4650-86BF-73E96F61EECD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23bb8e09fac8ec4fe0e8ff5b3c23ab995f03694c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055157"
---
# <span data-ttu-id="e9b73-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="e9b73-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="e9b73-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e9b73-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b73-103">Tworzy obiekt konfiguracji do automatycznego tworzenia poprawek maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e9b73-103">Creates a configuration object for virtual machine automatic patching.</span></span>

## <span data-ttu-id="e9b73-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e9b73-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e9b73-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e9b73-105">DESCRIPTION</span></span>
<span data-ttu-id="e9b73-106">Polecenie cmdlet **New-AzureVMSqlServerAutoPatchingConfig** tworzy obiekt konfiguracji do automatycznego tworzenia poprawek maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e9b73-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for virtual machine automatic patching.</span></span>

## <span data-ttu-id="e9b73-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e9b73-107">EXAMPLES</span></span>

### <span data-ttu-id="e9b73-108">Przykład 1. Tworzenie obiektu konfiguracji w celu skonfigurowania automatycznej poprawki</span><span class="sxs-lookup"><span data-stu-id="e9b73-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $APS = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
          Enable                        : True
          DayOfWeek                     : Thursday
          MaintenanceWindowStartingHour : 11
          MaintenanceWindowDuration     : 120
          PatchCategory                 : Important
```

<span data-ttu-id="e9b73-109">To polecenie tworzy obiekt konfiguracji, którego można użyć w celu skonfigurowania automatycznej poprawki za pomocą polecenia Set-AzureVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="e9b73-109">This command creates configuration object that can be used to configure automatic patching using Set-AzureVMSqlServerExtension.</span></span>

## <span data-ttu-id="e9b73-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e9b73-110">PARAMETERS</span></span>

### <span data-ttu-id="e9b73-111">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="e9b73-111">-DayOfWeek</span></span>
<span data-ttu-id="e9b73-112">Określa dzień tygodnia, w którym powinny być instalowane aktualizacje.</span><span class="sxs-lookup"><span data-stu-id="e9b73-112">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="e9b73-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e9b73-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e9b73-114">Niedziele</span><span class="sxs-lookup"><span data-stu-id="e9b73-114">Sunday</span></span>
- <span data-ttu-id="e9b73-115">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="e9b73-115">Monday</span></span>
- <span data-ttu-id="e9b73-116">Wtorku</span><span class="sxs-lookup"><span data-stu-id="e9b73-116">Tuesday</span></span>
- <span data-ttu-id="e9b73-117">Środa</span><span class="sxs-lookup"><span data-stu-id="e9b73-117">Wednesday</span></span>
- <span data-ttu-id="e9b73-118">Czwartek</span><span class="sxs-lookup"><span data-stu-id="e9b73-118">Thursday</span></span>
- <span data-ttu-id="e9b73-119">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="e9b73-119">Friday</span></span>
- <span data-ttu-id="e9b73-120">Sobota</span><span class="sxs-lookup"><span data-stu-id="e9b73-120">Saturday</span></span>
- <span data-ttu-id="e9b73-121">Codzienne</span><span class="sxs-lookup"><span data-stu-id="e9b73-121">Everyday</span></span>

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

### <span data-ttu-id="e9b73-122">-Enable</span><span class="sxs-lookup"><span data-stu-id="e9b73-122">-Enable</span></span>
<span data-ttu-id="e9b73-123">Wskazuje, że automatyczne poprawianie maszyny wirtualnej jest włączone.</span><span class="sxs-lookup"><span data-stu-id="e9b73-123">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="e9b73-124">Jeśli włączysz automatyczne poprawianie, polecenie cmdlet spowoduje przejście systemu Windows do trybu interakcyjnego.</span><span class="sxs-lookup"><span data-stu-id="e9b73-124">If you enable automated patching the cmdlet will put Windows Update into interactive mode.</span></span>
<span data-ttu-id="e9b73-125">Jeśli wyłączysz automatyczne stosowanie, ustawienia Windows Update nie zmienią się.</span><span class="sxs-lookup"><span data-stu-id="e9b73-125">If you disable automated patching, Windows Update settings will not change.</span></span>

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

### <span data-ttu-id="e9b73-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e9b73-126">-InformationAction</span></span>
<span data-ttu-id="e9b73-127">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="e9b73-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e9b73-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e9b73-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e9b73-129">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="e9b73-129">Continue</span></span>
- <span data-ttu-id="e9b73-130">Ignorować</span><span class="sxs-lookup"><span data-stu-id="e9b73-130">Ignore</span></span>
- <span data-ttu-id="e9b73-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="e9b73-131">Inquire</span></span>
- <span data-ttu-id="e9b73-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e9b73-132">SilentlyContinue</span></span>
- <span data-ttu-id="e9b73-133">Przestaw</span><span class="sxs-lookup"><span data-stu-id="e9b73-133">Stop</span></span>
- <span data-ttu-id="e9b73-134">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="e9b73-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b73-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e9b73-135">-InformationVariable</span></span>
<span data-ttu-id="e9b73-136">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="e9b73-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b73-137">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="e9b73-137">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="e9b73-138">Określa czas trwania okna obsługi.</span><span class="sxs-lookup"><span data-stu-id="e9b73-138">Specifies the duration of the maintenance window.</span></span>
<span data-ttu-id="e9b73-139">Automatyczne poprawianie spowoduje uniknięcie wykonania akcji, która może wpływać na dostępność maszyny wirtualnej poza tym oknem.</span><span class="sxs-lookup"><span data-stu-id="e9b73-139">Automated patching will avoid performing an action that can impact a virtual machine availability outside of that window.</span></span>
<span data-ttu-id="e9b73-140">Dozwolone są tylko 30 minut.</span><span class="sxs-lookup"><span data-stu-id="e9b73-140">Only 30 minutes increments are allowed.</span></span>

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

### <span data-ttu-id="e9b73-141">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="e9b73-141">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="e9b73-142">Określa godzinę dnia, kiedy zostanie uruchomione okno konserwacja.</span><span class="sxs-lookup"><span data-stu-id="e9b73-142">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="e9b73-143">Ten czas określa, kiedy aktualizacje rozpoczynają instalację i są zaokrąglane do godziny.</span><span class="sxs-lookup"><span data-stu-id="e9b73-143">This time defines when updates start installing and is rounded to the hour.</span></span>

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

### <span data-ttu-id="e9b73-144">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="e9b73-144">-PatchCategory</span></span>
<span data-ttu-id="e9b73-145">Określa, czy należy uwzględnić ważne aktualizacje.</span><span class="sxs-lookup"><span data-stu-id="e9b73-145">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="e9b73-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b73-146">CommonParameters</span></span>
<span data-ttu-id="e9b73-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9b73-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b73-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9b73-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b73-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9b73-149">INPUTS</span></span>

## <span data-ttu-id="e9b73-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e9b73-150">OUTPUTS</span></span>

### <span data-ttu-id="e9b73-151">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="e9b73-151">AutoPatchingSettings</span></span>
<span data-ttu-id="e9b73-152">To polecenie cmdlet zwraca obiekt zawiera ustawienia automatycznej poprawki.</span><span class="sxs-lookup"><span data-stu-id="e9b73-152">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="e9b73-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e9b73-153">NOTES</span></span>

## <span data-ttu-id="e9b73-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9b73-154">RELATED LINKS</span></span>

[<span data-ttu-id="e9b73-155">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e9b73-155">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)

[<span data-ttu-id="e9b73-156">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e9b73-156">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)

[<span data-ttu-id="e9b73-157">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e9b73-157">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)



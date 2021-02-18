---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 6fe89822af5be532674e22dd3e1c1edd583fced4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181562"
---
# <span data-ttu-id="51a1d-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="51a1d-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="51a1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51a1d-102">SYNOPSIS</span></span>
<span data-ttu-id="51a1d-103">Tworzy obiekt konfiguracji na celu automatyczne poprawianie poprawek na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="51a1d-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="51a1d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="51a1d-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="51a1d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="51a1d-105">DESCRIPTION</span></span>
<span data-ttu-id="51a1d-106">Polecenie **cmdlet New-AzVMSqlServerAutoPatchingConfig** tworzy obiekt konfiguracji do automatycznego poprawiania na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="51a1d-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="51a1d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="51a1d-107">EXAMPLES</span></span>

### <span data-ttu-id="51a1d-108">Przykład 1. Tworzenie obiektu konfiguracji w celu skonfigurowania automatycznego poprawiania poprawek</span><span class="sxs-lookup"><span data-stu-id="51a1d-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="51a1d-109">To polecenie tworzy obiekt konfiguracji na celu tworzenie poprawek.</span><span class="sxs-lookup"><span data-stu-id="51a1d-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="51a1d-110">To polecenie określa dzień tygodnia i definiuje okno konserwacji.</span><span class="sxs-lookup"><span data-stu-id="51a1d-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="51a1d-111">Ta konfiguracja umożliwia tworzenie poprawek, w których są używane te wartości.</span><span class="sxs-lookup"><span data-stu-id="51a1d-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="51a1d-112">Polecenie przechowuje wynik w $AutoBackupConfig zmienną.</span><span class="sxs-lookup"><span data-stu-id="51a1d-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="51a1d-113">Ten element konfiguracji można określić dla innych pozycji cmdlet, takich jak polecenie cmdlet Set-AzVMSqlServerExtension cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51a1d-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="51a1d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51a1d-114">PARAMETERS</span></span>

### <span data-ttu-id="51a1d-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="51a1d-115">-DayOfWeek</span></span>
<span data-ttu-id="51a1d-116">Określa dzień tygodnia, w którym mają być instalowane aktualizacje.</span><span class="sxs-lookup"><span data-stu-id="51a1d-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="51a1d-117">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="51a1d-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="51a1d-118">Niedziela</span><span class="sxs-lookup"><span data-stu-id="51a1d-118">Sunday</span></span>
- <span data-ttu-id="51a1d-119">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="51a1d-119">Monday</span></span>
- <span data-ttu-id="51a1d-120">Wtorek</span><span class="sxs-lookup"><span data-stu-id="51a1d-120">Tuesday</span></span>
- <span data-ttu-id="51a1d-121">Środa</span><span class="sxs-lookup"><span data-stu-id="51a1d-121">Wednesday</span></span>
- <span data-ttu-id="51a1d-122">Czwartek</span><span class="sxs-lookup"><span data-stu-id="51a1d-122">Thursday</span></span>
- <span data-ttu-id="51a1d-123">Piątek</span><span class="sxs-lookup"><span data-stu-id="51a1d-123">Friday</span></span>
- <span data-ttu-id="51a1d-124">Sobota</span><span class="sxs-lookup"><span data-stu-id="51a1d-124">Saturday</span></span>
- <span data-ttu-id="51a1d-125">Codzienne czynności</span><span class="sxs-lookup"><span data-stu-id="51a1d-125">Everyday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51a1d-126">— Włącz</span><span class="sxs-lookup"><span data-stu-id="51a1d-126">-Enable</span></span>
<span data-ttu-id="51a1d-127">Oznacza, że włączono automatyczne poprawianie poprawek dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="51a1d-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="51a1d-128">Włączenie automatycznego poprawiania za pomocą polecenia cmdlet włącza usługę Windows Update w tryb interakcyjny.</span><span class="sxs-lookup"><span data-stu-id="51a1d-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="51a1d-129">Wyłączenie automatycznego poprawiania nie powoduje zmiany ustawień usługi Windows Update.</span><span class="sxs-lookup"><span data-stu-id="51a1d-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="51a1d-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="51a1d-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="51a1d-131">Określa czas trwania (w minutach) okna konserwacji.</span><span class="sxs-lookup"><span data-stu-id="51a1d-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="51a1d-132">Automatyczne poprawianie pozwala uniknąć wykonywania akcji, która może mieć wpływ na dostępność maszyny wirtualnej poza tym oknem.</span><span class="sxs-lookup"><span data-stu-id="51a1d-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="51a1d-133">Określ wielokrotność 30 minut.</span><span class="sxs-lookup"><span data-stu-id="51a1d-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="51a1d-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="51a1d-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="51a1d-135">Określa godzinę dnia, w którym rozpoczyna się okno konserwacji.</span><span class="sxs-lookup"><span data-stu-id="51a1d-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="51a1d-136">Ten czas określa, kiedy rozpocznie się instalowanie aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="51a1d-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="51a1d-137">- PatchCategory</span><span class="sxs-lookup"><span data-stu-id="51a1d-137">-PatchCategory</span></span>
<span data-ttu-id="51a1d-138">Określa, czy należy uwzględniać ważne aktualizacje.</span><span class="sxs-lookup"><span data-stu-id="51a1d-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51a1d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51a1d-139">CommonParameters</span></span>
<span data-ttu-id="51a1d-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51a1d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51a1d-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51a1d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51a1d-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51a1d-142">INPUTS</span></span>

### <span data-ttu-id="51a1d-143">Brak</span><span class="sxs-lookup"><span data-stu-id="51a1d-143">None</span></span>

## <span data-ttu-id="51a1d-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="51a1d-144">OUTPUTS</span></span>

### <span data-ttu-id="51a1d-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="51a1d-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="51a1d-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="51a1d-146">NOTES</span></span>

## <span data-ttu-id="51a1d-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51a1d-147">RELATED LINKS</span></span>

[<span data-ttu-id="51a1d-148">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="51a1d-148">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="51a1d-149">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="51a1d-149">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)



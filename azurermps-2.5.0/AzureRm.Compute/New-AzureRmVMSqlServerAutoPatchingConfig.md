---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverautopatchingconfig
schema: 2.0.0
ms.openlocfilehash: 1204a8b14cdbb45f46edd2a1ca2e4c12c27845a3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898982"
---
# <span data-ttu-id="d577f-101">New-AzureRmVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="d577f-101">New-AzureRmVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="d577f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d577f-102">SYNOPSIS</span></span>
<span data-ttu-id="d577f-103">Tworzy obiekt konfiguracji na potrzeby automatycznego poprawiania na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d577f-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d577f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d577f-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="d577f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d577f-105">DESCRIPTION</span></span>
<span data-ttu-id="d577f-106">Polecenie cmdlet **New-AzureRmVMSqlServerAutoPatchingConfig** tworzy obiekt konfiguracji na potrzeby automatycznego poprawiania na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d577f-106">The **New-AzureRmVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="d577f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d577f-107">EXAMPLES</span></span>

### <span data-ttu-id="d577f-108">Przykład 1. Tworzenie obiektu konfiguracji w celu skonfigurowania automatycznej poprawki</span><span class="sxs-lookup"><span data-stu-id="d577f-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureRmVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="d577f-109">To polecenie tworzy obiekt konfiguracji do tworzenia poprawek.</span><span class="sxs-lookup"><span data-stu-id="d577f-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="d577f-110">Polecenie określa dzień tygodnia i definiuje okno obsługi.</span><span class="sxs-lookup"><span data-stu-id="d577f-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="d577f-111">Ta konfiguracja umożliwia stosowanie poprawek korzystających z tych wartości.</span><span class="sxs-lookup"><span data-stu-id="d577f-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="d577f-112">Polecenie zapisuje wyniki w zmiennej $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="d577f-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="d577f-113">Możesz określić ten element konfiguracji dla innych poleceń cmdlet, takich jak polecenie cmdlet Set-AzureRmVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="d577f-113">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="d577f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d577f-114">PARAMETERS</span></span>

### <span data-ttu-id="d577f-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="d577f-115">-DayOfWeek</span></span>
<span data-ttu-id="d577f-116">Określa dzień tygodnia, w którym powinny być instalowane aktualizacje.</span><span class="sxs-lookup"><span data-stu-id="d577f-116">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="d577f-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d577f-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d577f-118">Niedziele</span><span class="sxs-lookup"><span data-stu-id="d577f-118">Sunday</span></span>
- <span data-ttu-id="d577f-119">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="d577f-119">Monday</span></span>
- <span data-ttu-id="d577f-120">Wtorku</span><span class="sxs-lookup"><span data-stu-id="d577f-120">Tuesday</span></span>
- <span data-ttu-id="d577f-121">Środa</span><span class="sxs-lookup"><span data-stu-id="d577f-121">Wednesday</span></span>
- <span data-ttu-id="d577f-122">Czwartek</span><span class="sxs-lookup"><span data-stu-id="d577f-122">Thursday</span></span>
- <span data-ttu-id="d577f-123">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="d577f-123">Friday</span></span>
- <span data-ttu-id="d577f-124">Sobota</span><span class="sxs-lookup"><span data-stu-id="d577f-124">Saturday</span></span>
- <span data-ttu-id="d577f-125">Codzienne</span><span class="sxs-lookup"><span data-stu-id="d577f-125">Everyday</span></span>

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

### <span data-ttu-id="d577f-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="d577f-126">-Enable</span></span>
<span data-ttu-id="d577f-127">Wskazuje, że automatyczne poprawianie maszyny wirtualnej jest włączone.</span><span class="sxs-lookup"><span data-stu-id="d577f-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="d577f-128">Jeśli włączysz automatyczne poprawianie, polecenie cmdlet przełączy system Windows do trybu interakcyjnego.</span><span class="sxs-lookup"><span data-stu-id="d577f-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="d577f-129">Jeśli wyłączysz automatyczne stosowanie, ustawienia Windows Update nie zmieniają się.</span><span class="sxs-lookup"><span data-stu-id="d577f-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="d577f-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="d577f-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="d577f-131">Określa czas trwania okna konserwacji (w minutach).</span><span class="sxs-lookup"><span data-stu-id="d577f-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="d577f-132">Automatyczne poprawianie nie pozwala na wykonywanie akcji, które mogą wpłynąć na dostępność maszyny wirtualnej poza tym oknem.</span><span class="sxs-lookup"><span data-stu-id="d577f-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="d577f-133">Określ wielokrotność 30 minut.</span><span class="sxs-lookup"><span data-stu-id="d577f-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="d577f-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="d577f-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="d577f-135">Określa godzinę dnia, kiedy zostanie uruchomione okno konserwacja.</span><span class="sxs-lookup"><span data-stu-id="d577f-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="d577f-136">Ten czas określa, kiedy aktualizacje rozpoczną instalację.</span><span class="sxs-lookup"><span data-stu-id="d577f-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="d577f-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="d577f-137">-PatchCategory</span></span>
<span data-ttu-id="d577f-138">Określa, czy należy uwzględnić ważne aktualizacje.</span><span class="sxs-lookup"><span data-stu-id="d577f-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="d577f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d577f-139">CommonParameters</span></span>
<span data-ttu-id="d577f-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d577f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d577f-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d577f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d577f-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d577f-142">INPUTS</span></span>

### <span data-ttu-id="d577f-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d577f-143">None</span></span>
<span data-ttu-id="d577f-144">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d577f-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d577f-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d577f-145">OUTPUTS</span></span>

### <span data-ttu-id="d577f-146">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="d577f-146">AutoPatchingSettings</span></span>
<span data-ttu-id="d577f-147">To polecenie cmdlet zwraca obiekt zawiera ustawienia automatycznej poprawki.</span><span class="sxs-lookup"><span data-stu-id="d577f-147">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="d577f-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d577f-148">NOTES</span></span>

## <span data-ttu-id="d577f-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d577f-149">RELATED LINKS</span></span>



[<span data-ttu-id="d577f-150">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d577f-150">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)



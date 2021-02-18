---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: ac7fb7d6af2e04387ea4abfa3fe62c4df9271b13
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181083"
---
# <span data-ttu-id="5d70d-101">New-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="5d70d-101">New-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="5d70d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d70d-102">SYNOPSIS</span></span>
<span data-ttu-id="5d70d-103">Konfiguruje wyzwalacz na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="5d70d-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="5d70d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5d70d-104">SYNTAX</span></span>

### <span data-ttu-id="5d70d-105">FileEventTriggerParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5d70d-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d70d-106">PeriodicTimerTriggerParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d70d-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d70d-107">FileEventTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d70d-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d70d-108">PeriodicTimerTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d70d-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d70d-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="5d70d-109">DESCRIPTION</span></span>
<span data-ttu-id="5d70d-110">Polecenie **cmdlet New-AzDataBoxEdgeTrigger** konfiguruje wyzwalacz na urządzeniu z krawędzią pola danych.</span><span class="sxs-lookup"><span data-stu-id="5d70d-110">The **New-AzDataBoxEdgeTrigger** cmdlet configures a trigger on the Data Box Edge device.</span></span> 

## <span data-ttu-id="5d70d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5d70d-111">EXAMPLES</span></span>

### <span data-ttu-id="5d70d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5d70d-112">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="5d70d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d70d-113">PARAMETERS</span></span>

### <span data-ttu-id="5d70d-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="5d70d-114">-AsJob</span></span>
<span data-ttu-id="5d70d-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5d70d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d70d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d70d-116">-DefaultProfile</span></span>
<span data-ttu-id="5d70d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d70d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d70d-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5d70d-118">-DeviceName</span></span>
<span data-ttu-id="5d70d-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="5d70d-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d70d-120">-FileEvent</span><span class="sxs-lookup"><span data-stu-id="5d70d-120">-FileEvent</span></span>
<span data-ttu-id="5d70d-121">Przekaż ten parametr przełącznika, aby skonfigurować wyzwalacz FileEvent</span><span class="sxs-lookup"><span data-stu-id="5d70d-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileEventTriggerParameterSet, FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d70d-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5d70d-122">-Name</span></span>
<span data-ttu-id="5d70d-123">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="5d70d-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d70d-124">-PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="5d70d-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="5d70d-125">Przekaż ten parametr przełącznika, aby skonfigurować wyzwalacz PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="5d70d-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d70d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d70d-126">-ResourceGroupName</span></span>
<span data-ttu-id="5d70d-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5d70d-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d70d-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="5d70d-128">-RoleName</span></span>
<span data-ttu-id="5d70d-129">Rola obliczeniowa, w stosunku do której zostaną podniesione zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="5d70d-129">Compute role against which events will be raised.</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d70d-130">— Planowanie</span><span class="sxs-lookup"><span data-stu-id="5d70d-130">-Schedule</span></span>
<span data-ttu-id="5d70d-131">Częstotliwość okresowa, przy której należy podnieść zdarzenie czasomierza.</span><span class="sxs-lookup"><span data-stu-id="5d70d-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="5d70d-132">Określ harmonogram w dniach (od 1 do 365), godzinach (między 1 a 23) lub minutach (między 1 a 59).</span><span class="sxs-lookup"><span data-stu-id="5d70d-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d70d-133">— ShareId</span><span class="sxs-lookup"><span data-stu-id="5d70d-133">-ShareId</span></span>
<span data-ttu-id="5d70d-134">Identyfikator udziału plików do udostępnienia w wyzwalaczu FileEvent</span><span class="sxs-lookup"><span data-stu-id="5d70d-134">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d70d-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="5d70d-135">-ShareName</span></span>
<span data-ttu-id="5d70d-136">Identyfikator udziału plików do udostępnienia w wyzwalaczu FileEvent</span><span class="sxs-lookup"><span data-stu-id="5d70d-136">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d70d-137">— StartTime</span><span class="sxs-lookup"><span data-stu-id="5d70d-137">-StartTime</span></span>
<span data-ttu-id="5d70d-138">Godzina dnia, która powoduje uruchomienie prawidłowego wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="5d70d-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="5d70d-139">Harmonogram jest obliczany z odwołaniem do czasu określonego w sekundach.</span><span class="sxs-lookup"><span data-stu-id="5d70d-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="5d70d-140">Jeśli strefa czasowa nie zostanie określona, czas będzie traktowany jako strefa czasowa urządzenia.</span><span class="sxs-lookup"><span data-stu-id="5d70d-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="5d70d-141">Wartość będzie zawsze zwracana w czasie UTC.</span><span class="sxs-lookup"><span data-stu-id="5d70d-141">The value will always be returned as UTC time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d70d-142">— Temat</span><span class="sxs-lookup"><span data-stu-id="5d70d-142">-Topic</span></span>
<span data-ttu-id="5d70d-143">Temat, w którym zdarzenia okresowe są publikowane na urządzeniu IoT.</span><span class="sxs-lookup"><span data-stu-id="5d70d-143">Topic where periodic events are published to IoT device.</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d70d-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5d70d-144">-Confirm</span></span>
<span data-ttu-id="5d70d-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5d70d-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d70d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d70d-146">-WhatIf</span></span>
<span data-ttu-id="5d70d-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d70d-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d70d-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5d70d-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d70d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d70d-149">CommonParameters</span></span>
<span data-ttu-id="5d70d-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d70d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d70d-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d70d-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d70d-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d70d-152">INPUTS</span></span>

### <span data-ttu-id="5d70d-153">Brak</span><span class="sxs-lookup"><span data-stu-id="5d70d-153">None</span></span>

## <span data-ttu-id="5d70d-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5d70d-154">OUTPUTS</span></span>

### <span data-ttu-id="5d70d-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="5d70d-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="5d70d-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5d70d-156">NOTES</span></span>

## <span data-ttu-id="5d70d-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d70d-157">RELATED LINKS</span></span>

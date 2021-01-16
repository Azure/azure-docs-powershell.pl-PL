---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: ac7fb7d6af2e04387ea4abfa3fe62c4df9271b13
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355057"
---
# <span data-ttu-id="b154a-101">New-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="b154a-101">New-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="b154a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b154a-102">SYNOPSIS</span></span>
<span data-ttu-id="b154a-103">Konfiguruje wyzwalacz na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="b154a-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="b154a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b154a-104">SYNTAX</span></span>

### <span data-ttu-id="b154a-105">FileEventTriggerParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b154a-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b154a-106">PeriodicTimerTriggerParameterSet</span><span class="sxs-lookup"><span data-stu-id="b154a-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b154a-107">FileEventTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b154a-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b154a-108">PeriodicTimerTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b154a-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b154a-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b154a-109">DESCRIPTION</span></span>
<span data-ttu-id="b154a-110">Polecenie cmdlet **New-AzDataBoxEdgeTrigger** konfiguruje wyzwalacz na urządzeniu z danymi na krawędziach pola danych.</span><span class="sxs-lookup"><span data-stu-id="b154a-110">The **New-AzDataBoxEdgeTrigger** cmdlet configures a trigger on the Data Box Edge device.</span></span> 

## <span data-ttu-id="b154a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b154a-111">EXAMPLES</span></span>

### <span data-ttu-id="b154a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b154a-112">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="b154a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b154a-113">PARAMETERS</span></span>

### <span data-ttu-id="b154a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b154a-114">-AsJob</span></span>
<span data-ttu-id="b154a-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b154a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b154a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b154a-116">-DefaultProfile</span></span>
<span data-ttu-id="b154a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b154a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b154a-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b154a-118">-DeviceName</span></span>
<span data-ttu-id="b154a-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="b154a-119">Device Name</span></span>

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

### <span data-ttu-id="b154a-120">-FileEvent</span><span class="sxs-lookup"><span data-stu-id="b154a-120">-FileEvent</span></span>
<span data-ttu-id="b154a-121">Przekaż ten parametr przełącznika, aby skonfigurować wyzwalacz FileEvent</span><span class="sxs-lookup"><span data-stu-id="b154a-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

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

### <span data-ttu-id="b154a-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b154a-122">-Name</span></span>
<span data-ttu-id="b154a-123">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="b154a-123">Resource Name</span></span>

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

### <span data-ttu-id="b154a-124">-PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="b154a-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="b154a-125">Przekaż ten parametr przełącznika, aby skonfigurować wyzwalacz PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="b154a-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

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

### <span data-ttu-id="b154a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b154a-126">-ResourceGroupName</span></span>
<span data-ttu-id="b154a-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b154a-127">Resource Group Name</span></span>

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

### <span data-ttu-id="b154a-128">-Rolename</span><span class="sxs-lookup"><span data-stu-id="b154a-128">-RoleName</span></span>
<span data-ttu-id="b154a-129">Rola obliczeniowa, na podstawie której zostaną podwyższone zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="b154a-129">Compute role against which events will be raised.</span></span>

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

### <span data-ttu-id="b154a-130">-Schedule</span><span class="sxs-lookup"><span data-stu-id="b154a-130">-Schedule</span></span>
<span data-ttu-id="b154a-131">Częstotliwość okresowa, przy której zdarzenie timer musi zostać podwyższone.</span><span class="sxs-lookup"><span data-stu-id="b154a-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="b154a-132">Określ harmonogram w dniach (od 1 do 365), godzin (od 1 do 23) lub minut (od 1 do 59).</span><span class="sxs-lookup"><span data-stu-id="b154a-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

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

### <span data-ttu-id="b154a-133">-ShareId</span><span class="sxs-lookup"><span data-stu-id="b154a-133">-ShareId</span></span>
<span data-ttu-id="b154a-134">Identyfikator udziału pliku, który ma zostać przekazany w wyzwalaczu FileEvent</span><span class="sxs-lookup"><span data-stu-id="b154a-134">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="b154a-135">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="b154a-135">-ShareName</span></span>
<span data-ttu-id="b154a-136">Identyfikator udziału pliku, który ma zostać przekazany w wyzwalaczu FileEvent</span><span class="sxs-lookup"><span data-stu-id="b154a-136">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="b154a-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b154a-137">-StartTime</span></span>
<span data-ttu-id="b154a-138">Godzina, w której powstaje prawidłowy wyzwalacz.</span><span class="sxs-lookup"><span data-stu-id="b154a-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="b154a-139">Harmonogram jest obliczany w odniesieniu do czasu określonego w sekundach.</span><span class="sxs-lookup"><span data-stu-id="b154a-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="b154a-140">Jeśli nie określono strefy czasowej, czas będzie uznawany za "strefę czasową urządzenia".</span><span class="sxs-lookup"><span data-stu-id="b154a-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="b154a-141">Wartość będzie zawsze zwracana jako czas UTC.</span><span class="sxs-lookup"><span data-stu-id="b154a-141">The value will always be returned as UTC time.</span></span>

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

### <span data-ttu-id="b154a-142">— Temat</span><span class="sxs-lookup"><span data-stu-id="b154a-142">-Topic</span></span>
<span data-ttu-id="b154a-143">Temat, w którym zdarzenia okresowe są publikowane na urządzeniu IoT.</span><span class="sxs-lookup"><span data-stu-id="b154a-143">Topic where periodic events are published to IoT device.</span></span>

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

### <span data-ttu-id="b154a-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b154a-144">-Confirm</span></span>
<span data-ttu-id="b154a-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b154a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b154a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b154a-146">-WhatIf</span></span>
<span data-ttu-id="b154a-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b154a-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b154a-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b154a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b154a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b154a-149">CommonParameters</span></span>
<span data-ttu-id="b154a-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b154a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b154a-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b154a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b154a-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b154a-152">INPUTS</span></span>

### <span data-ttu-id="b154a-153">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b154a-153">None</span></span>

## <span data-ttu-id="b154a-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b154a-154">OUTPUTS</span></span>

### <span data-ttu-id="b154a-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="b154a-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="b154a-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b154a-156">NOTES</span></span>

## <span data-ttu-id="b154a-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b154a-157">RELATED LINKS</span></span>

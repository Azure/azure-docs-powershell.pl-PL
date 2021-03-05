---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
ms.openlocfilehash: b761422a3a2c81d1070dbc5852ca67e2ac91117c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980362"
---
# <span data-ttu-id="9d232-101">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9d232-101">Add-AzAutoscaleSetting</span></span>

## <span data-ttu-id="9d232-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d232-102">SYNOPSIS</span></span>
<span data-ttu-id="9d232-103">Tworzy ustawienie skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="9d232-103">Creates an Autoscale setting.</span></span>

## <span data-ttu-id="9d232-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9d232-104">SYNTAX</span></span>

### <span data-ttu-id="9d232-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9d232-105">UpdateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d232-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9d232-106">CreateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d232-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9d232-107">DESCRIPTION</span></span>
<span data-ttu-id="9d232-108">Polecenie **cmdlet Add-AzAutoscaleSetting** tworzy ustawienie skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="9d232-108">The **Add-AzAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="9d232-109">To polecenie cmdlet implementuje wzorzec ShouldProcess, czyli może wymagać potwierdzenia od użytkownika przed utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="9d232-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="9d232-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9d232-110">EXAMPLES</span></span>

### <span data-ttu-id="9d232-111">Przykład 1. Tworzenie ustawienia automatycznego skalowania</span><span class="sxs-lookup"><span data-stu-id="9d232-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfile $Profile1, $Profile2
```

<span data-ttu-id="9d232-112">Pierwsze dwa polecenia używają polecenia [New-AzAutoscaleRule](https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscalerule) w celu utworzenia dwóch reguł skalowania automatycznego: $Rule 1 i $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="9d232-112">The first two commands use [New-AzAutoscaleRule](https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscalerule) to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="9d232-113">Trzecie i czwarte polecenia używają funkcji [New-AzAutoscaleProfile](https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscaleprofile) do tworzenia profilów autoskalowania, $Profile 1 i $Profile 2 przy użyciu $Rule 1 i $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="9d232-113">The third and fourth commands use [New-AzAutoscaleProfile](https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscaleprofile) to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="9d232-114">Ostatnie polecenie umożliwia utworzenie ustawienia skalowania automatycznego przy użyciu profilów w $Profile 1 i $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="9d232-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="9d232-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d232-115">PARAMETERS</span></span>

### <span data-ttu-id="9d232-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="9d232-116">-AutoscaleProfile</span></span>
<span data-ttu-id="9d232-117">Określa listę profilów do dodania do ustawienia skalowania automatycznego lub $Null, aby nie dodawać profilu.</span><span class="sxs-lookup"><span data-stu-id="9d232-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d232-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d232-118">-DefaultProfile</span></span>
<span data-ttu-id="9d232-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="9d232-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d232-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="9d232-120">-DisableSetting</span></span>
<span data-ttu-id="9d232-121">Wyłącza istniejące ustawienie automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="9d232-121">Disables an existing Autoscale setting.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d232-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d232-122">-InputObject</span></span>
<span data-ttu-id="9d232-123">Pełna specyfikacja ustawienia autoskalowania</span><span class="sxs-lookup"><span data-stu-id="9d232-123">The complete spec of an AutoscaleSetting</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting
Parameter Sets: UpdateAutoscaleSetting
Aliases: SettingSpec

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d232-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9d232-124">-Location</span></span>
<span data-ttu-id="9d232-125">Określa położenie ustawienia autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="9d232-125">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d232-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9d232-126">-Name</span></span>
<span data-ttu-id="9d232-127">Określa nazwę ustawienia skalowania automatycznego do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="9d232-127">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d232-128">— Powiadomienie</span><span class="sxs-lookup"><span data-stu-id="9d232-128">-Notification</span></span>
<span data-ttu-id="9d232-129">Określa listę powiadomień rozdzielanych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="9d232-129">Specifies a list of comma-separated notifications.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d232-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d232-130">-ResourceGroupName</span></span>
<span data-ttu-id="9d232-131">Określa nazwę grupy zasobów dla zasobu skojarzonego z ustawieniem skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="9d232-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d232-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="9d232-132">-TargetResourceId</span></span>
<span data-ttu-id="9d232-133">Określa identyfikator zasobu do automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="9d232-133">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d232-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9d232-134">-Confirm</span></span>
<span data-ttu-id="9d232-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9d232-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d232-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d232-136">-WhatIf</span></span>
<span data-ttu-id="9d232-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d232-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d232-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9d232-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d232-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d232-139">CommonParameters</span></span>
<span data-ttu-id="9d232-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d232-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d232-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d232-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d232-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d232-142">INPUTS</span></span>

### <span data-ttu-id="9d232-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9d232-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="9d232-144">System.String</span><span class="sxs-lookup"><span data-stu-id="9d232-144">System.String</span></span>

### <span data-ttu-id="9d232-145">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="9d232-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9d232-146">System.Collections.generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlet.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="9d232-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9d232-147">System.Collections.generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlet.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="9d232-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9d232-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d232-148">OUTPUTS</span></span>

### <span data-ttu-id="9d232-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9d232-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="9d232-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9d232-150">NOTES</span></span>

## <span data-ttu-id="9d232-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d232-151">RELATED LINKS</span></span>

[<span data-ttu-id="9d232-152">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9d232-152">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="9d232-153">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="9d232-153">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="9d232-154">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="9d232-154">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="9d232-155">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9d232-155">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)



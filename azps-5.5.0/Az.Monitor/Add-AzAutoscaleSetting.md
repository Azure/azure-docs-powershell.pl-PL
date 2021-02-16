---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
ms.openlocfilehash: b2f7410f45a5b60a768d22fe7e66b7d8c1e4ad94
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184995"
---
# <span data-ttu-id="4cea3-101">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="4cea3-101">Add-AzAutoscaleSetting</span></span>

## <span data-ttu-id="4cea3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cea3-102">SYNOPSIS</span></span>
<span data-ttu-id="4cea3-103">Tworzy ustawienie skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="4cea3-103">Creates an Autoscale setting.</span></span>

## <span data-ttu-id="4cea3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4cea3-104">SYNTAX</span></span>

### <span data-ttu-id="4cea3-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="4cea3-105">UpdateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cea3-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="4cea3-106">CreateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cea3-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="4cea3-107">DESCRIPTION</span></span>
<span data-ttu-id="4cea3-108">Polecenie **cmdlet Add-AzAutoscaleSetting** tworzy ustawienie autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="4cea3-108">The **Add-AzAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="4cea3-109">To polecenie cmdlet implementuje wzorzec ShouldProcess, czyli może wymagać potwierdzenia od użytkownika przed utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="4cea3-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="4cea3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4cea3-110">EXAMPLES</span></span>

### <span data-ttu-id="4cea3-111">Przykład 1. Tworzenie ustawienia automatycznego skalowania</span><span class="sxs-lookup"><span data-stu-id="4cea3-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfile $Profile1, $Profile2
```

<span data-ttu-id="4cea3-112">Pierwsze dwa polecenia używają polecenia [New-AzAutoscaleRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule) w celu utworzenia dwóch reguł skalowania automatycznego: $Rule 1 i $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="4cea3-112">The first two commands use [New-AzAutoscaleRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule) to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="4cea3-113">Trzecie i czwarte polecenia używają funkcji [New-AzAutoscaleProfile](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile) do tworzenia profilów autoskalowania, $Profile 1 i $Profile 2 przy użyciu $Rule 1 i $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="4cea3-113">The third and fourth commands use [New-AzAutoscaleProfile](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile) to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="4cea3-114">Ostatnie polecenie umożliwia utworzenie ustawienia skalowania automatycznego przy użyciu profilów w $Profile 1 i $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="4cea3-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="4cea3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cea3-115">PARAMETERS</span></span>

### <span data-ttu-id="4cea3-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="4cea3-116">-AutoscaleProfile</span></span>
<span data-ttu-id="4cea3-117">Określa listę profilów do dodania do ustawienia skalowania automatycznego lub $Null, aby nie dodawać profilu.</span><span class="sxs-lookup"><span data-stu-id="4cea3-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

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

### <span data-ttu-id="4cea3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cea3-118">-DefaultProfile</span></span>
<span data-ttu-id="4cea3-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="4cea3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cea3-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="4cea3-120">-DisableSetting</span></span>
<span data-ttu-id="4cea3-121">Wyłącza istniejące ustawienie skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="4cea3-121">Disables an existing Autoscale setting.</span></span>

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

### <span data-ttu-id="4cea3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cea3-122">-InputObject</span></span>
<span data-ttu-id="4cea3-123">Pełna specyfikacja ustawienia autoskalowania</span><span class="sxs-lookup"><span data-stu-id="4cea3-123">The complete spec of an AutoscaleSetting</span></span>

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

### <span data-ttu-id="4cea3-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4cea3-124">-Location</span></span>
<span data-ttu-id="4cea3-125">Określa położenie ustawienia autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="4cea3-125">Specifies the location of the Autoscale setting.</span></span>

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

### <span data-ttu-id="4cea3-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4cea3-126">-Name</span></span>
<span data-ttu-id="4cea3-127">Określa nazwę ustawienia skalowania automatycznego do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="4cea3-127">Specifies the name of the Autoscale setting to create.</span></span>

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

### <span data-ttu-id="4cea3-128">— Powiadomienie</span><span class="sxs-lookup"><span data-stu-id="4cea3-128">-Notification</span></span>
<span data-ttu-id="4cea3-129">Określa listę powiadomień rozdzielanych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="4cea3-129">Specifies a list of comma-separated notifications.</span></span>

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

### <span data-ttu-id="4cea3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cea3-130">-ResourceGroupName</span></span>
<span data-ttu-id="4cea3-131">Określa nazwę grupy zasobów dla zasobu skojarzonego z ustawieniem Skala automatyczna.</span><span class="sxs-lookup"><span data-stu-id="4cea3-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

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

### <span data-ttu-id="4cea3-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4cea3-132">-TargetResourceId</span></span>
<span data-ttu-id="4cea3-133">Określa identyfikator zasobu do automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="4cea3-133">Specifies the ID of the resource to autoscale.</span></span>

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

### <span data-ttu-id="4cea3-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4cea3-134">-Confirm</span></span>
<span data-ttu-id="4cea3-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4cea3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cea3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cea3-136">-WhatIf</span></span>
<span data-ttu-id="4cea3-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cea3-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4cea3-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4cea3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cea3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cea3-139">CommonParameters</span></span>
<span data-ttu-id="4cea3-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cea3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cea3-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4cea3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cea3-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cea3-142">INPUTS</span></span>

### <span data-ttu-id="4cea3-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="4cea3-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="4cea3-144">System.String</span><span class="sxs-lookup"><span data-stu-id="4cea3-144">System.String</span></span>

### <span data-ttu-id="4cea3-145">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="4cea3-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4cea3-146">System.Collections.generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlet.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="4cea3-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4cea3-147">System.Collections.generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlet.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="4cea3-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4cea3-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4cea3-148">OUTPUTS</span></span>

### <span data-ttu-id="4cea3-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4cea3-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="4cea3-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4cea3-150">NOTES</span></span>

## <span data-ttu-id="4cea3-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cea3-151">RELATED LINKS</span></span>

[<span data-ttu-id="4cea3-152">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="4cea3-152">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="4cea3-153">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="4cea3-153">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="4cea3-154">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="4cea3-154">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="4cea3-155">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="4cea3-155">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
ms.openlocfilehash: b2f7410f45a5b60a768d22fe7e66b7d8c1e4ad94
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231763"
---
# <span data-ttu-id="76746-101">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="76746-101">Add-AzAutoscaleSetting</span></span>

## <span data-ttu-id="76746-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76746-102">SYNOPSIS</span></span>
<span data-ttu-id="76746-103">Umożliwia utworzenie ustawienia skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="76746-103">Creates an Autoscale setting.</span></span>

## <span data-ttu-id="76746-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76746-104">SYNTAX</span></span>

### <span data-ttu-id="76746-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="76746-105">UpdateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76746-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="76746-106">CreateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76746-107">Opis</span><span class="sxs-lookup"><span data-stu-id="76746-107">DESCRIPTION</span></span>
<span data-ttu-id="76746-108">Polecenie cmdlet **Add-AzAutoscaleSetting** powoduje utworzenie ustawienia skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="76746-108">The **Add-AzAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="76746-109">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="76746-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="76746-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76746-110">EXAMPLES</span></span>

### <span data-ttu-id="76746-111">Przykład 1. Tworzenie ustawienia skalowania automatycznego</span><span class="sxs-lookup"><span data-stu-id="76746-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfile $Profile1, $Profile2
```

<span data-ttu-id="76746-112">W dwóch pierwszych poleceniach użyto poleceń [New-AzAutoscaleRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule) w celu utworzenia dwóch reguł autoskalowania $Rule 1 i $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="76746-112">The first two commands use [New-AzAutoscaleRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule) to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="76746-113">W trzecim i czwartym menu są tworzone profile autoskalowania $Profile [AzAutoscaleProfile](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile) 1 i $profile 2, przy użyciu $Rule 1 i $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="76746-113">The third and fourth commands use [New-AzAutoscaleProfile](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile) to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="76746-114">Polecenie ostatnie powoduje utworzenie ustawienia skalowania automatycznego przy użyciu profilów w $Profile 1 i $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="76746-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="76746-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76746-115">PARAMETERS</span></span>

### <span data-ttu-id="76746-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="76746-116">-AutoscaleProfile</span></span>
<span data-ttu-id="76746-117">Określa listę profilów, które mają zostać dodane do ustawienia skalowania automatycznego, lub $Null, aby dodać pozycję bez profilu.</span><span class="sxs-lookup"><span data-stu-id="76746-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

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

### <span data-ttu-id="76746-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76746-118">-DefaultProfile</span></span>
<span data-ttu-id="76746-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="76746-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76746-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="76746-120">-DisableSetting</span></span>
<span data-ttu-id="76746-121">Wyłącza istniejące ustawienie skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="76746-121">Disables an existing Autoscale setting.</span></span>

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

### <span data-ttu-id="76746-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="76746-122">-InputObject</span></span>
<span data-ttu-id="76746-123">Kompletna Specyfikacja AutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="76746-123">The complete spec of an AutoscaleSetting</span></span>

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

### <span data-ttu-id="76746-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="76746-124">-Location</span></span>
<span data-ttu-id="76746-125">Określa lokalizację ustawienia skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="76746-125">Specifies the location of the Autoscale setting.</span></span>

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

### <span data-ttu-id="76746-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="76746-126">-Name</span></span>
<span data-ttu-id="76746-127">Określa nazwę ustawienia skalowania automatycznego, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="76746-127">Specifies the name of the Autoscale setting to create.</span></span>

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

### <span data-ttu-id="76746-128">-Powiadomienie</span><span class="sxs-lookup"><span data-stu-id="76746-128">-Notification</span></span>
<span data-ttu-id="76746-129">Określa listę oddzielonych przecinkami powiadomień.</span><span class="sxs-lookup"><span data-stu-id="76746-129">Specifies a list of comma-separated notifications.</span></span>

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

### <span data-ttu-id="76746-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76746-130">-ResourceGroupName</span></span>
<span data-ttu-id="76746-131">Określa nazwę grupy zasobów dla zasobu skojarzonego z ustawieniem skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="76746-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

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

### <span data-ttu-id="76746-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="76746-132">-TargetResourceId</span></span>
<span data-ttu-id="76746-133">Określa identyfikator zasobu do automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="76746-133">Specifies the ID of the resource to autoscale.</span></span>

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

### <span data-ttu-id="76746-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="76746-134">-Confirm</span></span>
<span data-ttu-id="76746-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76746-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76746-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76746-136">-WhatIf</span></span>
<span data-ttu-id="76746-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76746-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76746-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="76746-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76746-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76746-139">CommonParameters</span></span>
<span data-ttu-id="76746-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76746-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76746-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76746-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76746-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76746-142">INPUTS</span></span>

### <span data-ttu-id="76746-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="76746-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="76746-144">System. String</span><span class="sxs-lookup"><span data-stu-id="76746-144">System.String</span></span>

### <span data-ttu-id="76746-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="76746-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="76746-146">System. Collections. Generic. list "1 [[Microsoft. Azure. Management. Monitor. Management.. AutoscaleProfile; Microsoft. Azure. PowerShell. cmdlets.</span><span class="sxs-lookup"><span data-stu-id="76746-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="76746-147">System. Collections. Generic. list "1 [[Microsoft. Azure. Management. Monitor. Management.. AutoscaleNotification; Microsoft. Azure. PowerShell. cmdlets.</span><span class="sxs-lookup"><span data-stu-id="76746-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="76746-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76746-148">OUTPUTS</span></span>

### <span data-ttu-id="76746-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="76746-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="76746-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76746-150">NOTES</span></span>

## <span data-ttu-id="76746-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76746-151">RELATED LINKS</span></span>

[<span data-ttu-id="76746-152">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="76746-152">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="76746-153">Nowe — AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="76746-153">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="76746-154">Nowe — AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="76746-154">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="76746-155">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="76746-155">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)



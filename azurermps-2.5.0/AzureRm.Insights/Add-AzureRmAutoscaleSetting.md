---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermautoscalesetting
schema: 2.0.0
ms.openlocfilehash: 8025c68c7fcaf2e7757cc81718636785bd62a19b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899346"
---
# <span data-ttu-id="2dc14-101">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="2dc14-101">Add-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="2dc14-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2dc14-102">SYNOPSIS</span></span>
<span data-ttu-id="2dc14-103">Umożliwia utworzenie ustawienia skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="2dc14-103">Creates an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dc14-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2dc14-104">SYNTAX</span></span>

### <span data-ttu-id="2dc14-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="2dc14-105">UpdateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dc14-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="2dc14-106">CreateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dc14-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2dc14-107">DESCRIPTION</span></span>
<span data-ttu-id="2dc14-108">Polecenie cmdlet **Add-AzureRmAutoscaleSetting** powoduje utworzenie ustawienia skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="2dc14-108">The **Add-AzureRmAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="2dc14-109">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="2dc14-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="2dc14-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2dc14-110">EXAMPLES</span></span>

### <span data-ttu-id="2dc14-111">Przykład 1. Tworzenie ustawienia skalowania automatycznego</span><span class="sxs-lookup"><span data-stu-id="2dc14-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

<span data-ttu-id="2dc14-112">Dwa pierwsze polecenia używają New-AzureRmAutoscaleRule do tworzenia dwóch reguł autoskalowania $Rule 1 i $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="2dc14-112">The first two commands use New-AzureRmAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="2dc14-113">W przypadku trzeciego i czwartego polecenia za pomocą New-AzureRmAutoscaleProfile utworzyć profile skalowania automatycznego, $Profile 1 i $Profile 2, używając $Rule 1 i $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="2dc14-113">The third and fourth commands use New-AzureRmAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="2dc14-114">Polecenie ostatnie powoduje utworzenie ustawienia skalowania automatycznego przy użyciu profilów w $Profile 1 i $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="2dc14-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="2dc14-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2dc14-115">PARAMETERS</span></span>

### <span data-ttu-id="2dc14-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="2dc14-116">-AutoscaleProfile</span></span>
<span data-ttu-id="2dc14-117">Określa listę profilów, które mają zostać dodane do ustawienia skalowania automatycznego, lub $Null, aby dodać pozycję bez profilu.</span><span class="sxs-lookup"><span data-stu-id="2dc14-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

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

### <span data-ttu-id="2dc14-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dc14-118">-DefaultProfile</span></span>
<span data-ttu-id="2dc14-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2dc14-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dc14-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="2dc14-120">-DisableSetting</span></span>
<span data-ttu-id="2dc14-121">Wyłącza istniejące ustawienie skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="2dc14-121">Disables an existing Autoscale setting.</span></span>

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

### <span data-ttu-id="2dc14-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2dc14-122">-InputObject</span></span>
<span data-ttu-id="2dc14-123">Kompletna Specyfikacja AutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="2dc14-123">The complete spec of an AutoscaleSetting</span></span>

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

### <span data-ttu-id="2dc14-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2dc14-124">-Location</span></span>
<span data-ttu-id="2dc14-125">Określa lokalizację ustawienia skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="2dc14-125">Specifies the location of the Autoscale setting.</span></span>

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

### <span data-ttu-id="2dc14-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2dc14-126">-Name</span></span>
<span data-ttu-id="2dc14-127">Określa nazwę ustawienia skalowania automatycznego, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="2dc14-127">Specifies the name of the Autoscale setting to create.</span></span>

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

### <span data-ttu-id="2dc14-128">-Powiadomienie</span><span class="sxs-lookup"><span data-stu-id="2dc14-128">-Notification</span></span>
<span data-ttu-id="2dc14-129">Określa listę oddzielonych przecinkami powiadomień.</span><span class="sxs-lookup"><span data-stu-id="2dc14-129">Specifies a list of comma-separated notifications.</span></span>

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

### <span data-ttu-id="2dc14-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dc14-130">-ResourceGroupName</span></span>
<span data-ttu-id="2dc14-131">Określa nazwę grupy zasobów dla zasobu skojarzonego z ustawieniem skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="2dc14-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

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

### <span data-ttu-id="2dc14-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="2dc14-132">-TargetResourceId</span></span>
<span data-ttu-id="2dc14-133">Określa identyfikator zasobu do automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="2dc14-133">Specifies the ID of the resource to autoscale.</span></span>

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

### <span data-ttu-id="2dc14-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2dc14-134">-Confirm</span></span>
<span data-ttu-id="2dc14-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dc14-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dc14-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dc14-136">-WhatIf</span></span>
<span data-ttu-id="2dc14-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dc14-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2dc14-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2dc14-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dc14-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dc14-139">CommonParameters</span></span>
<span data-ttu-id="2dc14-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dc14-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dc14-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dc14-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dc14-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2dc14-142">INPUTS</span></span>

### <span data-ttu-id="2dc14-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="2dc14-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="2dc14-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2dc14-144">System.String</span></span>

### <span data-ttu-id="2dc14-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2dc14-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2dc14-146">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Monitor. Management. model. AutoscaleProfile; Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2dc14-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="2dc14-147">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Monitor. Management. model. AutoscaleNotification; Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2dc14-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2dc14-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2dc14-148">OUTPUTS</span></span>

### <span data-ttu-id="2dc14-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2dc14-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="2dc14-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2dc14-150">NOTES</span></span>

## <span data-ttu-id="2dc14-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2dc14-151">RELATED LINKS</span></span>

[<span data-ttu-id="2dc14-152">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="2dc14-152">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="2dc14-153">Nowe — AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="2dc14-153">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="2dc14-154">Nowe — AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="2dc14-154">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="2dc14-155">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="2dc14-155">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)



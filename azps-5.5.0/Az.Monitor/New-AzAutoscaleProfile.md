---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
ms.openlocfilehash: f857f578ab3f0b8baacd0c5d392659ac09b0790f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203475"
---
# <span data-ttu-id="4b9ec-101">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="4b9ec-101">New-AzAutoscaleProfile</span></span>

## <span data-ttu-id="4b9ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b9ec-102">SYNOPSIS</span></span>
<span data-ttu-id="4b9ec-103">Tworzy profil autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-103">Creates an Autoscale profile.</span></span>

## <span data-ttu-id="4b9ec-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4b9ec-104">SYNTAX</span></span>

### <span data-ttu-id="4b9ec-105">CreateWithoutScheduledTimes</span><span class="sxs-lookup"><span data-stu-id="4b9ec-105">CreateWithoutScheduledTimes</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b9ec-106">CreateWithFixedDateScheduling</span><span class="sxs-lookup"><span data-stu-id="4b9ec-106">CreateWithFixedDateScheduling</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b9ec-107">CreateUsingRecurrentScheduling</span><span class="sxs-lookup"><span data-stu-id="4b9ec-107">CreateUsingRecurrentScheduling</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDay <System.Collections.Generic.List`1[System.String]>
 -ScheduleHour <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinute <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b9ec-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4b9ec-108">DESCRIPTION</span></span>
<span data-ttu-id="4b9ec-109">Polecenie **cmdlet New-AzAutoscaleProfile** tworzy profil autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-109">The **New-AzAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="4b9ec-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4b9ec-110">EXAMPLES</span></span>

### <span data-ttu-id="4b9ec-111">Przykład 1. Tworzenie jednego profilu ze stałą datą</span><span class="sxs-lookup"><span data-stu-id="4b9ec-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="4b9ec-112">Pierwsze polecenie tworzy regułę automatycznego skalowania o nazwie Żądania, a następnie zapisuje ją w $Rule zmienną.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="4b9ec-113">Drugie polecenie tworzy profil o nazwie Profile01 o stałej dacie przy użyciu reguły w $Rule.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="4b9ec-114">Przykład 2. Tworzenie profilu z harmonogramem</span><span class="sxs-lookup"><span data-stu-id="4b9ec-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="4b9ec-115">Pierwsze polecenie tworzy regułę skalowania automatycznego o nazwie Żądania, a następnie zapisuje ją w $Rule zmienną.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="4b9ec-116">Drugie polecenie tworzy profil o nazwie SecondProfileName z harmonogramem cyklicznym przy użyciu reguły w $Rule.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="4b9ec-117">Przykład 3. Tworzenie profilów z dwiema regułami</span><span class="sxs-lookup"><span data-stu-id="4b9ec-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDay "1" -ScheduleHour 5 -ScheduleMinute 15 -ScheduleTimeZone UTC
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : profileName
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="4b9ec-118">Pierwsze dwa polecenia tworzą reguły i przechowują je w zmiennych, $Rule 1 i $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>
<span data-ttu-id="4b9ec-119">Trzecie polecenie tworzy profil o nazwie ProfileName przy użyciu reguł z reguły 1 i 2, a następnie zapisuje go w zmiennej $Profile 1.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>
<span data-ttu-id="4b9ec-120">Ostatnie polecenie tworzy profil o nazwie SecondProfileName przy użyciu reguł z reguły 1 i 2, a następnie zapisuje go w zmiennej $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="4b9ec-121">Przykład 4. Tworzenie profilu bez harmonogramu i ustalonej daty</span><span class="sxs-lookup"><span data-stu-id="4b9ec-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "ProfileName"
```

<span data-ttu-id="4b9ec-122">Pierwsze polecenie tworzy regułę automatycznego skalowania o nazwie Żądania, a następnie zapisuje ją w $Rule zmienną.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="4b9ec-123">Drugie polecenie tworzy profil bez harmonogramu lub ustalonej daty, a następnie zapisuje go w $Profile danych.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="4b9ec-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b9ec-124">PARAMETERS</span></span>

### <span data-ttu-id="4b9ec-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="4b9ec-125">-DefaultCapacity</span></span>
<span data-ttu-id="4b9ec-126">Określa domyślną pojemność.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-126">Specifies the default capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b9ec-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b9ec-127">-DefaultProfile</span></span>
<span data-ttu-id="4b9ec-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="4b9ec-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b9ec-129">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="4b9ec-129">-EndTimeWindow</span></span>
<span data-ttu-id="4b9ec-130">Określa koniec okna czasu.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-130">Specifies the end of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b9ec-131">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="4b9ec-131">-MaximumCapacity</span></span>
<span data-ttu-id="4b9ec-132">Określa maksymalną wydajność.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-132">Specifies the maximum capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b9ec-133">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="4b9ec-133">-MinimumCapacity</span></span>
<span data-ttu-id="4b9ec-134">Określa minimalną wydajność.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-134">Specifies the minimum capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b9ec-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4b9ec-135">-Name</span></span>
<span data-ttu-id="4b9ec-136">Określa nazwę profilu do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-136">Specifies the name of the profile to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b9ec-137">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="4b9ec-137">-RecurrenceFrequency</span></span>
<span data-ttu-id="4b9ec-138">Określa częstotliwość cyklu.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-138">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="4b9ec-139">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4b9ec-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4b9ec-140">Brak</span><span class="sxs-lookup"><span data-stu-id="4b9ec-140">None</span></span>
- <span data-ttu-id="4b9ec-141">Sekunda</span><span class="sxs-lookup"><span data-stu-id="4b9ec-141">Second</span></span>
- <span data-ttu-id="4b9ec-142">Minuta</span><span class="sxs-lookup"><span data-stu-id="4b9ec-142">Minute</span></span>
- <span data-ttu-id="4b9ec-143">Godzina</span><span class="sxs-lookup"><span data-stu-id="4b9ec-143">Hour</span></span>
- <span data-ttu-id="4b9ec-144">Dzień</span><span class="sxs-lookup"><span data-stu-id="4b9ec-144">Day</span></span>
- <span data-ttu-id="4b9ec-145">Tydzień</span><span class="sxs-lookup"><span data-stu-id="4b9ec-145">Week</span></span>
- <span data-ttu-id="4b9ec-146">Miesiąc</span><span class="sxs-lookup"><span data-stu-id="4b9ec-146">Month</span></span>
- <span data-ttu-id="4b9ec-147">Rok Nie wszystkie te wartości są obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-147">Year Not all of these values are supported.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b9ec-148">— reguła</span><span class="sxs-lookup"><span data-stu-id="4b9ec-148">-Rule</span></span>
<span data-ttu-id="4b9ec-149">Określa listę reguł do dodania do profilu.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-149">Specifies the list of rules to add to the profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b9ec-150">-ScheduleDay</span><span class="sxs-lookup"><span data-stu-id="4b9ec-150">-ScheduleDay</span></span>
<span data-ttu-id="4b9ec-151">Określa zaplanowane dni.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-151">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b9ec-152">-ScheduleHour</span><span class="sxs-lookup"><span data-stu-id="4b9ec-152">-ScheduleHour</span></span>
<span data-ttu-id="4b9ec-153">Określa zaplanowane godziny.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-153">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b9ec-154">-ScheduleMinute</span><span class="sxs-lookup"><span data-stu-id="4b9ec-154">-ScheduleMinute</span></span>
<span data-ttu-id="4b9ec-155">Określa zaplanowane minuty.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-155">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b9ec-156">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="4b9ec-156">-ScheduleTimeZone</span></span>
<span data-ttu-id="4b9ec-157">Określa strefę czasową harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-157">Specifies the time zone of the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b9ec-158">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="4b9ec-158">-StartTimeWindow</span></span>
<span data-ttu-id="4b9ec-159">Określa początek okna czasu.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-159">Specifies the start of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b9ec-160">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="4b9ec-160">-TimeWindowTimeZone</span></span>
<span data-ttu-id="4b9ec-161">Określa strefę czasową w oknie czasowym.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-161">Specifies the time zone of the time window.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b9ec-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b9ec-162">CommonParameters</span></span>
<span data-ttu-id="4b9ec-163">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b9ec-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b9ec-164">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b9ec-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b9ec-165">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b9ec-165">INPUTS</span></span>

### <span data-ttu-id="4b9ec-166">System.String</span><span class="sxs-lookup"><span data-stu-id="4b9ec-166">System.String</span></span>

### <span data-ttu-id="4b9ec-167">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="4b9ec-167">System.DateTime</span></span>

### <span data-ttu-id="4b9ec-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="4b9ec-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span></span>

### <span data-ttu-id="4b9ec-169">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4b9ec-169">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4b9ec-170">System.Collections.Generic.List `1[[System.Nullable` 1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]], System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4b9ec-170">System.Collections.Generic.List`1[[System.Nullable`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]], System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4b9ec-171">System.Collections.generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.PowerShell.Cmdlet.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="4b9ec-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4b9ec-172">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b9ec-172">OUTPUTS</span></span>

### <span data-ttu-id="4b9ec-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="4b9ec-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="4b9ec-174">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4b9ec-174">NOTES</span></span>

## <span data-ttu-id="4b9ec-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b9ec-175">RELATED LINKS</span></span>

[<span data-ttu-id="4b9ec-176">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="4b9ec-176">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="4b9ec-177">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="4b9ec-177">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="4b9ec-178">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="4b9ec-178">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="4b9ec-179">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="4b9ec-179">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="4b9ec-180">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="4b9ec-180">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)



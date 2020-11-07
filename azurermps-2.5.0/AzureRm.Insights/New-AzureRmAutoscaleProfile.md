---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscaleprofile
schema: 2.0.0
ms.openlocfilehash: 2192a03713b82e49f1958a34678353856197b3a6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899327"
---
# <span data-ttu-id="bcca6-101">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="bcca6-101">New-AzureRmAutoscaleProfile</span></span>

## <span data-ttu-id="bcca6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bcca6-102">SYNOPSIS</span></span>
<span data-ttu-id="bcca6-103">Tworzy profil autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="bcca6-103">Creates an Autoscale profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcca6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bcca6-104">SYNTAX</span></span>

### <span data-ttu-id="bcca6-105">CreateWithoutScheduledTimes</span><span class="sxs-lookup"><span data-stu-id="bcca6-105">CreateWithoutScheduledTimes</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcca6-106">CreateWithFixedDateScheduling</span><span class="sxs-lookup"><span data-stu-id="bcca6-106">CreateWithFixedDateScheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcca6-107">CreateUsingRecurrentScheduling</span><span class="sxs-lookup"><span data-stu-id="bcca6-107">CreateUsingRecurrentScheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDay <System.Collections.Generic.List`1[System.String]>
 -ScheduleHour <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinute <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcca6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bcca6-108">DESCRIPTION</span></span>
<span data-ttu-id="bcca6-109">Polecenie cmdlet **New-AzureRmAutoscaleProfile** tworzy profil skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="bcca6-109">The **New-AzureRmAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="bcca6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bcca6-110">EXAMPLES</span></span>

### <span data-ttu-id="bcca6-111">Przykład 1. Tworzenie pojedynczego profilu ze stałą datą</span><span class="sxs-lookup"><span data-stu-id="bcca6-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="bcca6-112">Pierwsze polecenie powoduje utworzenie reguły autoskalowania o nazwie żądania, a następnie zapisanie jej w zmiennej $Rule.</span><span class="sxs-lookup"><span data-stu-id="bcca6-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="bcca6-113">Drugie polecenie tworzy profil o nazwie Profile01 ze stałą datą przy użyciu reguły w $Rule.</span><span class="sxs-lookup"><span data-stu-id="bcca6-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="bcca6-114">Przykład 2: Tworzenie profilu z harmonogramem</span><span class="sxs-lookup"><span data-stu-id="bcca6-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="bcca6-115">Pierwsze polecenie powoduje utworzenie reguły autoskalowania o nazwie żądania, a następnie zapisanie jej w zmiennej $Rule.</span><span class="sxs-lookup"><span data-stu-id="bcca6-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="bcca6-116">Drugie polecenie tworzy profil o nazwie SecondProfileName z harmonogramem cyklicznym przy użyciu reguły w $Rule.</span><span class="sxs-lookup"><span data-stu-id="bcca6-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="bcca6-117">Przykład 3: Tworzenie profilów przy użyciu dwóch reguł</span><span class="sxs-lookup"><span data-stu-id="bcca6-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDays "1" -ScheduleHours 5 -ScheduleMinutes 15 -ScheduleTimeZone UTC
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

<span data-ttu-id="bcca6-118">Pierwsze dwa polecenia tworzą reguły i przechowują je w zmiennych $Rule odpowiednio 1 i $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="bcca6-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>
<span data-ttu-id="bcca6-119">Trzecia komenda tworzy profil o nazwie nazwa pliku, korzystając z reguł w Rule1 i Rule2, a następnie zapisuje go w zmiennej $Profile 1.</span><span class="sxs-lookup"><span data-stu-id="bcca6-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>
<span data-ttu-id="bcca6-120">Ostatnie polecenie tworzy profil o nazwie SecondProfileName przy użyciu reguł w Rule1 i Rule2, a następnie zapisuje go w zmiennej $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="bcca6-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="bcca6-121">Przykład 4: Tworzenie profilu bez harmonogramu lub ustalonej daty</span><span class="sxs-lookup"><span data-stu-id="bcca6-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "ProfileName"
```

<span data-ttu-id="bcca6-122">Pierwsze polecenie powoduje utworzenie reguły autoskalowania o nazwie żądania, a następnie zapisanie jej w zmiennej $Rule.</span><span class="sxs-lookup"><span data-stu-id="bcca6-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="bcca6-123">Drugie polecenie tworzy profil bez harmonogramu lub ustaloną datę, a następnie zapisuje go w zmiennej $Profile.</span><span class="sxs-lookup"><span data-stu-id="bcca6-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="bcca6-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bcca6-124">PARAMETERS</span></span>

### <span data-ttu-id="bcca6-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="bcca6-125">-DefaultCapacity</span></span>
<span data-ttu-id="bcca6-126">Określa wydajność domyślną.</span><span class="sxs-lookup"><span data-stu-id="bcca6-126">Specifies the default capacity.</span></span>

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

### <span data-ttu-id="bcca6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcca6-127">-DefaultProfile</span></span>
<span data-ttu-id="bcca6-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bcca6-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcca6-129">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="bcca6-129">-EndTimeWindow</span></span>
<span data-ttu-id="bcca6-130">Określa koniec okna czasu.</span><span class="sxs-lookup"><span data-stu-id="bcca6-130">Specifies the end of the time window.</span></span>

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

### <span data-ttu-id="bcca6-131">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="bcca6-131">-MaximumCapacity</span></span>
<span data-ttu-id="bcca6-132">Określa maksymalną wydajność.</span><span class="sxs-lookup"><span data-stu-id="bcca6-132">Specifies the maximum capacity.</span></span>

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

### <span data-ttu-id="bcca6-133">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="bcca6-133">-MinimumCapacity</span></span>
<span data-ttu-id="bcca6-134">Umożliwia określenie minimalnej pojemności.</span><span class="sxs-lookup"><span data-stu-id="bcca6-134">Specifies the minimum capacity.</span></span>

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

### <span data-ttu-id="bcca6-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bcca6-135">-Name</span></span>
<span data-ttu-id="bcca6-136">Określa nazwę profilu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="bcca6-136">Specifies the name of the profile to create.</span></span>

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

### <span data-ttu-id="bcca6-137">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="bcca6-137">-RecurrenceFrequency</span></span>
<span data-ttu-id="bcca6-138">Określa częstotliwość cyklu.</span><span class="sxs-lookup"><span data-stu-id="bcca6-138">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="bcca6-139">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="bcca6-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bcca6-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bcca6-140">None</span></span>
- <span data-ttu-id="bcca6-141">Drugiego</span><span class="sxs-lookup"><span data-stu-id="bcca6-141">Second</span></span>
- <span data-ttu-id="bcca6-142">Minutę</span><span class="sxs-lookup"><span data-stu-id="bcca6-142">Minute</span></span>
- <span data-ttu-id="bcca6-143">Dobow</span><span class="sxs-lookup"><span data-stu-id="bcca6-143">Hour</span></span>
- <span data-ttu-id="bcca6-144">Dniach</span><span class="sxs-lookup"><span data-stu-id="bcca6-144">Day</span></span>
- <span data-ttu-id="bcca6-145">Tygodnia</span><span class="sxs-lookup"><span data-stu-id="bcca6-145">Week</span></span>
- <span data-ttu-id="bcca6-146">Sześciomiesięcznego</span><span class="sxs-lookup"><span data-stu-id="bcca6-146">Month</span></span>
- <span data-ttu-id="bcca6-147">Rok nie wszystkie te wartości są obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="bcca6-147">Year Not all of these values are supported.</span></span>

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

### <span data-ttu-id="bcca6-148">— Reguła</span><span class="sxs-lookup"><span data-stu-id="bcca6-148">-Rule</span></span>
<span data-ttu-id="bcca6-149">Określa listę reguł, które należy dodać do profilu.</span><span class="sxs-lookup"><span data-stu-id="bcca6-149">Specifies the list of rules to add to the profile.</span></span>

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

### <span data-ttu-id="bcca6-150">-ScheduleDay</span><span class="sxs-lookup"><span data-stu-id="bcca6-150">-ScheduleDay</span></span>
<span data-ttu-id="bcca6-151">Określa zaplanowane dni.</span><span class="sxs-lookup"><span data-stu-id="bcca6-151">Specifies the scheduled days.</span></span>

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

### <span data-ttu-id="bcca6-152">-ScheduleHour</span><span class="sxs-lookup"><span data-stu-id="bcca6-152">-ScheduleHour</span></span>
<span data-ttu-id="bcca6-153">Określa zaplanowane godziny.</span><span class="sxs-lookup"><span data-stu-id="bcca6-153">Specifies the scheduled hours.</span></span>

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

### <span data-ttu-id="bcca6-154">-ScheduleMinute</span><span class="sxs-lookup"><span data-stu-id="bcca6-154">-ScheduleMinute</span></span>
<span data-ttu-id="bcca6-155">Określa zaplanowane minuty.</span><span class="sxs-lookup"><span data-stu-id="bcca6-155">Specifies the scheduled minutes.</span></span>

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

### <span data-ttu-id="bcca6-156">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="bcca6-156">-ScheduleTimeZone</span></span>
<span data-ttu-id="bcca6-157">Określa strefę czasową harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="bcca6-157">Specifies the time zone of the schedule.</span></span>

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

### <span data-ttu-id="bcca6-158">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="bcca6-158">-StartTimeWindow</span></span>
<span data-ttu-id="bcca6-159">Określa początek okna czasu.</span><span class="sxs-lookup"><span data-stu-id="bcca6-159">Specifies the start of the time window.</span></span>

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

### <span data-ttu-id="bcca6-160">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="bcca6-160">-TimeWindowTimeZone</span></span>
<span data-ttu-id="bcca6-161">Określa strefę czasową w oknie czasu.</span><span class="sxs-lookup"><span data-stu-id="bcca6-161">Specifies the time zone of the time window.</span></span>

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

### <span data-ttu-id="bcca6-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcca6-162">CommonParameters</span></span>
<span data-ttu-id="bcca6-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcca6-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcca6-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcca6-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcca6-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bcca6-165">INPUTS</span></span>

### <span data-ttu-id="bcca6-166">System. String</span><span class="sxs-lookup"><span data-stu-id="bcca6-166">System.String</span></span>

### <span data-ttu-id="bcca6-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="bcca6-167">System.DateTime</span></span>

### <span data-ttu-id="bcca6-168">Microsoft. Azure. Management. Monitor. Management. models. RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="bcca6-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span></span>

### <span data-ttu-id="bcca6-169">System. Collections. Generic. list "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="bcca6-169">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="bcca6-170">System. Collections. Generic. list `1[[System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]], mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="bcca6-170">System.Collections.Generic.List`1[[System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]], mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="bcca6-171">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Monitor. Management. model. ScaleRule; Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bcca6-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="bcca6-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bcca6-172">OUTPUTS</span></span>

### <span data-ttu-id="bcca6-173">Microsoft. Azure. Management. Monitor. Management. models. AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="bcca6-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="bcca6-174">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bcca6-174">NOTES</span></span>

## <span data-ttu-id="bcca6-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bcca6-175">RELATED LINKS</span></span>

[<span data-ttu-id="bcca6-176">Dodaj-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="bcca6-176">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="bcca6-177">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="bcca6-177">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="bcca6-178">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="bcca6-178">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="bcca6-179">Nowe — AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="bcca6-179">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="bcca6-180">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="bcca6-180">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)



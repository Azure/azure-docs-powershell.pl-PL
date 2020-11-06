---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
ms.openlocfilehash: a5cea42544f2f24ad6c1f1cc1ce64bf122e53440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553307"
---
# <span data-ttu-id="48d53-101">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="48d53-101">New-AzureRmAutoscaleProfile</span></span>

## <span data-ttu-id="48d53-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48d53-102">SYNOPSIS</span></span>
<span data-ttu-id="48d53-103">Tworzy profil autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="48d53-103">Creates an Autoscale profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48d53-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48d53-104">SYNTAX</span></span>

### <span data-ttu-id="48d53-105">Parametry polecenia cmdlet New-AzureRmAutoscaleProfile bez zaplanowanych godzin</span><span class="sxs-lookup"><span data-stu-id="48d53-105">Parameters for New-AzureRmAutoscaleProfile cmdlet without scheduled times</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48d53-106">Parametry polecenia cmdlet New-AzureRmAutoscaleProfile przy użyciu funkcji naprawianie daty planowania</span><span class="sxs-lookup"><span data-stu-id="48d53-106">Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48d53-107">Parametry polecenia cmdlet New-AzureRmAutoscaleProfile przy użyciu harmonogramu ponownego bieżące</span><span class="sxs-lookup"><span data-stu-id="48d53-107">Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDays <System.Collections.Generic.List`1[System.String]>
 -ScheduleHours <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinutes <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48d53-108">Opis</span><span class="sxs-lookup"><span data-stu-id="48d53-108">DESCRIPTION</span></span>
<span data-ttu-id="48d53-109">Polecenie cmdlet **New-AzureRmAutoscaleProfile** tworzy profil skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="48d53-109">The **New-AzureRmAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="48d53-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48d53-110">EXAMPLES</span></span>

### <span data-ttu-id="48d53-111">Przykład 1. Tworzenie pojedynczego profilu ze stałą datą</span><span class="sxs-lookup"><span data-stu-id="48d53-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="48d53-112">Pierwsze polecenie powoduje utworzenie reguły autoskalowania o nazwie żądania, a następnie zapisanie jej w zmiennej $Rule.</span><span class="sxs-lookup"><span data-stu-id="48d53-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="48d53-113">Drugie polecenie tworzy profil o nazwie Profile01 ze stałą datą przy użyciu reguły w $Rule.</span><span class="sxs-lookup"><span data-stu-id="48d53-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="48d53-114">Przykład 2: Tworzenie profilu z harmonogramem</span><span class="sxs-lookup"><span data-stu-id="48d53-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="48d53-115">Pierwsze polecenie powoduje utworzenie reguły autoskalowania o nazwie żądania, a następnie zapisanie jej w zmiennej $Rule.</span><span class="sxs-lookup"><span data-stu-id="48d53-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="48d53-116">Drugie polecenie tworzy profil o nazwie SecondProfileName z harmonogramem cyklicznym przy użyciu reguły w $Rule.</span><span class="sxs-lookup"><span data-stu-id="48d53-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="48d53-117">Przykład 3: Tworzenie profilów przy użyciu dwóch reguł</span><span class="sxs-lookup"><span data-stu-id="48d53-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDays "1" -ScheduleHours 5 -ScheduleMinutes 15 -ScheduleTimeZone UTC
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

<span data-ttu-id="48d53-118">Pierwsze dwa polecenia tworzą reguły i przechowują je w zmiennych $Rule odpowiednio 1 i $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="48d53-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>

<span data-ttu-id="48d53-119">Trzecia komenda tworzy profil o nazwie nazwa pliku, korzystając z reguł w Rule1 i Rule2, a następnie zapisuje go w zmiennej $Profile 1.</span><span class="sxs-lookup"><span data-stu-id="48d53-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>

<span data-ttu-id="48d53-120">Ostatnie polecenie tworzy profil o nazwie SecondProfileName przy użyciu reguł w Rule1 i Rule2, a następnie zapisuje go w zmiennej $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="48d53-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="48d53-121">Przykład 4: Tworzenie profilu bez harmonogramu lub ustalonej daty</span><span class="sxs-lookup"><span data-stu-id="48d53-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "ProfileName"
```

<span data-ttu-id="48d53-122">Pierwsze polecenie powoduje utworzenie reguły autoskalowania o nazwie żądania, a następnie zapisanie jej w zmiennej $Rule.</span><span class="sxs-lookup"><span data-stu-id="48d53-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="48d53-123">Drugie polecenie tworzy profil bez harmonogramu lub ustaloną datę, a następnie zapisuje go w zmiennej $Profile.</span><span class="sxs-lookup"><span data-stu-id="48d53-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="48d53-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48d53-124">PARAMETERS</span></span>

### <span data-ttu-id="48d53-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="48d53-125">-DefaultCapacity</span></span>
<span data-ttu-id="48d53-126">Określa wydajność domyślną.</span><span class="sxs-lookup"><span data-stu-id="48d53-126">Specifies the default capacity.</span></span>

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

### <span data-ttu-id="48d53-127">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="48d53-127">-EndTimeWindow</span></span>
<span data-ttu-id="48d53-128">Określa koniec okna czasu.</span><span class="sxs-lookup"><span data-stu-id="48d53-128">Specifies the end of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48d53-129">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="48d53-129">-MaximumCapacity</span></span>
<span data-ttu-id="48d53-130">Określa maksymalną wydajność.</span><span class="sxs-lookup"><span data-stu-id="48d53-130">Specifies the maximum capacity.</span></span>

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

### <span data-ttu-id="48d53-131">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="48d53-131">-MinimumCapacity</span></span>
<span data-ttu-id="48d53-132">Umożliwia określenie minimalnej pojemności.</span><span class="sxs-lookup"><span data-stu-id="48d53-132">Specifies the minimum capacity.</span></span>

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

### <span data-ttu-id="48d53-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="48d53-133">-Name</span></span>
<span data-ttu-id="48d53-134">Określa nazwę profilu, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="48d53-134">Specifies the name of the profile to create.</span></span>

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

### <span data-ttu-id="48d53-135">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="48d53-135">-RecurrenceFrequency</span></span>
<span data-ttu-id="48d53-136">Określa częstotliwość cyklu.</span><span class="sxs-lookup"><span data-stu-id="48d53-136">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="48d53-137">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="48d53-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="48d53-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="48d53-138">None</span></span>
- <span data-ttu-id="48d53-139">Drugiego</span><span class="sxs-lookup"><span data-stu-id="48d53-139">Second</span></span>
- <span data-ttu-id="48d53-140">Minutę</span><span class="sxs-lookup"><span data-stu-id="48d53-140">Minute</span></span>
- <span data-ttu-id="48d53-141">Dobow</span><span class="sxs-lookup"><span data-stu-id="48d53-141">Hour</span></span>
- <span data-ttu-id="48d53-142">Dniach</span><span class="sxs-lookup"><span data-stu-id="48d53-142">Day</span></span>
- <span data-ttu-id="48d53-143">Tygodnia</span><span class="sxs-lookup"><span data-stu-id="48d53-143">Week</span></span>
- <span data-ttu-id="48d53-144">Sześciomiesięcznego</span><span class="sxs-lookup"><span data-stu-id="48d53-144">Month</span></span>
- <span data-ttu-id="48d53-145">Poprzedniego</span><span class="sxs-lookup"><span data-stu-id="48d53-145">Year</span></span>

<span data-ttu-id="48d53-146">Nie wszystkie te wartości są obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="48d53-146">Not all of these values are supported.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48d53-147">— Reguły</span><span class="sxs-lookup"><span data-stu-id="48d53-147">-Rules</span></span>
<span data-ttu-id="48d53-148">Określa listę reguł, które należy dodać do profilu.</span><span class="sxs-lookup"><span data-stu-id="48d53-148">Specifies the list of rules to add to the profile.</span></span>

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

### <span data-ttu-id="48d53-149">-ScheduleDays</span><span class="sxs-lookup"><span data-stu-id="48d53-149">-ScheduleDays</span></span>
<span data-ttu-id="48d53-150">Określa zaplanowane dni.</span><span class="sxs-lookup"><span data-stu-id="48d53-150">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48d53-151">-ScheduleHours</span><span class="sxs-lookup"><span data-stu-id="48d53-151">-ScheduleHours</span></span>
<span data-ttu-id="48d53-152">Określa zaplanowane godziny.</span><span class="sxs-lookup"><span data-stu-id="48d53-152">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48d53-153">-ScheduleMinutes</span><span class="sxs-lookup"><span data-stu-id="48d53-153">-ScheduleMinutes</span></span>
<span data-ttu-id="48d53-154">Określa zaplanowane minuty.</span><span class="sxs-lookup"><span data-stu-id="48d53-154">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48d53-155">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="48d53-155">-ScheduleTimeZone</span></span>
<span data-ttu-id="48d53-156">Określa strefę czasową harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="48d53-156">Specifies the time zone of the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48d53-157">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="48d53-157">-StartTimeWindow</span></span>
<span data-ttu-id="48d53-158">Określa początek okna czasu.</span><span class="sxs-lookup"><span data-stu-id="48d53-158">Specifies the start of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48d53-159">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="48d53-159">-TimeWindowTimeZone</span></span>
<span data-ttu-id="48d53-160">Określa strefę czasową w oknie czasu.</span><span class="sxs-lookup"><span data-stu-id="48d53-160">Specifies the time zone of the time window.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48d53-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48d53-161">-DefaultProfile</span></span>
<span data-ttu-id="48d53-162">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="48d53-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48d53-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48d53-163">CommonParameters</span></span>
<span data-ttu-id="48d53-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48d53-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48d53-165">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48d53-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48d53-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48d53-166">INPUTS</span></span>

## <span data-ttu-id="48d53-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48d53-167">OUTPUTS</span></span>

### <span data-ttu-id="48d53-168">Microsoft. Azure. Management. Monitor. Management. models. AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="48d53-168">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="48d53-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48d53-169">NOTES</span></span>

## <span data-ttu-id="48d53-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48d53-170">RELATED LINKS</span></span>

[<span data-ttu-id="48d53-171">Dodaj-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="48d53-171">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="48d53-172">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="48d53-172">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="48d53-173">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="48d53-173">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="48d53-174">Nowe — AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="48d53-174">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="48d53-175">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="48d53-175">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)



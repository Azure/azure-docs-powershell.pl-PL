---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
ms.openlocfilehash: 1c3837bffcf5b3cde03623e06ad1233ed833a4c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004833"
---
# <span data-ttu-id="d6fc8-101">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="d6fc8-101">New-AzAutomationSchedule</span></span>

## <span data-ttu-id="d6fc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="d6fc8-103">Tworzy harmonogram automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="d6fc8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d6fc8-104">SYNTAX</span></span>

### <span data-ttu-id="d6fc8-105">ByDaily (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d6fc8-105">ByDaily (Default)</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6fc8-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="d6fc8-106">ByWeekly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6fc8-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="d6fc8-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6fc8-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="d6fc8-108">ByMonthlyDayOfWeek</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6fc8-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="d6fc8-109">ByOneTime</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6fc8-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="d6fc8-110">ByHourly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6fc8-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="d6fc8-111">DESCRIPTION</span></span>
<span data-ttu-id="d6fc8-112">Polecenie **cmdlet New-AzAutomationSchedule** tworzy harmonogram w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-112">The **New-AzAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="d6fc8-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d6fc8-113">EXAMPLES</span></span>

### <span data-ttu-id="d6fc8-114">Przykład 1. Tworzenie harmonogramu czasowego w czasie lokalnym</span><span class="sxs-lookup"><span data-stu-id="d6fc8-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\> $TimeZone = ([System.TimeZoneInfo]::Local).Id
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="d6fc8-115">Pierwsze polecenie pobiera identyfikator strefy czasowej z systemu i przechowuje je w $TimeZone czasowej.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="d6fc8-116">Drugie polecenie tworzy harmonogram uruchamiany raz w bieżącej dacie o godzinie 23:00 w określonej strefie czasowej.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="d6fc8-117">Przykład 2. Tworzenie harmonogramu cyklicznego</span><span class="sxs-lookup"><span data-stu-id="d6fc8-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DayInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d6fc8-118">Pierwsze polecenie tworzy obiekt daty przy użyciu polecenia cmdlet **Get-Date,** a następnie zapisuje ten obiekt w $StartDate danych.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="d6fc8-119">Określ czas, który w przyszłości wynosi co najmniej pięć minut.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-119">Specify a time that is at least five minutes in the future.</span></span>
<span data-ttu-id="d6fc8-120">Drugie polecenie tworzy obiekt daty przy użyciu polecenia cmdlet **Get-Date,** a następnie zapisuje ten obiekt w $EndDate danych.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="d6fc8-121">To polecenie określa czas w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-121">The command specifies a future time.</span></span>
<span data-ttu-id="d6fc8-122">Ostatnie polecenie tworzy harmonogram dzienny o nazwie Harmonogram02, który rozpoczyna się w czasie przechowywanym w $StartDate i wygasa w czasie przechowywanym w $EndDate.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-122">The final command creates a daily schedule named Schedule02 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

### <span data-ttu-id="d6fc8-123">Przykład 3. Tworzenie tygodniowego harmonogramu cyklicznego</span><span class="sxs-lookup"><span data-stu-id="d6fc8-123">Example 3: Create a weekly recurring schedule</span></span>
```
PS C:\> $StartTime = (Get-Date "13:00:00").AddDays(1)
PS C:\> [System.DayOfWeek[]]$WeekDays = @([System.DayOfWeek]::Monday..[System.DayOfWeek]::Friday)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule03" -StartTime $StartTime - WeekInterval 1 -DaysOfWeek $WeekDays -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d6fc8-124">Pierwsze polecenie tworzy obiekt daty przy użyciu polecenia cmdlet **Get-Date,** a następnie zapisuje ten obiekt w $StartDate danych.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-124">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="d6fc8-125">Drugie polecenie tworzy tablicę dni tygodnia zawierającą poniedziałek, wtorek, środę, czwartek i piątek.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-125">The second command creates an array of week days that contains Monday, Tuesday, Wednesday, Thursday and Friday.</span></span>
<span data-ttu-id="d6fc8-126">Ostatnie polecenie tworzy harmonogram dzienny o nazwie Harmonogram03, który będzie uruchamiany od poniedziałku do piątku każdego tygodnia o 13:00.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-126">The final command creates a daily schedule named Schedule03 that will run Monday to Friday each week at 13:00.</span></span> <span data-ttu-id="d6fc8-127">Harmonogram nigdy nie wygaśnie.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-127">The schedule will never expire.</span></span>

## <span data-ttu-id="d6fc8-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6fc8-128">PARAMETERS</span></span>

### <span data-ttu-id="d6fc8-129">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d6fc8-129">-AutomationAccountName</span></span>
<span data-ttu-id="d6fc8-130">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet tworzy harmonogram.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-130">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6fc8-131">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="d6fc8-131">-DayInterval</span></span>
<span data-ttu-id="d6fc8-132">Określa interwał (w dniach) dla harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-132">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="d6fc8-133">Jeśli nie określisz tego parametru i nie określisz parametru *OneTime,* wartość domyślna to jeden (1).</span><span class="sxs-lookup"><span data-stu-id="d6fc8-133">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByDaily
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6fc8-134">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="d6fc8-134">-DayOfWeek</span></span>
<span data-ttu-id="d6fc8-135">Określa listę dni tygodnia dla harmonogramu tygodniowego.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-135">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: System.Nullable`1[System.DayOfWeek]
Parameter Sets: ByMonthlyDayOfWeek
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6fc8-136">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="d6fc8-136">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="d6fc8-137">Określa wystąpienie tygodnia w miesiącu, w który został uruchomiony harmonogram.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-137">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="d6fc8-138">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="d6fc8-138">psdx_paramvalues</span></span>
- <span data-ttu-id="d6fc8-139">1</span><span class="sxs-lookup"><span data-stu-id="d6fc8-139">1</span></span>
- <span data-ttu-id="d6fc8-140">2</span><span class="sxs-lookup"><span data-stu-id="d6fc8-140">2</span></span>
- <span data-ttu-id="d6fc8-141">3</span><span class="sxs-lookup"><span data-stu-id="d6fc8-141">3</span></span>
- <span data-ttu-id="d6fc8-142">4</span><span class="sxs-lookup"><span data-stu-id="d6fc8-142">4</span></span>
- <span data-ttu-id="d6fc8-143">-1</span><span class="sxs-lookup"><span data-stu-id="d6fc8-143">-1</span></span>
- <span data-ttu-id="d6fc8-144">Pierwszy</span><span class="sxs-lookup"><span data-stu-id="d6fc8-144">First</span></span>
- <span data-ttu-id="d6fc8-145">Sekunda</span><span class="sxs-lookup"><span data-stu-id="d6fc8-145">Second</span></span>
- <span data-ttu-id="d6fc8-146">Trzecia</span><span class="sxs-lookup"><span data-stu-id="d6fc8-146">Third</span></span>
- <span data-ttu-id="d6fc8-147">Czwarta</span><span class="sxs-lookup"><span data-stu-id="d6fc8-147">Fourth</span></span>
- <span data-ttu-id="d6fc8-148">LastDay</span><span class="sxs-lookup"><span data-stu-id="d6fc8-148">LastDay</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Cmdlet.DayOfWeekOccurrence
Parameter Sets: ByMonthlyDayOfWeek
Aliases:
Accepted values: First, Second, Third, Fourth, Last

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6fc8-149">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="d6fc8-149">-DaysOfMonth</span></span>
<span data-ttu-id="d6fc8-150">Określa listę dni miesiąca dla harmonogramu miesięcznego.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-150">Specifies a list of days of the month for the monthly schedule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Cmdlet.DaysOfMonth[]
Parameter Sets: ByMonthlyDaysOfMonth
Aliases:
Accepted values: One, Two, Three, Four, Five, Six, Seventh, Eighth, Ninth, Tenth, Eleventh, Twelfth, Thirteenth, Fourteenth, Fifteenth, Sixteenth, Seventeenth, Eighteenth, Nineteenth, Twentieth, TwentyFirst, TwentySecond, TwentyThird, TwentyFourth, TwentyFifth, TwentySixth, TwentySeventh, TwentyEighth, TwentyNinth, Thirtieth, ThirtyFirst, LastDay

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6fc8-151">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="d6fc8-151">-DaysOfWeek</span></span>
<span data-ttu-id="d6fc8-152">Określa listę dni tygodnia dla harmonogramu tygodniowego.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-152">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: System.DayOfWeek[]
Parameter Sets: ByWeekly
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6fc8-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6fc8-153">-DefaultProfile</span></span>
<span data-ttu-id="d6fc8-154">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d6fc8-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6fc8-155">— Opis</span><span class="sxs-lookup"><span data-stu-id="d6fc8-155">-Description</span></span>
<span data-ttu-id="d6fc8-156">Określa opis harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-156">Specifies a description for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6fc8-157">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d6fc8-157">-ExpiryTime</span></span>
<span data-ttu-id="d6fc8-158">Określa czas wygaśnięcia harmonogramu jako obiekt **DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="d6fc8-158">Specifies the expiry time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="d6fc8-159">Możesz określić ciąg, który może zostać przekonwertowany na prawidłowy **dateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="d6fc8-159">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByDaily, ByWeekly, ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek, ByHourly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6fc8-160">-ForUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6fc8-160">-ForUpdateConfiguration</span></span>
<span data-ttu-id="d6fc8-161">Wskazuje, że ten obiekt harmonogramu będzie używany do planowania konfiguracji aktualizacji oprogramowania</span><span class="sxs-lookup"><span data-stu-id="d6fc8-161">Indicates that this schedule object will be used for scheduling a software update configuration</span></span>

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

### <span data-ttu-id="d6fc8-162">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="d6fc8-162">-HourInterval</span></span>
<span data-ttu-id="d6fc8-163">Określa interwał (w godzinach) dla harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-163">Specifies an interval, in hours, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByHourly
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6fc8-164">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="d6fc8-164">-MonthInterval</span></span>
<span data-ttu-id="d6fc8-165">Określa interwał (w miesiącu) dla harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-165">Specifies an interval, in Months, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6fc8-166">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d6fc8-166">-Name</span></span>
<span data-ttu-id="d6fc8-167">Określa nazwę harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-167">Specifies a name for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6fc8-168">— OneTime</span><span class="sxs-lookup"><span data-stu-id="d6fc8-168">-OneTime</span></span>
<span data-ttu-id="d6fc8-169">Określa, że polecenie cmdlet tworzy harmonogram czasowy.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-169">Specifies that the cmdlet creates a one-time schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByOneTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6fc8-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6fc8-170">-ResourceGroupName</span></span>
<span data-ttu-id="d6fc8-171">Określa nazwę grupy zasobów, dla której to polecenie cmdlet tworzy harmonogram.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-171">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6fc8-172">— StartTime</span><span class="sxs-lookup"><span data-stu-id="d6fc8-172">-StartTime</span></span>
<span data-ttu-id="d6fc8-173">Określa czas rozpoczęcia harmonogramu jako obiekt **DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="d6fc8-173">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="d6fc8-174">Możesz określić ciąg, który może zostać przekonwertowany na prawidłowy **dateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="d6fc8-174">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="d6fc8-175">Jeśli parametr *TimeZone* jest określony, przesunięcie zostanie zignorowane i zostanie użyta określona strefa czasowa.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-175">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6fc8-176">- Strefa czasowa</span><span class="sxs-lookup"><span data-stu-id="d6fc8-176">-TimeZone</span></span>
<span data-ttu-id="d6fc8-177">Określa strefę czasową harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-177">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="d6fc8-178">Ten ciąg może być identyfikatorem IANA lub identyfikatorem strefy czasowej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-178">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6fc8-179">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="d6fc8-179">-WeekInterval</span></span>
<span data-ttu-id="d6fc8-180">Określa interwał (w tygodniach) dla harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-180">Specifies an interval, in weeks, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByWeekly
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6fc8-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6fc8-181">CommonParameters</span></span>
<span data-ttu-id="d6fc8-182">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6fc8-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6fc8-183">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6fc8-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6fc8-184">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6fc8-184">INPUTS</span></span>

### <span data-ttu-id="d6fc8-185">System.String</span><span class="sxs-lookup"><span data-stu-id="d6fc8-185">System.String</span></span>

### <span data-ttu-id="d6fc8-186">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d6fc8-186">System.DateTimeOffset</span></span>

### <span data-ttu-id="d6fc8-187">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="d6fc8-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d6fc8-188">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6fc8-188">OUTPUTS</span></span>

### <span data-ttu-id="d6fc8-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="d6fc8-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="d6fc8-190">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d6fc8-190">NOTES</span></span>

## <span data-ttu-id="d6fc8-191">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6fc8-191">RELATED LINKS</span></span>

[<span data-ttu-id="d6fc8-192">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="d6fc8-192">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="d6fc8-193">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="d6fc8-193">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="d6fc8-194">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="d6fc8-194">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)



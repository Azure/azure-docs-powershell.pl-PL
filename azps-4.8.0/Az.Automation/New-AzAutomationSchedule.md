---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
ms.openlocfilehash: 9f9cd5b779fcc4e1b9dd6f3df7ed0255adeaa3af
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062398"
---
# <span data-ttu-id="14c74-101">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="14c74-101">New-AzAutomationSchedule</span></span>

## <span data-ttu-id="14c74-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="14c74-102">SYNOPSIS</span></span>
<span data-ttu-id="14c74-103">Tworzy harmonogram automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="14c74-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="14c74-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="14c74-104">SYNTAX</span></span>

### <span data-ttu-id="14c74-105">ByDaily (domyślny)</span><span class="sxs-lookup"><span data-stu-id="14c74-105">ByDaily (Default)</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="14c74-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="14c74-106">ByWeekly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14c74-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="14c74-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14c74-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="14c74-108">ByMonthlyDayOfWeek</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14c74-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="14c74-109">ByOneTime</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14c74-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="14c74-110">ByHourly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14c74-111">Opis</span><span class="sxs-lookup"><span data-stu-id="14c74-111">DESCRIPTION</span></span>
<span data-ttu-id="14c74-112">Polecenie cmdlet **New-AzAutomationSchedule** tworzy harmonogram w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="14c74-112">The **New-AzAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="14c74-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="14c74-113">EXAMPLES</span></span>

### <span data-ttu-id="14c74-114">Przykład 1. Tworzenie jednorazowego harmonogramu w czasie lokalnym</span><span class="sxs-lookup"><span data-stu-id="14c74-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\> $TimeZone = ([System.TimeZoneInfo]::Local).Id
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="14c74-115">Pierwsze polecenie pobiera identyfikator strefy czasowej z systemu i zapisuje go w zmiennej $TimeZone.</span><span class="sxs-lookup"><span data-stu-id="14c74-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="14c74-116">Drugie polecenie tworzy harmonogram, który jest uruchamiany raz w bieżącej dacie o godzinie 11:00 PM w określonej strefie czasowej...</span><span class="sxs-lookup"><span data-stu-id="14c74-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="14c74-117">Przykład 2: Tworzenie harmonogramu cyklicznego</span><span class="sxs-lookup"><span data-stu-id="14c74-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DayInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="14c74-118">Pierwsze polecenie tworzy obiekt date przy użyciu polecenia cmdlet **Get-Date** , a następnie zapisuje obiekt w zmiennej $startdate.</span><span class="sxs-lookup"><span data-stu-id="14c74-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="14c74-119">Określ czas w przyszłości, co najmniej pięć minut.</span><span class="sxs-lookup"><span data-stu-id="14c74-119">Specify a time that is at least five minutes in the future.</span></span>
<span data-ttu-id="14c74-120">Drugie polecenie tworzy obiekt date przy użyciu polecenia cmdlet **Get-Date** , a następnie zapisuje obiekt w zmiennej $EndDate.</span><span class="sxs-lookup"><span data-stu-id="14c74-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="14c74-121">Polecenie określa przyszły termin.</span><span class="sxs-lookup"><span data-stu-id="14c74-121">The command specifies a future time.</span></span>
<span data-ttu-id="14c74-122">Ostatnie polecenie tworzy dzienny harmonogram o nazwie Schedule02, który rozpoczyna się w czasie przechowywanym w $StartDate i wygasa w czasie przechowywanym w $EndDate.</span><span class="sxs-lookup"><span data-stu-id="14c74-122">The final command creates a daily schedule named Schedule02 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

### <span data-ttu-id="14c74-123">Przykład 3: Tworzenie tygodniowego harmonogramu cyklicznego</span><span class="sxs-lookup"><span data-stu-id="14c74-123">Example 3: Create a weekly recurring schedule</span></span>
```
PS C:\> $StartTime = (Get-Date "13:00:00").AddDays(1)
PS C:\> [System.DayOfWeek[]]$WeekDays = @([System.DayOfWeek]::Monday..[System.DayOfWeek]::Friday)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule03" -StartTime $StartTime - WeekInterval 1 -DaysOfWeek $WeekDays -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="14c74-124">Pierwsze polecenie tworzy obiekt date przy użyciu polecenia cmdlet **Get-Date** , a następnie zapisuje obiekt w zmiennej $startdate.</span><span class="sxs-lookup"><span data-stu-id="14c74-124">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="14c74-125">Drugie polecenie tworzy tablicę dni tygodnia zawierającą poniedziałek, wtorek, środa, czwartek i piątek.</span><span class="sxs-lookup"><span data-stu-id="14c74-125">The second command creates an array of week days that contains Monday, Tuesday, Wednesday, Thursday and Friday.</span></span>
<span data-ttu-id="14c74-126">Ostatnie polecenie tworzy dzienny harmonogram o nazwie Schedule03, który będzie od poniedziałku do piątku co tydzień o godzinie 13:00.</span><span class="sxs-lookup"><span data-stu-id="14c74-126">The final command creates a daily schedule named Schedule03 that will run Monday to Friday each week at 13:00.</span></span> <span data-ttu-id="14c74-127">Harmonogram nigdy nie wygaśnie.</span><span class="sxs-lookup"><span data-stu-id="14c74-127">The schedule will never expire.</span></span>

## <span data-ttu-id="14c74-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="14c74-128">PARAMETERS</span></span>

### <span data-ttu-id="14c74-129">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="14c74-129">-AutomationAccountName</span></span>
<span data-ttu-id="14c74-130">Określa nazwę konta automatyzacji, dla którego jest tworzony harmonogram za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14c74-130">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="14c74-131">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="14c74-131">-DayInterval</span></span>
<span data-ttu-id="14c74-132">Określa interwał (w dniach) harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="14c74-132">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="14c74-133">Jeśli nie określono tego parametru, a parametr *onetime* nie zostanie określony, wartością domyślną jest jeden (1).</span><span class="sxs-lookup"><span data-stu-id="14c74-133">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

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

### <span data-ttu-id="14c74-134">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="14c74-134">-DayOfWeek</span></span>
<span data-ttu-id="14c74-135">Określa listę dni tygodnia dla harmonogramu tygodniowego.</span><span class="sxs-lookup"><span data-stu-id="14c74-135">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="14c74-136">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="14c74-136">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="14c74-137">Określa wystąpienie tygodnia w ciągu miesiąca, w którym ma się rozpoczynać harmonogram.</span><span class="sxs-lookup"><span data-stu-id="14c74-137">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="14c74-138">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="14c74-138">psdx_paramvalues</span></span>
- <span data-ttu-id="14c74-139">jedno</span><span class="sxs-lookup"><span data-stu-id="14c74-139">1</span></span>
- <span data-ttu-id="14c74-140">2,6</span><span class="sxs-lookup"><span data-stu-id="14c74-140">2</span></span>
- <span data-ttu-id="14c74-141">3,2</span><span class="sxs-lookup"><span data-stu-id="14c74-141">3</span></span>
- <span data-ttu-id="14c74-142">r.[4</span><span class="sxs-lookup"><span data-stu-id="14c74-142">4</span></span>
- <span data-ttu-id="14c74-143">-1</span><span class="sxs-lookup"><span data-stu-id="14c74-143">-1</span></span>
- <span data-ttu-id="14c74-144">Pierwszy</span><span class="sxs-lookup"><span data-stu-id="14c74-144">First</span></span>
- <span data-ttu-id="14c74-145">Drugiego</span><span class="sxs-lookup"><span data-stu-id="14c74-145">Second</span></span>
- <span data-ttu-id="14c74-146">1/3</span><span class="sxs-lookup"><span data-stu-id="14c74-146">Third</span></span>
- <span data-ttu-id="14c74-147">Czwarty</span><span class="sxs-lookup"><span data-stu-id="14c74-147">Fourth</span></span>
- <span data-ttu-id="14c74-148">LastDay</span><span class="sxs-lookup"><span data-stu-id="14c74-148">LastDay</span></span>

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

### <span data-ttu-id="14c74-149">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="14c74-149">-DaysOfMonth</span></span>
<span data-ttu-id="14c74-150">Określa listę dni miesiąca dla harmonogramu miesięcznego.</span><span class="sxs-lookup"><span data-stu-id="14c74-150">Specifies a list of days of the month for the monthly schedule.</span></span>

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

### <span data-ttu-id="14c74-151">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="14c74-151">-DaysOfWeek</span></span>
<span data-ttu-id="14c74-152">Określa listę dni tygodnia dla harmonogramu tygodniowego.</span><span class="sxs-lookup"><span data-stu-id="14c74-152">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="14c74-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14c74-153">-DefaultProfile</span></span>
<span data-ttu-id="14c74-154">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="14c74-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14c74-155">— Opis</span><span class="sxs-lookup"><span data-stu-id="14c74-155">-Description</span></span>
<span data-ttu-id="14c74-156">Określa opis harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="14c74-156">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="14c74-157">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="14c74-157">-ExpiryTime</span></span>
<span data-ttu-id="14c74-158">Określa czas wygaśnięcia harmonogramu jako obiekt **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="14c74-158">Specifies the expiry time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="14c74-159">Możesz określić ciąg, który może być konwertowany na prawidłowy znak **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="14c74-159">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="14c74-160">-ForUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="14c74-160">-ForUpdateConfiguration</span></span>
<span data-ttu-id="14c74-161">Wskazuje, że ten obiekt harmonogramu będzie wykorzystany do zaplanowania konfiguracji aktualizacji oprogramowania</span><span class="sxs-lookup"><span data-stu-id="14c74-161">Indicates that this schedule object will be used for scheduling a software update configuration</span></span>

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

### <span data-ttu-id="14c74-162">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="14c74-162">-HourInterval</span></span>
<span data-ttu-id="14c74-163">Określa interwał (w godzinach) harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="14c74-163">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="14c74-164">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="14c74-164">-MonthInterval</span></span>
<span data-ttu-id="14c74-165">Określa interwał (w miesiącach) harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="14c74-165">Specifies an interval, in Months, for the schedule.</span></span>

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

### <span data-ttu-id="14c74-166">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="14c74-166">-Name</span></span>
<span data-ttu-id="14c74-167">Określa nazwę harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="14c74-167">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="14c74-168">-OneTime</span><span class="sxs-lookup"><span data-stu-id="14c74-168">-OneTime</span></span>
<span data-ttu-id="14c74-169">Określa, że polecenie cmdlet tworzy harmonogram jednorazowy.</span><span class="sxs-lookup"><span data-stu-id="14c74-169">Specifies that the cmdlet creates a one-time schedule.</span></span>

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

### <span data-ttu-id="14c74-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14c74-170">-ResourceGroupName</span></span>
<span data-ttu-id="14c74-171">Określa nazwę grupy zasobów, dla której jest tworzony harmonogram za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14c74-171">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="14c74-172">-StartTime</span><span class="sxs-lookup"><span data-stu-id="14c74-172">-StartTime</span></span>
<span data-ttu-id="14c74-173">Określa godzinę rozpoczęcia harmonogramu jako obiekt **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="14c74-173">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="14c74-174">Możesz określić ciąg, który może być konwertowany na prawidłowy znak **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="14c74-174">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="14c74-175">Jeśli określono parametr *timezone* , przesunięcia zostaną zignorowane, a określona strefa czasowa jest używana.</span><span class="sxs-lookup"><span data-stu-id="14c74-175">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

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

### <span data-ttu-id="14c74-176">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="14c74-176">-TimeZone</span></span>
<span data-ttu-id="14c74-177">Określa strefę czasową harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="14c74-177">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="14c74-178">Ten ciąg może być IDENTYFIKATORem IANA lub IDENTYFIKATORem strefy czasowej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="14c74-178">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

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

### <span data-ttu-id="14c74-179">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="14c74-179">-WeekInterval</span></span>
<span data-ttu-id="14c74-180">Określa interwał (w tygodniach) harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="14c74-180">Specifies an interval, in weeks, for the schedule.</span></span>

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

### <span data-ttu-id="14c74-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c74-181">CommonParameters</span></span>
<span data-ttu-id="14c74-182">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14c74-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c74-183">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14c74-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c74-184">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14c74-184">INPUTS</span></span>

### <span data-ttu-id="14c74-185">System. String</span><span class="sxs-lookup"><span data-stu-id="14c74-185">System.String</span></span>

### <span data-ttu-id="14c74-186">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="14c74-186">System.DateTimeOffset</span></span>

### <span data-ttu-id="14c74-187">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="14c74-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="14c74-188">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="14c74-188">OUTPUTS</span></span>

### <span data-ttu-id="14c74-189">Microsoft. Azure. Commands. Automation. model. Schedule</span><span class="sxs-lookup"><span data-stu-id="14c74-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="14c74-190">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="14c74-190">NOTES</span></span>

## <span data-ttu-id="14c74-191">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14c74-191">RELATED LINKS</span></span>

[<span data-ttu-id="14c74-192">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="14c74-192">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="14c74-193">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="14c74-193">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="14c74-194">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="14c74-194">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)



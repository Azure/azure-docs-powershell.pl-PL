---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9574CEB5-B699-4606-8C5E-CE2C0D01092D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
ms.openlocfilehash: 740077def0ba0eccb1d962b88317fadb3c5c897c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526321"
---
# <span data-ttu-id="27200-101">New-AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="27200-101">New-AzureRmBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="27200-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="27200-102">SYNOPSIS</span></span>
<span data-ttu-id="27200-103">Tworzy zasady przechowywania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="27200-103">Creates a Backup retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27200-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="27200-104">SYNTAX</span></span>

### <span data-ttu-id="27200-105">DailyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="27200-105">DailyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-DailyRetention] -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27200-106">WeeklyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="27200-106">WeeklyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-WeeklyRetention] -DaysOfWeek <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27200-107">MonthlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="27200-107">MonthlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27200-108">MonthlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="27200-108">MonthlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27200-109">YearlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="27200-109">YearlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -MonthsOfYear <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27200-110">YearlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="27200-110">YearlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -MonthsOfYear <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27200-111">Opis</span><span class="sxs-lookup"><span data-stu-id="27200-111">DESCRIPTION</span></span>
<span data-ttu-id="27200-112">Polecenie cmdlet **New-AzureRmBackupRetentionPolicyObject** tworzy zasady przechowywania kopii zapasowej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="27200-112">The **New-AzureRmBackupRetentionPolicyObject** cmdlet creates an Azure Backup retention policy.</span></span>
<span data-ttu-id="27200-113">Zasady przechowywania określają, jak długo kopia zapasowa zachowuje punkt odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="27200-113">A retention policy defines how long Backup keeps a recovery point.</span></span>
<span data-ttu-id="27200-114">Typy przechowywania są następujące:</span><span class="sxs-lookup"><span data-stu-id="27200-114">The types of retention are the following:</span></span> 
- <span data-ttu-id="27200-115">Dobow</span><span class="sxs-lookup"><span data-stu-id="27200-115">Daily</span></span> 
- <span data-ttu-id="27200-116">Weekly</span><span class="sxs-lookup"><span data-stu-id="27200-116">Weekly</span></span> 
- <span data-ttu-id="27200-117">Podstaw</span><span class="sxs-lookup"><span data-stu-id="27200-117">Monthly</span></span> 
- <span data-ttu-id="27200-118">Rocznie Utwórz jednej zasady przechowywania dla każdego typu retencji, który ma zostać użyty.</span><span class="sxs-lookup"><span data-stu-id="27200-118">Yearly Create one retention policy for each type of retention that you plan to use.</span></span>
<span data-ttu-id="27200-119">Zasady tworzenia kopii zapasowych są skojarzone z co najmniej jednym zasadami przechowywania.</span><span class="sxs-lookup"><span data-stu-id="27200-119">A backup policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="27200-120">Aby utworzyć zasady tworzenia kopii zapasowych, użyj polecenia cmdlet New-AzureRmBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="27200-120">To create a backup policy, use the New-AzureRmBackupProtectionPolicy cmdlet.</span></span>
<span data-ttu-id="27200-121">Możesz zamiast tego podać zasady przechowywania dla Enable-AzureRmBackupProtection polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27200-121">You can instead provide a retention policy to the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="27200-122">Przykłady</span><span class="sxs-lookup"><span data-stu-id="27200-122">EXAMPLES</span></span>

### <span data-ttu-id="27200-123">Przykład 1: Tworzenie zasad przechowywania do codziennego przechowywania</span><span class="sxs-lookup"><span data-stu-id="27200-123">Example 1: Create a retention policy for daily retention</span></span>
```
PS C:\>$Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Daily
RetentionType      Retention          RetentionTimes
-------------      ---------          --------------
Daily              30
```

<span data-ttu-id="27200-124">Pierwsze polecenie tworzy zasady przechowywania przez 30 dni codziennego przechowywania, a następnie zapisuje je w zmiennej $Daily.</span><span class="sxs-lookup"><span data-stu-id="27200-124">The first command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>
<span data-ttu-id="27200-125">Drugie polecenie wyświetla zawartość $Daily.</span><span class="sxs-lookup"><span data-stu-id="27200-125">The second command displays the contents of $Daily.</span></span>

### <span data-ttu-id="27200-126">Przykład 2: Tworzenie miesięcznych zasad przechowywania</span><span class="sxs-lookup"><span data-stu-id="27200-126">Example 2: Create a monthly retention policy</span></span>
```
PS C:\>$Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $Monthly | select *
RetentionFormat : Daily
DaysOfMonth     : {10, 20}
WeekNumber      : 
DaysOfWeek      : 
RetentionType   : Monthly
Retention       : 12
RetentionTimes  :
```

<span data-ttu-id="27200-127">Pierwsze polecenie tworzy zasady przechowywania, które przechowują kopię zapasową w dziesiątym i dwudziestym dniu każdego miesiąca przez dwanaście miesięcy.</span><span class="sxs-lookup"><span data-stu-id="27200-127">The first command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="27200-128">Polecenie przechowuje zasady przechowywania w zmiennej $Monthly.</span><span class="sxs-lookup"><span data-stu-id="27200-128">The command stores the retention policy in the $Monthly variable.</span></span>
<span data-ttu-id="27200-129">Drugie polecenie wyświetla zawartość $Monthly.</span><span class="sxs-lookup"><span data-stu-id="27200-129">The second command displays the contents of $Monthly.</span></span>

## <span data-ttu-id="27200-130">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="27200-130">PARAMETERS</span></span>

### <span data-ttu-id="27200-131">-DailyRetention</span><span class="sxs-lookup"><span data-stu-id="27200-131">-DailyRetention</span></span>
<span data-ttu-id="27200-132">Wskazuje, że to polecenie cmdlet tworzy codzienne zasady przechowywania.</span><span class="sxs-lookup"><span data-stu-id="27200-132">Indicates that this cmdlet creates a Daily retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyRetentionParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27200-133">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="27200-133">-DaysOfMonth</span></span>
<span data-ttu-id="27200-134">Określa dni miesiąca, w których należy określić, że kopie zapasowe punktów odzyskiwania są zachowywane i przez czas.</span><span class="sxs-lookup"><span data-stu-id="27200-134">Specifies the days of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="27200-135">Dozwolone wartości dla tego parametru to: liczby całkowite z zakresu od 1 do 28 i ostatnie.</span><span class="sxs-lookup"><span data-stu-id="27200-135">The acceptable values for this parameter are: integers from 1 through 28 and Last.</span></span>
<span data-ttu-id="27200-136">Określ ten parametr, jeśli określisz parametry *DailyRetention* , *MonthlyRetentionInDailyFormat* i *YearlyRetentionInDailyFormat* .</span><span class="sxs-lookup"><span data-stu-id="27200-136">Specify this parameter if you specify the *DailyRetention* , *MonthlyRetentionInDailyFormat* , and *YearlyRetentionInDailyFormat* parameters.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: MonthlyRetentionInDailyFormatParamSet, YearlyRetentionInDailyFormatParamSet
Aliases:
Accepted values: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27200-137">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="27200-137">-DaysOfWeek</span></span>
<span data-ttu-id="27200-138">Określa tablicę dni tygodnia.</span><span class="sxs-lookup"><span data-stu-id="27200-138">Specifies an array of days of the week.</span></span>
<span data-ttu-id="27200-139">Dni, w których to polecenie cmdlet określa, jakie punkty odzyskiwania są zachowywane i jak długo.</span><span class="sxs-lookup"><span data-stu-id="27200-139">The days that this cmdlet specifies identify which recovery points that Backup retains and for how long.</span></span>
<span data-ttu-id="27200-140">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="27200-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="27200-141">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="27200-141">Monday</span></span> 
- <span data-ttu-id="27200-142">Wtorku</span><span class="sxs-lookup"><span data-stu-id="27200-142">Tuesday</span></span> 
- <span data-ttu-id="27200-143">Środa</span><span class="sxs-lookup"><span data-stu-id="27200-143">Wednesday</span></span> 
- <span data-ttu-id="27200-144">Czwartek</span><span class="sxs-lookup"><span data-stu-id="27200-144">Thursday</span></span> 
- <span data-ttu-id="27200-145">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="27200-145">Friday</span></span> 
- <span data-ttu-id="27200-146">Sobota</span><span class="sxs-lookup"><span data-stu-id="27200-146">Saturday</span></span> 
- <span data-ttu-id="27200-147">Niedziela Określ ten parametr, jeśli określisz parametry *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* i *YearlyRetentionInWeeklyFormat* .</span><span class="sxs-lookup"><span data-stu-id="27200-147">Sunday Specify this parameter if you specify the *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* , and *YearlyRetentionInWeeklyFormat* parameters.</span></span>
<span data-ttu-id="27200-148">Należy się upewnić, że dni tygodnia, które zostały wybrane dla kopii zapasowej i do przechowywania, są wyrównane.</span><span class="sxs-lookup"><span data-stu-id="27200-148">Be sure that the days of the week you select for backup and for retention are aligned.</span></span>
<span data-ttu-id="27200-149">Jeśli na przykład dla kopii zapasowej jest ustawiona wartość soboty, zasady przechowywania muszą także korzystać z soboty.</span><span class="sxs-lookup"><span data-stu-id="27200-149">For example, if your backup is set for Saturdays, the retention policies must also use Saturday.</span></span>

```yaml
Type: System.String[]
Parameter Sets: WeeklyRetentionParamSet, MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27200-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27200-150">-DefaultProfile</span></span>
<span data-ttu-id="27200-151">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="27200-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27200-152">-MonthlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="27200-152">-MonthlyRetentionInDailyFormat</span></span>
<span data-ttu-id="27200-153">Wskazuje, że to polecenie cmdlet tworzy zasady miesięczne w codziennym formacie.</span><span class="sxs-lookup"><span data-stu-id="27200-153">Indicates that this cmdlet creates a Monthly policy in Daily format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInDailyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27200-154">-MonthlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="27200-154">-MonthlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="27200-155">Wskazuje, że to polecenie cmdlet tworzy zasady miesięczne w formacie tygodnia.</span><span class="sxs-lookup"><span data-stu-id="27200-155">Indicates that this cmdlet creates a Monthly policy in Weekly format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27200-156">-MonthsOfYear</span><span class="sxs-lookup"><span data-stu-id="27200-156">-MonthsOfYear</span></span>
<span data-ttu-id="27200-157">Określa, które miesiące roku mają punkty odzyskiwania, których kopie zapasowe są zachowywane w skali rocznej.</span><span class="sxs-lookup"><span data-stu-id="27200-157">Specifies which months of the year have the recovery points that Backup retains on a yearly basis.</span></span>
<span data-ttu-id="27200-158">Dopuszczalne wartości tego parametru to: nazwy miesięcy, na przykład styczeń lub luty.</span><span class="sxs-lookup"><span data-stu-id="27200-158">The acceptable values for this parameter are: names of months, such as January or February.</span></span>

```yaml
Type: System.String[]
Parameter Sets: YearlyRetentionInDailyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases:
Accepted values: January, February, March, April, May, June, July, August, September, October, November, December

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27200-159">-Retencja</span><span class="sxs-lookup"><span data-stu-id="27200-159">-Retention</span></span>
<span data-ttu-id="27200-160">Określa okres przechowywania, w dniach, miesiącach lub latach, dla którego kopia zapasowa zawiera punkt kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="27200-160">Specifies the retention period, in days, months, or years, for which Backup stores a backup point.</span></span>
<span data-ttu-id="27200-161">Jednostka zależy od tego, czy to polecenie cmdlet umożliwia wybranie opcji przechowywania codziennie, comiesięcznego czy rocznego.</span><span class="sxs-lookup"><span data-stu-id="27200-161">The unit depends on whether this cmdlet selects a daily, monthly, or yearly retention option.</span></span>
<span data-ttu-id="27200-162">Jeśli na przykład określono parametr *DailyRetention* , polecenie cmdlet interpretuje bieżący parametr jako liczbę dni.</span><span class="sxs-lookup"><span data-stu-id="27200-162">For example, if specify the *DailyRetention* parameter, the cmdlet interprets the current parameter as a number of days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27200-163">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="27200-163">-WeeklyRetention</span></span>
<span data-ttu-id="27200-164">Wskazuje, że to polecenie cmdlet tworzy cotygodniowe zasady przechowywania.</span><span class="sxs-lookup"><span data-stu-id="27200-164">Indicates that this cmdlet creates a Weekly retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyRetentionParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27200-165">-WeekNumber</span><span class="sxs-lookup"><span data-stu-id="27200-165">-WeekNumber</span></span>
<span data-ttu-id="27200-166">Określa tygodnie miesiąca, które identyfikują, które kopie zapasowe punktów odzyskiwania są zachowywane i jak długo.</span><span class="sxs-lookup"><span data-stu-id="27200-166">Specifies the weeks of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="27200-167">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="27200-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="27200-168">Pierwszy</span><span class="sxs-lookup"><span data-stu-id="27200-168">First</span></span> 
- <span data-ttu-id="27200-169">Drugiego</span><span class="sxs-lookup"><span data-stu-id="27200-169">Second</span></span> 
- <span data-ttu-id="27200-170">1/3</span><span class="sxs-lookup"><span data-stu-id="27200-170">Third</span></span> 
- <span data-ttu-id="27200-171">Czwarty</span><span class="sxs-lookup"><span data-stu-id="27200-171">Fourth</span></span> 
- <span data-ttu-id="27200-172">Końcu</span><span class="sxs-lookup"><span data-stu-id="27200-172">Last</span></span>

```yaml
Type: System.String[]
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases:
Accepted values: First, Second, Third, Fourth, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27200-173">-YearlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="27200-173">-YearlyRetentionInDailyFormat</span></span>
<span data-ttu-id="27200-174">Wskazuje, że to polecenie cmdlet tworzy zasady przechowywania roczne w codziennej formie.</span><span class="sxs-lookup"><span data-stu-id="27200-174">Indicates that this cmdlet creates a Yearly retention policy in Daily format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInDailyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27200-175">-YearlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="27200-175">-YearlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="27200-176">Wskazuje, że to polecenie cmdlet tworzy roczne zasady przechowywania w formacie tygodnia.</span><span class="sxs-lookup"><span data-stu-id="27200-176">Indicates that this cmdlet creates a Yearly retention policy in Weekly format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInWeeklyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27200-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27200-177">CommonParameters</span></span>
<span data-ttu-id="27200-178">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27200-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27200-179">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27200-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27200-180">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27200-180">INPUTS</span></span>

### <span data-ttu-id="27200-181">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="27200-181">None</span></span>

## <span data-ttu-id="27200-182">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="27200-182">OUTPUTS</span></span>

### <span data-ttu-id="27200-183">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="27200-183">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy</span></span>

## <span data-ttu-id="27200-184">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="27200-184">NOTES</span></span>
* <span data-ttu-id="27200-185">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="27200-185">None</span></span>

## <span data-ttu-id="27200-186">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27200-186">RELATED LINKS</span></span>

[<span data-ttu-id="27200-187">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="27200-187">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="27200-188">Nowe — AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="27200-188">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)



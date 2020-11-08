---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: D28DD808-E8EF-4C71-A353-8BF1E458DF6F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9fcae4a0232331a020a716b3f7284b8f6dfc3212
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055185"
---
# <span data-ttu-id="4f4f8-101">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="4f4f8-101">New-AzureAutomationSchedule</span></span>

## <span data-ttu-id="4f4f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4f4f8-102">SYNOPSIS</span></span>

<span data-ttu-id="4f4f8-103">Tworzy harmonogram automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="4f4f8-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="4f4f8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4f4f8-104">SYNTAX</span></span>

### <span data-ttu-id="4f4f8-105">ByDaily (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4f4f8-105">ByDaily (Default)</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f4f8-106">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="4f4f8-106">ByOneTime</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>] [-OneTime]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4f4f8-107">ByHourly</span><span class="sxs-lookup"><span data-stu-id="4f4f8-107">ByHourly</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4f4f8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4f4f8-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="4f4f8-109">Polecenie cmdlet **New-AzureAutomationSchedule** tworzy harmonogram w usłudze Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="4f4f8-109">The **New-AzureAutomationSchedule** cmdlet creates a schedule in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="4f4f8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4f4f8-110">EXAMPLES</span></span>

### <span data-ttu-id="4f4f8-111">Przykład 1. Tworzenie harmonogramu jednorazowego</span><span class="sxs-lookup"><span data-stu-id="4f4f8-111">Example 1: Create a one-time schedule</span></span>
```
PS C:\> New-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime
```

<span data-ttu-id="4f4f8-112">Poniższe polecenie tworzy harmonogram, który jest uruchamiany raz w bieżącej dacie o godzinie 11:00 PM.</span><span class="sxs-lookup"><span data-stu-id="4f4f8-112">The following command creates a schedule that runs one time on the current date at 11:00 PM.</span></span>

### <span data-ttu-id="4f4f8-113">Przykład 2: Tworzenie harmonogramu cyklicznego</span><span class="sxs-lookup"><span data-stu-id="4f4f8-113">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1
```

<span data-ttu-id="4f4f8-114">Poniższe polecenia tworzą nowy harmonogram, który jest uruchamiany w dniu 1:00 PM codziennie przez rok rozpoczynający się w dniu bieżącym.</span><span class="sxs-lookup"><span data-stu-id="4f4f8-114">The following commands create a new schedule that runs at 1:00 PM every day for one year starting on the current day.</span></span>

## <span data-ttu-id="4f4f8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4f4f8-115">PARAMETERS</span></span>

### <span data-ttu-id="4f4f8-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4f4f8-116">-AutomationAccountName</span></span>
<span data-ttu-id="4f4f8-117">Określa nazwę konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="4f4f8-117">Specifies the name of an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f4f8-118">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="4f4f8-118">-DayInterval</span></span>
<span data-ttu-id="4f4f8-119">Określa interwał (w dniach) harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="4f4f8-119">Specifies an interval, in days, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByDaily
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f4f8-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="4f4f8-120">-Description</span></span>
<span data-ttu-id="4f4f8-121">Określa opis.</span><span class="sxs-lookup"><span data-stu-id="4f4f8-121">Specifies a description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f4f8-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4f4f8-122">-ExpiryTime</span></span>
<span data-ttu-id="4f4f8-123">Określa czas wygaśnięcia harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="4f4f8-123">Specifies the expiry time of a schedule.</span></span>
<span data-ttu-id="4f4f8-124">Można podać ciąg, jeśli można go przekonwertować na prawidłowy **element DateTime**.</span><span class="sxs-lookup"><span data-stu-id="4f4f8-124">A string can be provided if it can be converted to a valid **DateTime**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByDaily, ByHourly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f4f8-125">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="4f4f8-125">-HourInterval</span></span>
<span data-ttu-id="4f4f8-126">Określa interwał (w godzinach) harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="4f4f8-126">Specifies an interval, in hours, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByHourly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f4f8-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4f4f8-127">-Name</span></span>
<span data-ttu-id="4f4f8-128">Określa nazwę harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="4f4f8-128">Specifies a name for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f4f8-129">-OneTime</span><span class="sxs-lookup"><span data-stu-id="4f4f8-129">-OneTime</span></span>
<span data-ttu-id="4f4f8-130">Wskazuje, że ta operacja powoduje utworzenie jednorazowego harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="4f4f8-130">Indicates that this operation creates a one-time schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByOneTime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f4f8-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="4f4f8-131">-Profile</span></span>
<span data-ttu-id="4f4f8-132">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f4f8-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4f4f8-133">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="4f4f8-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f4f8-134">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4f4f8-134">-StartTime</span></span>
<span data-ttu-id="4f4f8-135">Określa godzinę rozpoczęcia harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="4f4f8-135">Specifies the start time of a schedule.</span></span>
<span data-ttu-id="4f4f8-136">Można podać ciąg, jeśli można go przekonwertować na prawidłowy **element DateTime**.</span><span class="sxs-lookup"><span data-stu-id="4f4f8-136">A string can be provided if it can be converted to a valid **DateTime**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f4f8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f4f8-137">CommonParameters</span></span>
<span data-ttu-id="4f4f8-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f4f8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f4f8-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f4f8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f4f8-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f4f8-140">INPUTS</span></span>

## <span data-ttu-id="4f4f8-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4f4f8-141">OUTPUTS</span></span>

### <span data-ttu-id="4f4f8-142">Microsoft. Azure. Commands. Automation. model. Schedule</span><span class="sxs-lookup"><span data-stu-id="4f4f8-142">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="4f4f8-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4f4f8-143">NOTES</span></span>

## <span data-ttu-id="4f4f8-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f4f8-144">RELATED LINKS</span></span>

[<span data-ttu-id="4f4f8-145">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="4f4f8-145">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="4f4f8-146">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="4f4f8-146">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)

[<span data-ttu-id="4f4f8-147">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="4f4f8-147">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)



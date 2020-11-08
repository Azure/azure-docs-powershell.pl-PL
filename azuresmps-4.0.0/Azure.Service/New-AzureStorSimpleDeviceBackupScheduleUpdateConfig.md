---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 22C6845E-D7BD-4BBC-B373-394A23488A94
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0695dc42d9c540e30ddf9ac55bd6fc136c84bff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054490"
---
# <span data-ttu-id="0f33a-101">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="0f33a-101">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>

## <span data-ttu-id="0f33a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0f33a-102">SYNOPSIS</span></span>
<span data-ttu-id="0f33a-103">Umożliwia utworzenie obiektu konfiguracji Planowanie kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="0f33a-103">Creates a backup schedule update configuration object.</span></span>

## <span data-ttu-id="0f33a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0f33a-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id <String> -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] [-Enabled <Boolean>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0f33a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0f33a-105">DESCRIPTION</span></span>
<span data-ttu-id="0f33a-106">Polecenie cmdlet **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** tworzy obiekt konfiguracji **BackupScheduleUpdateRequest** .</span><span class="sxs-lookup"><span data-stu-id="0f33a-106">The **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet creates a **BackupScheduleUpdateRequest** configuration object.</span></span>
<span data-ttu-id="0f33a-107">Ten obiekt konfiguracji służy do aktualizowania zasad tworzenia kopii zapasowych przy użyciu polecenia cmdlet **Set-AzureStorSimpleDeviceBackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="0f33a-107">Use this configuration object to update a backup policy by using the **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="0f33a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0f33a-108">EXAMPLES</span></span>

### <span data-ttu-id="0f33a-109">Przykład 1: Tworzenie żądania aktualizacji harmonogramu</span><span class="sxs-lookup"><span data-stu-id="0f33a-109">Example 1: Create a schedule update request</span></span>
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "147f734d-a31a-4473-8501-6ba38be2cb30" -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 50 -Enabled $True
VERBOSE: ClientRequestId: ef346641-54b4-4273-8898-7f863e7c5b7e_PS


BackupType     : CloudSnapshot
Id             : 147f734d-a31a-4473-8501-6ba38be2cb30
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 50
StartTime      : 2014-12-16T00:39:32+05:30
Status         : Enabled
```

<span data-ttu-id="0f33a-110">To polecenie tworzy żądanie aktualizacji harmonogramu kopii zapasowej dla harmonogramu o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="0f33a-110">This command creates a backup schedule update request for the schedule that has the specified ID.</span></span>
<span data-ttu-id="0f33a-111">Żądanie polega na zapełnieniu harmonogramu kopii zapasowej migawki w chmurze, która powtarza się co godzinę.</span><span class="sxs-lookup"><span data-stu-id="0f33a-111">The request is to make the schedule a cloud snapshot backup that recurs every hour.</span></span>
<span data-ttu-id="0f33a-112">Kopie zapasowe są zachowywane przez 50 dni.</span><span class="sxs-lookup"><span data-stu-id="0f33a-112">The backups are kept for 50 days.</span></span>
<span data-ttu-id="0f33a-113">Ten harmonogram jest włączony od domyślnego czasu, który jest bieżącą godziną.</span><span class="sxs-lookup"><span data-stu-id="0f33a-113">This schedule is enabled from the default time, which is the current time.</span></span>

## <span data-ttu-id="0f33a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f33a-114">PARAMETERS</span></span>

### <span data-ttu-id="0f33a-115">-Backuptype</span><span class="sxs-lookup"><span data-stu-id="0f33a-115">-BackupType</span></span>
<span data-ttu-id="0f33a-116">Określa typ kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="0f33a-116">Specifies the backup type.</span></span>
<span data-ttu-id="0f33a-117">Prawidłowe wartości to: LocalSnapshot oraz CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="0f33a-117">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f33a-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="0f33a-118">-Enabled</span></span>
<span data-ttu-id="0f33a-119">Wskazuje, czy włączyć harmonogram wykonywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="0f33a-119">Indicates whether to enable the backup schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f33a-120">-ID</span><span class="sxs-lookup"><span data-stu-id="0f33a-120">-Id</span></span>
<span data-ttu-id="0f33a-121">Określa identyfikator wystąpienia harmonogramu kopii zapasowych do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="0f33a-121">Specifies the instance ID of the backup schedule to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f33a-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="0f33a-122">-Profile</span></span>
<span data-ttu-id="0f33a-123">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0f33a-123">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="0f33a-124">-Recurrencetypetype</span><span class="sxs-lookup"><span data-stu-id="0f33a-124">-RecurrenceType</span></span>
<span data-ttu-id="0f33a-125">Określa typ cyklu dla tego harmonogramu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="0f33a-125">Specifies the type of recurrence for this backup schedule.</span></span>
<span data-ttu-id="0f33a-126">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="0f33a-126">Valid values are:</span></span> 

- <span data-ttu-id="0f33a-127">Minut</span><span class="sxs-lookup"><span data-stu-id="0f33a-127">Minutes</span></span>
- <span data-ttu-id="0f33a-128">Godzinowego</span><span class="sxs-lookup"><span data-stu-id="0f33a-128">Hourly</span></span>
- <span data-ttu-id="0f33a-129">Dobow</span><span class="sxs-lookup"><span data-stu-id="0f33a-129">Daily</span></span>
- <span data-ttu-id="0f33a-130">Weekly</span><span class="sxs-lookup"><span data-stu-id="0f33a-130">Weekly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f33a-131">-RecurrenceValue</span><span class="sxs-lookup"><span data-stu-id="0f33a-131">-RecurrenceValue</span></span>
<span data-ttu-id="0f33a-132">Określa, jak często ma być wykonywane wykonywanie kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="0f33a-132">Specifies how often to make a backup.</span></span>
<span data-ttu-id="0f33a-133">W tym parametrze jest używana jednostka określona przez parametr *cykliczntype* .</span><span class="sxs-lookup"><span data-stu-id="0f33a-133">This parameter uses the unit specified by the *RecurrenceType* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f33a-134">-RetentionCount</span><span class="sxs-lookup"><span data-stu-id="0f33a-134">-RetentionCount</span></span>
<span data-ttu-id="0f33a-135">Określa liczbę dni, przez które mają być zachowywane kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="0f33a-135">Specifies the number of days to keep a backup.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f33a-136">-StartFromDateTime</span><span class="sxs-lookup"><span data-stu-id="0f33a-136">-StartFromDateTime</span></span>
<span data-ttu-id="0f33a-137">Określa datę, od której należy zacząć tworzenie kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="0f33a-137">Specifies the date from which to start making backups.</span></span>
<span data-ttu-id="0f33a-138">Wartość domyślna to bieżąca godzina.</span><span class="sxs-lookup"><span data-stu-id="0f33a-138">The default value is the current time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f33a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f33a-139">CommonParameters</span></span>
<span data-ttu-id="0f33a-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f33a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f33a-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f33a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f33a-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f33a-142">INPUTS</span></span>

### <span data-ttu-id="0f33a-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0f33a-143">None</span></span>

## <span data-ttu-id="0f33a-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0f33a-144">OUTPUTS</span></span>

### <span data-ttu-id="0f33a-145">BackupScheduleUpdateRequest</span><span class="sxs-lookup"><span data-stu-id="0f33a-145">BackupScheduleUpdateRequest</span></span>
<span data-ttu-id="0f33a-146">To polecenie cmdlet zwraca obiekt **BackupScheduleUpdateRequest** , który zawiera informacje o zaktualizowanych harmonogramach kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="0f33a-146">This cmdlet returns a **BackupScheduleUpdateRequest** object that contains information about updated backup schedules.</span></span>

## <span data-ttu-id="0f33a-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0f33a-147">NOTES</span></span>

## <span data-ttu-id="0f33a-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f33a-148">RELATED LINKS</span></span>

[<span data-ttu-id="0f33a-149">Nowe — AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="0f33a-149">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)

[<span data-ttu-id="0f33a-150">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="0f33a-150">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)



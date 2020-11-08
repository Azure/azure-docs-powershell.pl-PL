---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EE7EC812-640B-4672-B23C-673F912F0EDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 945d06ddc1be6d2b0864b0421a5a087e14d98218
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054494"
---
# <span data-ttu-id="7f0b0-101">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="7f0b0-101">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>

## <span data-ttu-id="7f0b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f0b0-102">SYNOPSIS</span></span>
<span data-ttu-id="7f0b0-103">Tworzy obiekt konfiguracji Harmonogram kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-103">Creates a backup schedule configuration object.</span></span>

## <span data-ttu-id="7f0b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f0b0-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] -Enabled <Boolean>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7f0b0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7f0b0-105">DESCRIPTION</span></span>
<span data-ttu-id="7f0b0-106">Polecenie cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** tworzy obiekt konfiguracji **BackupScheduleBase** .</span><span class="sxs-lookup"><span data-stu-id="7f0b0-106">The **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet creates a **BackupScheduleBase** configuration object.</span></span>
<span data-ttu-id="7f0b0-107">Ten obiekt konfiguracji służy do tworzenia nowych zasad tworzenia kopii zapasowych przy użyciu polecenia cmdlet **New-AzureStorSimpleDeviceBackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="7f0b0-107">Use this configuration object to create new backup policy by using the **New-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="7f0b0-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f0b0-108">EXAMPLES</span></span>

### <span data-ttu-id="7f0b0-109">Przykład 1. Tworzenie kopii zapasowej obiektu konfiguracji</span><span class="sxs-lookup"><span data-stu-id="7f0b0-109">Example 1: Create a backup configuration object</span></span>
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 1 -RetentionCount 100 -Enabled $True
VERBOSE: ClientRequestId: 426a79ee-fed3-4d3d-9123-e371f83222b3_PS


BackupType     : CloudSnapshot
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 100
StartTime      : 2014-12-16T00:37:19+05:30
Status         : Enabled
```

<span data-ttu-id="7f0b0-110">To polecenie tworzy obiekt bazowy harmonogramu kopii zapasowej dla kopii zapasowych migawek w chmurze.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-110">This command creates a backup schedule base object for cloud snapshot backups.</span></span>
<span data-ttu-id="7f0b0-111">Kopia zapasowa jest wykonywana codziennie, a kopie zapasowe są zachowywane przez 100 dni.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-111">The backup occurs every day, and the backups are kept for 100 days.</span></span>
<span data-ttu-id="7f0b0-112">Ten harmonogram jest włączony od domyślnego czasu, który jest bieżącą godziną.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-112">This schedule is enabled from the default time, which is the current time.</span></span>

## <span data-ttu-id="7f0b0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f0b0-113">PARAMETERS</span></span>

### <span data-ttu-id="7f0b0-114">-Backuptype</span><span class="sxs-lookup"><span data-stu-id="7f0b0-114">-BackupType</span></span>
<span data-ttu-id="7f0b0-115">Określa typ kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-115">Specifies the backup type.</span></span>
<span data-ttu-id="7f0b0-116">Prawidłowe wartości to: LocalSnapshot oraz CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-116">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

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

### <span data-ttu-id="7f0b0-117">-Enabled</span><span class="sxs-lookup"><span data-stu-id="7f0b0-117">-Enabled</span></span>
<span data-ttu-id="7f0b0-118">Wskazuje, czy włączyć harmonogram wykonywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-118">Indicates whether to enable the backup schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f0b0-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="7f0b0-119">-Profile</span></span>
<span data-ttu-id="7f0b0-120">Określa Profil platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="7f0b0-121">-Recurrencetypetype</span><span class="sxs-lookup"><span data-stu-id="7f0b0-121">-RecurrenceType</span></span>
<span data-ttu-id="7f0b0-122">Określa typ cyklu dla tego harmonogramu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-122">Specifies the type of recurrence for this backup schedule.</span></span>
<span data-ttu-id="7f0b0-123">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="7f0b0-123">Valid values are:</span></span> 

- <span data-ttu-id="7f0b0-124">Minut</span><span class="sxs-lookup"><span data-stu-id="7f0b0-124">Minutes</span></span>
- <span data-ttu-id="7f0b0-125">Godzinowego</span><span class="sxs-lookup"><span data-stu-id="7f0b0-125">Hourly</span></span>
- <span data-ttu-id="7f0b0-126">Dobow</span><span class="sxs-lookup"><span data-stu-id="7f0b0-126">Daily</span></span>
- <span data-ttu-id="7f0b0-127">Weekly</span><span class="sxs-lookup"><span data-stu-id="7f0b0-127">Weekly</span></span>

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

### <span data-ttu-id="7f0b0-128">-RecurrenceValue</span><span class="sxs-lookup"><span data-stu-id="7f0b0-128">-RecurrenceValue</span></span>
<span data-ttu-id="7f0b0-129">Określa, jak często ma być wykonywane wykonywanie kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-129">Specifies how often to make a backup.</span></span>
<span data-ttu-id="7f0b0-130">W tym parametrze jest używana jednostka określona przez parametr *cykliczntype* .</span><span class="sxs-lookup"><span data-stu-id="7f0b0-130">This parameter uses the unit specified by the *RecurrenceType* parameter.</span></span>

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

### <span data-ttu-id="7f0b0-131">-RetentionCount</span><span class="sxs-lookup"><span data-stu-id="7f0b0-131">-RetentionCount</span></span>
<span data-ttu-id="7f0b0-132">Określa liczbę dni, przez które mają być zachowywane kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-132">Specifies the number of days to keep a backup.</span></span>

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

### <span data-ttu-id="7f0b0-133">-StartFromDateTime</span><span class="sxs-lookup"><span data-stu-id="7f0b0-133">-StartFromDateTime</span></span>
<span data-ttu-id="7f0b0-134">Określa datę, od której należy zacząć tworzenie kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-134">Specifies the date from which to start making backups.</span></span>
<span data-ttu-id="7f0b0-135">Wartość domyślna to bieżąca godzina.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-135">The default value is the current time.</span></span>

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

### <span data-ttu-id="7f0b0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f0b0-136">CommonParameters</span></span>
<span data-ttu-id="7f0b0-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f0b0-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f0b0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f0b0-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f0b0-139">INPUTS</span></span>

### <span data-ttu-id="7f0b0-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7f0b0-140">None</span></span>

## <span data-ttu-id="7f0b0-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f0b0-141">OUTPUTS</span></span>

### <span data-ttu-id="7f0b0-142">BackupScheduleBase</span><span class="sxs-lookup"><span data-stu-id="7f0b0-142">BackupScheduleBase</span></span>
<span data-ttu-id="7f0b0-143">To polecenie cmdlet zwraca obiekt **BackupScheduleBase** .</span><span class="sxs-lookup"><span data-stu-id="7f0b0-143">This cmdlet returns a **BackupScheduleBase** object.</span></span>
<span data-ttu-id="7f0b0-144">Utwórz nowe zasady tworzenia kopii zapasowych przy użyciu **BackupScheduleBase** .</span><span class="sxs-lookup"><span data-stu-id="7f0b0-144">Use a **BackupScheduleBase** to construct new backup policy.</span></span>

## <span data-ttu-id="7f0b0-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f0b0-145">NOTES</span></span>

## <span data-ttu-id="7f0b0-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f0b0-146">RELATED LINKS</span></span>

[<span data-ttu-id="7f0b0-147">Nowe — AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="7f0b0-147">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)

[<span data-ttu-id="7f0b0-148">Nowe — AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="7f0b0-148">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)



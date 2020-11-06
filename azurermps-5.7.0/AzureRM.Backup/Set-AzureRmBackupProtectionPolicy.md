---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 7d41abd1d56bab4df0d716c3a9d11ea14140b784
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550640"
---
# <span data-ttu-id="f2af4-101">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f2af4-101">Set-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="f2af4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2af4-102">SYNOPSIS</span></span>
<span data-ttu-id="f2af4-103">Modyfikuje istniejące zasady ochrony.</span><span class="sxs-lookup"><span data-stu-id="f2af4-103">Modifies an existing protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2af4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2af4-104">SYNTAX</span></span>

### <span data-ttu-id="f2af4-105">NoScheduleParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f2af4-105">NoScheduleParamSet (Default)</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2af4-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="f2af4-106">DailyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2af4-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="f2af4-107">WeeklyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2af4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f2af4-108">DESCRIPTION</span></span>
<span data-ttu-id="f2af4-109">Polecenie cmdlet **Set-AzureRmBackupProtectionPolicy** modyfikuje istniejące zasady ochrony w usłudze Kopia zapasowa Azure.</span><span class="sxs-lookup"><span data-stu-id="f2af4-109">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing protection policy in Azure Backup.</span></span>
<span data-ttu-id="f2af4-110">Można zmodyfikować następujące składniki zasad ochrony:</span><span class="sxs-lookup"><span data-stu-id="f2af4-110">You can modify the following protection policy components:</span></span> 

- <span data-ttu-id="f2af4-111">Nazwę</span><span class="sxs-lookup"><span data-stu-id="f2af4-111">Name</span></span>
- <span data-ttu-id="f2af4-112">Harmonogram kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="f2af4-112">Backup schedule</span></span>
- <span data-ttu-id="f2af4-113">Zasady przechowywania</span><span class="sxs-lookup"><span data-stu-id="f2af4-113">Retention policies</span></span>

<span data-ttu-id="f2af4-114">Wszelkie zmiany mogą mieć wpływ na wykonywanie kopii zapasowych i zachowywanie elementów skojarzonych z tymi zasadami.</span><span class="sxs-lookup"><span data-stu-id="f2af4-114">Any change might affect the backup and retention of the items associated with the policy.</span></span>

## <span data-ttu-id="f2af4-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2af4-115">EXAMPLES</span></span>

## <span data-ttu-id="f2af4-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2af4-116">PARAMETERS</span></span>

### <span data-ttu-id="f2af4-117">-Bez przestojów</span><span class="sxs-lookup"><span data-stu-id="f2af4-117">-BackupTime</span></span>
<span data-ttu-id="f2af4-118">Określa nową godzinę utworzenia kopii zapasowej, na przykład obiekt **DateTime** , dla zasady.</span><span class="sxs-lookup"><span data-stu-id="f2af4-118">Specifies the new backup time of day, as a **DateTime** object, for the policy.</span></span>
<span data-ttu-id="f2af4-119">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="f2af4-119">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="f2af4-120">Aby uzyskać informacje o obiektach **DateTime** , wpisz `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="f2af4-120">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2af4-121">-Codziennie</span><span class="sxs-lookup"><span data-stu-id="f2af4-121">-Daily</span></span>
<span data-ttu-id="f2af4-122">Wskazuje, że operacja tworzenia kopii zapasowej jest uruchamiana w harmonogramie dziennym.</span><span class="sxs-lookup"><span data-stu-id="f2af4-122">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2af4-123">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="f2af4-123">-DaysOfWeek</span></span>
<span data-ttu-id="f2af4-124">Określa tablicę dni tygodnia.</span><span class="sxs-lookup"><span data-stu-id="f2af4-124">Specifies an array of days of the week.</span></span>
<span data-ttu-id="f2af4-125">Te zasady uruchamiają kopie zapasowe w dniach określonych przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f2af4-125">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="f2af4-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f2af4-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f2af4-127">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="f2af4-127">Monday</span></span> 
- <span data-ttu-id="f2af4-128">Wtorku</span><span class="sxs-lookup"><span data-stu-id="f2af4-128">Tuesday</span></span> 
- <span data-ttu-id="f2af4-129">Środa</span><span class="sxs-lookup"><span data-stu-id="f2af4-129">Wednesday</span></span> 
- <span data-ttu-id="f2af4-130">Czwartek</span><span class="sxs-lookup"><span data-stu-id="f2af4-130">Thursday</span></span> 
- <span data-ttu-id="f2af4-131">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="f2af4-131">Friday</span></span> 
- <span data-ttu-id="f2af4-132">Sobota</span><span class="sxs-lookup"><span data-stu-id="f2af4-132">Saturday</span></span> 
- <span data-ttu-id="f2af4-133">Niedziele</span><span class="sxs-lookup"><span data-stu-id="f2af4-133">Sunday</span></span>

```yaml
Type: String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2af4-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2af4-134">-DefaultProfile</span></span>
<span data-ttu-id="f2af4-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f2af4-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2af4-136">-NewName</span><span class="sxs-lookup"><span data-stu-id="f2af4-136">-NewName</span></span>
<span data-ttu-id="f2af4-137">Określa nową nazwę zasady.</span><span class="sxs-lookup"><span data-stu-id="f2af4-137">Specifies the new name for the policy.</span></span>
<span data-ttu-id="f2af4-138">Ta nazwa musi być unikatowa w magazynie.</span><span class="sxs-lookup"><span data-stu-id="f2af4-138">This name must be unique in a vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2af4-139">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f2af4-139">-ProtectionPolicy</span></span>
<span data-ttu-id="f2af4-140">Określa zasady ochrony, które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2af4-140">Specifies protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="f2af4-141">Aby uzyskać obiekt **AzureRmBackupProtectionPolicy** , użyj polecenia cmdlet Get-AzureRmBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="f2af4-141">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2af4-142">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f2af4-142">-RetentionPolicy</span></span>
<span data-ttu-id="f2af4-143">Określa tablicę zasad przechowywania zasad tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="f2af4-143">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="f2af4-144">Aby uzyskać obiekty **AzureRmBackupRetentionPolicy** , użyj polecenia cmdlet New-AzureRmBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="f2af4-144">To obtain **AzureRmBackupRetentionPolicy** objects, use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2af4-145">-Co tydzień</span><span class="sxs-lookup"><span data-stu-id="f2af4-145">-Weekly</span></span>
<span data-ttu-id="f2af4-146">Wskazuje, że operacja tworzenia kopii zapasowej jest wykonywana w harmonogramie tygodniowym.</span><span class="sxs-lookup"><span data-stu-id="f2af4-146">Indicates that the backup operation runs on a Weekly schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2af4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2af4-147">CommonParameters</span></span>
<span data-ttu-id="f2af4-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2af4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2af4-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2af4-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2af4-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2af4-150">INPUTS</span></span>

### <span data-ttu-id="f2af4-151">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f2af4-151">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="f2af4-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2af4-152">OUTPUTS</span></span>

### <span data-ttu-id="f2af4-153">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f2af4-153">None</span></span>

## <span data-ttu-id="f2af4-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2af4-154">NOTES</span></span>

## <span data-ttu-id="f2af4-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2af4-155">RELATED LINKS</span></span>

[<span data-ttu-id="f2af4-156">Nowe — AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f2af4-156">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)



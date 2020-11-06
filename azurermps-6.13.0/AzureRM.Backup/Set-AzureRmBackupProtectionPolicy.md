---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: caf6394ce84b18bd8e36b4504173fe7f7bb07fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541952"
---
# <span data-ttu-id="52d47-101">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="52d47-101">Set-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="52d47-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="52d47-102">SYNOPSIS</span></span>
<span data-ttu-id="52d47-103">Modyfikuje istniejące zasady ochrony.</span><span class="sxs-lookup"><span data-stu-id="52d47-103">Modifies an existing protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52d47-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="52d47-104">SYNTAX</span></span>

### <span data-ttu-id="52d47-105">NoScheduleParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="52d47-105">NoScheduleParamSet (Default)</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52d47-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="52d47-106">DailyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52d47-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="52d47-107">WeeklyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52d47-108">Opis</span><span class="sxs-lookup"><span data-stu-id="52d47-108">DESCRIPTION</span></span>
<span data-ttu-id="52d47-109">Polecenie cmdlet **Set-AzureRmBackupProtectionPolicy** modyfikuje istniejące zasady ochrony w usłudze Kopia zapasowa Azure.</span><span class="sxs-lookup"><span data-stu-id="52d47-109">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing protection policy in Azure Backup.</span></span>
<span data-ttu-id="52d47-110">Można zmodyfikować następujące składniki zasad ochrony:</span><span class="sxs-lookup"><span data-stu-id="52d47-110">You can modify the following protection policy components:</span></span> 
- <span data-ttu-id="52d47-111">Nazwę</span><span class="sxs-lookup"><span data-stu-id="52d47-111">Name</span></span>
- <span data-ttu-id="52d47-112">Harmonogram kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="52d47-112">Backup schedule</span></span>
- <span data-ttu-id="52d47-113">Zasady przechowywania wszelkie zmiany mogą mieć wpływ na wykonywanie kopii zapasowych i zachowywanie elementów skojarzonych z zasadami.</span><span class="sxs-lookup"><span data-stu-id="52d47-113">Retention policies Any change might affect the backup and retention of the items associated with the policy.</span></span>

## <span data-ttu-id="52d47-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="52d47-114">EXAMPLES</span></span>

## <span data-ttu-id="52d47-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="52d47-115">PARAMETERS</span></span>

### <span data-ttu-id="52d47-116">-Bez przestojów</span><span class="sxs-lookup"><span data-stu-id="52d47-116">-BackupTime</span></span>
<span data-ttu-id="52d47-117">Określa nową godzinę utworzenia kopii zapasowej, na przykład obiekt **DateTime** , dla zasady.</span><span class="sxs-lookup"><span data-stu-id="52d47-117">Specifies the new backup time of day, as a **DateTime** object, for the policy.</span></span>
<span data-ttu-id="52d47-118">Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="52d47-118">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="52d47-119">Aby uzyskać informacje o obiektach **DateTime** , wpisz `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="52d47-119">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d47-120">-Codziennie</span><span class="sxs-lookup"><span data-stu-id="52d47-120">-Daily</span></span>
<span data-ttu-id="52d47-121">Wskazuje, że operacja tworzenia kopii zapasowej jest uruchamiana w harmonogramie dziennym.</span><span class="sxs-lookup"><span data-stu-id="52d47-121">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d47-122">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="52d47-122">-DaysOfWeek</span></span>
<span data-ttu-id="52d47-123">Określa tablicę dni tygodnia.</span><span class="sxs-lookup"><span data-stu-id="52d47-123">Specifies an array of days of the week.</span></span>
<span data-ttu-id="52d47-124">Te zasady uruchamiają kopie zapasowe w dniach określonych przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="52d47-124">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="52d47-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="52d47-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="52d47-126">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="52d47-126">Monday</span></span> 
- <span data-ttu-id="52d47-127">Wtorku</span><span class="sxs-lookup"><span data-stu-id="52d47-127">Tuesday</span></span> 
- <span data-ttu-id="52d47-128">Środa</span><span class="sxs-lookup"><span data-stu-id="52d47-128">Wednesday</span></span> 
- <span data-ttu-id="52d47-129">Czwartek</span><span class="sxs-lookup"><span data-stu-id="52d47-129">Thursday</span></span> 
- <span data-ttu-id="52d47-130">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="52d47-130">Friday</span></span> 
- <span data-ttu-id="52d47-131">Sobota</span><span class="sxs-lookup"><span data-stu-id="52d47-131">Saturday</span></span> 
- <span data-ttu-id="52d47-132">Niedziele</span><span class="sxs-lookup"><span data-stu-id="52d47-132">Sunday</span></span>

```yaml
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d47-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52d47-133">-DefaultProfile</span></span>
<span data-ttu-id="52d47-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="52d47-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52d47-135">-NewName</span><span class="sxs-lookup"><span data-stu-id="52d47-135">-NewName</span></span>
<span data-ttu-id="52d47-136">Określa nową nazwę zasady.</span><span class="sxs-lookup"><span data-stu-id="52d47-136">Specifies the new name for the policy.</span></span>
<span data-ttu-id="52d47-137">Ta nazwa musi być unikatowa w magazynie.</span><span class="sxs-lookup"><span data-stu-id="52d47-137">This name must be unique in a vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d47-138">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="52d47-138">-ProtectionPolicy</span></span>
<span data-ttu-id="52d47-139">Określa zasady ochrony, które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52d47-139">Specifies protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="52d47-140">Aby uzyskać obiekt **AzureRmBackupProtectionPolicy** , użyj polecenia cmdlet Get-AzureRmBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="52d47-140">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52d47-141">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="52d47-141">-RetentionPolicy</span></span>
<span data-ttu-id="52d47-142">Określa tablicę zasad przechowywania zasad tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="52d47-142">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="52d47-143">Aby uzyskać obiekty **AzureRmBackupRetentionPolicy** , użyj polecenia cmdlet New-AzureRmBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="52d47-143">To obtain **AzureRmBackupRetentionPolicy** objects, use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d47-144">-Co tydzień</span><span class="sxs-lookup"><span data-stu-id="52d47-144">-Weekly</span></span>
<span data-ttu-id="52d47-145">Wskazuje, że operacja tworzenia kopii zapasowej jest wykonywana w harmonogramie tygodniowym.</span><span class="sxs-lookup"><span data-stu-id="52d47-145">Indicates that the backup operation runs on a Weekly schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d47-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d47-146">CommonParameters</span></span>
<span data-ttu-id="52d47-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52d47-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d47-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52d47-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d47-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52d47-149">INPUTS</span></span>

### <span data-ttu-id="52d47-150">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="52d47-150">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy</span></span>
<span data-ttu-id="52d47-151">Parametry: ProtectionPolicy (ByValue)</span><span class="sxs-lookup"><span data-stu-id="52d47-151">Parameters: ProtectionPolicy (ByValue)</span></span>

## <span data-ttu-id="52d47-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="52d47-152">OUTPUTS</span></span>

### <span data-ttu-id="52d47-153">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="52d47-153">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="52d47-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="52d47-154">NOTES</span></span>

## <span data-ttu-id="52d47-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52d47-155">RELATED LINKS</span></span>

[<span data-ttu-id="52d47-156">Nowe — AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="52d47-156">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)



---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/set-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 5a60320736e65fae83547bbf9b2825979f73601e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526677"
---
# <span data-ttu-id="4dd10-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4dd10-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="4dd10-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4dd10-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd10-103">Modyfikuje zasady ochrony kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="4dd10-103">Modifies a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4dd10-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4dd10-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase>
 [[-RetentionPolicy] <RetentionPolicyBase>] [[-SchedulePolicy] <SchedulePolicyBase>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dd10-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4dd10-105">DESCRIPTION</span></span>
<span data-ttu-id="4dd10-106">Polecenie cmdlet **Set-AzureRmBackupProtectionPolicy** modyfikuje istniejące zasady ochrony kopii zapasowych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4dd10-106">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="4dd10-107">Można modyfikować składniki Harmonogram kopii zapasowych i zasady przechowywania.</span><span class="sxs-lookup"><span data-stu-id="4dd10-107">You can modify the Backup schedule and retention policy components.</span></span>

<span data-ttu-id="4dd10-108">Wszelkie wprowadzone zmiany mają wpływ na wykonywanie kopii zapasowych i zachowywanie elementów skojarzonych z tymi zasadami.</span><span class="sxs-lookup"><span data-stu-id="4dd10-108">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>

<span data-ttu-id="4dd10-109">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="4dd10-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="4dd10-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4dd10-110">EXAMPLES</span></span>

### <span data-ttu-id="4dd10-111">Przykład 1. modyfikacja zasad ochrony kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="4dd10-111">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="4dd10-112">Pierwsze polecenie uzyskuje podstawowy obiekt SchedulePolicy, a następnie zapisuje go w zmiennej $SchPol.</span><span class="sxs-lookup"><span data-stu-id="4dd10-112">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="4dd10-113">Drugie polecenie usuwa wszystkie zaplanowane godziny wykonania z zasad harmonogramu w $SchPol.</span><span class="sxs-lookup"><span data-stu-id="4dd10-113">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>

<span data-ttu-id="4dd10-114">W trzecim poleceniu użyto polecenia cmdlet Get-Date, aby uzyskać bieżącą datę i godzinę, a następnie przechowywać ją w zmiennej $DT.</span><span class="sxs-lookup"><span data-stu-id="4dd10-114">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>

<span data-ttu-id="4dd10-115">Czwarte polecenie umożliwia dodanie daty i godziny w $DT do harmonogramu czasu uruchomienia zasad harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="4dd10-115">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>

<span data-ttu-id="4dd10-116">W piątym poleceniu jest pobierany podstawowy obiekt zasady przechowywania, a następnie jest on przechowywany w zmiennej $RetPol.</span><span class="sxs-lookup"><span data-stu-id="4dd10-116">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="4dd10-117">Szóste polecenie ustawia czas trwania przechowywania na 365 dni.</span><span class="sxs-lookup"><span data-stu-id="4dd10-117">The sixth command sets the retention duration to 365 days.</span></span>

<span data-ttu-id="4dd10-118">Po siódmym poleceniu otrzymano zasady ochrony kopii zapasowej o nazwie NewPolicy, a następnie zapisuje je w zmiennej $Pol.</span><span class="sxs-lookup"><span data-stu-id="4dd10-118">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="4dd10-119">Polecenie ostatnie modyfikuje zasady ochrony kopii zapasowej w $Pol przy użyciu zasad harmonogramu w $SchPol i zasad przechowywania w $RetPol.</span><span class="sxs-lookup"><span data-stu-id="4dd10-119">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="4dd10-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4dd10-120">PARAMETERS</span></span>

### <span data-ttu-id="4dd10-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dd10-121">-DefaultProfile</span></span>
<span data-ttu-id="4dd10-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4dd10-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4dd10-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="4dd10-123">-Policy</span></span>
<span data-ttu-id="4dd10-124">Określa zasady ochrony kopii zapasowej, które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dd10-124">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="4dd10-125">Aby uzyskać obiekt **BackupProtectionPolicy** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="4dd10-125">To obtain a **BackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4dd10-126">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4dd10-126">-RetentionPolicy</span></span>
<span data-ttu-id="4dd10-127">Określa podstawowe zasady przechowywania.</span><span class="sxs-lookup"><span data-stu-id="4dd10-127">Specifies the base retention policy.</span></span>
<span data-ttu-id="4dd10-128">Aby uzyskać obiekt **RetentionPolicy** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="4dd10-128">To obtain a **RetentionPolicy** object, use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd10-129">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="4dd10-129">-SchedulePolicy</span></span>
<span data-ttu-id="4dd10-130">Określa obiekt zasad dotyczących harmonogramu podstawowego.</span><span class="sxs-lookup"><span data-stu-id="4dd10-130">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="4dd10-131">Aby uzyskać obiekt **SchedulePolicy** , użyj obiektu Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.</span><span class="sxs-lookup"><span data-stu-id="4dd10-131">To obtain a **SchedulePolicy** object, use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd10-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4dd10-132">-Confirm</span></span>
<span data-ttu-id="4dd10-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dd10-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd10-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dd10-134">-WhatIf</span></span>
<span data-ttu-id="4dd10-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dd10-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4dd10-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4dd10-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd10-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd10-137">CommonParameters</span></span>
<span data-ttu-id="4dd10-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dd10-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd10-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dd10-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd10-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4dd10-140">INPUTS</span></span>

### <span data-ttu-id="4dd10-141">PolicyBase</span><span class="sxs-lookup"><span data-stu-id="4dd10-141">PolicyBase</span></span>
<span data-ttu-id="4dd10-142">Parametr "Policy" przyjmuje wartość typu "PolicyBase" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="4dd10-142">Parameter 'Policy' accepts value of type 'PolicyBase' from the pipeline</span></span>

## <span data-ttu-id="4dd10-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4dd10-143">OUTPUTS</span></span>

### <span data-ttu-id="4dd10-144">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. modele. JobBase]</span><span class="sxs-lookup"><span data-stu-id="4dd10-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="4dd10-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4dd10-145">NOTES</span></span>

## <span data-ttu-id="4dd10-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4dd10-146">RELATED LINKS</span></span>

[<span data-ttu-id="4dd10-147">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4dd10-147">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="4dd10-148">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="4dd10-148">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="4dd10-149">Nowe — AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4dd10-149">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="4dd10-150">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4dd10-150">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)



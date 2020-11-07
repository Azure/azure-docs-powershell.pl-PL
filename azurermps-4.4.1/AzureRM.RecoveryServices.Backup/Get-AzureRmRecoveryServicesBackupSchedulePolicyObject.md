---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: fcf5bec22dffc18d6c4f9950d8dfb3e5b37332a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718998"
---
# <span data-ttu-id="6212e-101">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="6212e-101">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="6212e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6212e-102">SYNOPSIS</span></span>
<span data-ttu-id="6212e-103">Pobiera obiekt zasad dotyczących harmonogramu podstawowego.</span><span class="sxs-lookup"><span data-stu-id="6212e-103">Gets a base schedule policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6212e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6212e-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6212e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6212e-105">DESCRIPTION</span></span>
<span data-ttu-id="6212e-106">Polecenie cmdlet **Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** pobiera **AzureRMRecoveryServicesSchedulePolicyObject** bazowy.</span><span class="sxs-lookup"><span data-stu-id="6212e-106">The **Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="6212e-107">Ten obiekt nie jest utrwalony w systemie.</span><span class="sxs-lookup"><span data-stu-id="6212e-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="6212e-108">Jest to obiekt tymczasowy, który można manipulować i używać z poleceniem cmdlet New-AzureRmRecoveryServicesBackupProtectionPolicy, aby utworzyć nowe zasady ochrony kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="6212e-108">It is temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="6212e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6212e-109">EXAMPLES</span></span>

### <span data-ttu-id="6212e-110">Przykład 1. Ustaw częstotliwość harmonogramu na co tydzień</span><span class="sxs-lookup"><span data-stu-id="6212e-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="6212e-111">Pierwsze polecenie pobiera obiekt zasady przechowywania, a następnie zapisuje go w zmiennej $RetPol.</span><span class="sxs-lookup"><span data-stu-id="6212e-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="6212e-112">Drugie polecenie pobiera obiekt zasad harmonogramu, a następnie zapisuje go w zmiennej $SchPol.</span><span class="sxs-lookup"><span data-stu-id="6212e-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="6212e-113">Trzecia zmiana częstotliwości dla zasad harmonogramu na co tydzień.</span><span class="sxs-lookup"><span data-stu-id="6212e-113">The third command changes the frequency for the schedule policy to weekly.</span></span>

<span data-ttu-id="6212e-114">Ostatnie polecenie tworzy zasady ochrony kopii zapasowej ze zaktualizowanym harmonogramem.</span><span class="sxs-lookup"><span data-stu-id="6212e-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="6212e-115">Przykład 2: Ustawianie czasu wykonywania kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="6212e-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="6212e-116">Pierwsze polecenie powoduje wyświetlenie obiektu zasad harmonogramu, a następnie zapisanie go w zmiennej $SchPol.</span><span class="sxs-lookup"><span data-stu-id="6212e-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="6212e-117">Drugie polecenie usuwa wszystkie zaplanowane czasy uruchamiania z $SchPol.</span><span class="sxs-lookup"><span data-stu-id="6212e-117">The second command removes all scheduled run times from $SchPol.</span></span>

<span data-ttu-id="6212e-118">W trzecim poleceniu jest pobierana aktualna Data i godzina, a następnie jest ona przechowywana w zmiennej $DT.</span><span class="sxs-lookup"><span data-stu-id="6212e-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>

<span data-ttu-id="6212e-119">Czwarte polecenie zamienia zaplanowane czasy uruchamiania na bieżącą godzinę.</span><span class="sxs-lookup"><span data-stu-id="6212e-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="6212e-120">Kopię zapasową można wykonać tylko raz dziennie, aby zresetować czas wykonywania kopii zapasowej, zastępując oryginalny harmonogram.</span><span class="sxs-lookup"><span data-stu-id="6212e-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>

<span data-ttu-id="6212e-121">Ostatnie polecenie tworzy zasady ochrony kopii zapasowych przy użyciu nowego harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="6212e-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="6212e-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6212e-122">PARAMETERS</span></span>

### <span data-ttu-id="6212e-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="6212e-123">-BackupManagementType</span></span>
<span data-ttu-id="6212e-124">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="6212e-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="6212e-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6212e-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6212e-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="6212e-126">AzureVM</span></span> 
- <span data-ttu-id="6212e-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="6212e-127">AzureSQLDatabase</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6212e-128">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="6212e-128">-WorkloadType</span></span>
<span data-ttu-id="6212e-129">Określa typ obciążenia pracą.</span><span class="sxs-lookup"><span data-stu-id="6212e-129">Specifies the workload type.</span></span>
<span data-ttu-id="6212e-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6212e-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6212e-131">AzureVM</span><span class="sxs-lookup"><span data-stu-id="6212e-131">AzureVM</span></span> 
- <span data-ttu-id="6212e-132">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="6212e-132">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6212e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6212e-133">-DefaultProfile</span></span>
<span data-ttu-id="6212e-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6212e-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6212e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6212e-135">CommonParameters</span></span>
<span data-ttu-id="6212e-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6212e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6212e-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6212e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6212e-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6212e-138">INPUTS</span></span>

## <span data-ttu-id="6212e-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6212e-139">OUTPUTS</span></span>

### <span data-ttu-id="6212e-140">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="6212e-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="6212e-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6212e-141">NOTES</span></span>

## <span data-ttu-id="6212e-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6212e-142">RELATED LINKS</span></span>

[<span data-ttu-id="6212e-143">Nowe — AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6212e-143">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="6212e-144">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6212e-144">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


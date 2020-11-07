---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: b3a1c990f8dff3b91c9e46fd1f01da734e47f963
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708656"
---
# <span data-ttu-id="bb315-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="bb315-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="bb315-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb315-102">SYNOPSIS</span></span>
<span data-ttu-id="bb315-103">Pobiera podstawowy obiekt zasad przechowywania.</span><span class="sxs-lookup"><span data-stu-id="bb315-103">Gets a base retention policy object.</span></span>

## <span data-ttu-id="bb315-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb315-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb315-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bb315-105">DESCRIPTION</span></span>
<span data-ttu-id="bb315-106">Polecenie cmdlet **Get-AzRecoveryServicesBackupRetentionPolicyObject** pobiera **AzureRMRecoveryServicesRetentionPolicyObject** bazowy.</span><span class="sxs-lookup"><span data-stu-id="bb315-106">The **Get-AzRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="bb315-107">Ten obiekt nie jest utrwalony w systemie.</span><span class="sxs-lookup"><span data-stu-id="bb315-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="bb315-108">Jest to tymczasowy obiekt, który można manipulować i używać z poleceniem cmdlet New-AzRecoveryServicesBackupProtectionPolicy, aby utworzyć nowe zasady tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="bb315-108">It is a temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="bb315-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb315-109">EXAMPLES</span></span>

### <span data-ttu-id="bb315-110">Przykład 1. Tworzenie zasad ochrony kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="bb315-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="bb315-111">Pierwsze polecenie pobiera obiekt zasady przechowywania, a następnie zapisuje go w zmiennej $RetPol.</span><span class="sxs-lookup"><span data-stu-id="bb315-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="bb315-112">Drugie polecenie ustawia czas trwania obiektu zasady przechowywania na 365 dni.</span><span class="sxs-lookup"><span data-stu-id="bb315-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="bb315-113">Trzecia komenda uzyskuje obiekt zasad harmonogramu, a następnie zapisuje go w zmiennej $SchPol.</span><span class="sxs-lookup"><span data-stu-id="bb315-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="bb315-114">Ostatnie polecenie tworzy zasady ochrony kopii zapasowej przy użyciu zasad przechowywania i harmonogramów utworzonych za pomocą poprzednich poleceń.</span><span class="sxs-lookup"><span data-stu-id="bb315-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="bb315-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb315-115">PARAMETERS</span></span>

### <span data-ttu-id="bb315-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="bb315-116">-BackupManagementType</span></span>
<span data-ttu-id="bb315-117">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="bb315-117">Specifies the Backup management type.</span></span>
<span data-ttu-id="bb315-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="bb315-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bb315-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="bb315-119">AzureVM</span></span> 
- <span data-ttu-id="bb315-120">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="bb315-120">AzureSQLDatabase</span></span>
- <span data-ttu-id="bb315-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="bb315-121">AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb315-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb315-122">-DefaultProfile</span></span>
<span data-ttu-id="bb315-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb315-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb315-124">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="bb315-124">-WorkloadType</span></span>
<span data-ttu-id="bb315-125">Określa typ obciążenia pracą.</span><span class="sxs-lookup"><span data-stu-id="bb315-125">Specifies the workload type.</span></span>
<span data-ttu-id="bb315-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="bb315-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bb315-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="bb315-127">AzureVM</span></span> 
- <span data-ttu-id="bb315-128">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="bb315-128">AzureSQLDatabase</span></span>
- <span data-ttu-id="bb315-129">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="bb315-129">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb315-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb315-130">CommonParameters</span></span>
<span data-ttu-id="bb315-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb315-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb315-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb315-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb315-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb315-133">INPUTS</span></span>

### <span data-ttu-id="bb315-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bb315-134">None</span></span>

## <span data-ttu-id="bb315-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb315-135">OUTPUTS</span></span>

### <span data-ttu-id="bb315-136">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="bb315-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="bb315-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb315-137">NOTES</span></span>

## <span data-ttu-id="bb315-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb315-138">RELATED LINKS</span></span>

[<span data-ttu-id="bb315-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="bb315-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="bb315-140">Nowe — AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="bb315-140">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)



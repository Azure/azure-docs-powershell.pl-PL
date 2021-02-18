---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: d426cd18aaf3382939e55668b1c19938319a3c51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192970"
---
# <span data-ttu-id="065b6-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="065b6-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="065b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="065b6-102">SYNOPSIS</span></span>
<span data-ttu-id="065b6-103">Pobiera obiekt podstawowych zasad przechowywania.</span><span class="sxs-lookup"><span data-stu-id="065b6-103">Gets a base retention policy object.</span></span>

## <span data-ttu-id="065b6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="065b6-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="065b6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="065b6-105">DESCRIPTION</span></span>
<span data-ttu-id="065b6-106">Polecenie cmdlet **Get-AzRecoveryServicesBackupRetentionPolicyObject** otrzymuje podstawę usługi **AzureRMRecoveryServicesRetentionPolicyObject.**</span><span class="sxs-lookup"><span data-stu-id="065b6-106">The **Get-AzRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="065b6-107">Ten obiekt nie jest utrwalony w systemie.</span><span class="sxs-lookup"><span data-stu-id="065b6-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="065b6-108">Jest to obiekt tymczasowy, który można modyfikować i używać razem z New-AzRecoveryServicesBackupProtectionPolicy cmdlet w celu utworzenia nowych zasad kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="065b6-108">It is a temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="065b6-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="065b6-109">EXAMPLES</span></span>

### <span data-ttu-id="065b6-110">Przykład 1. Tworzenie zasad ochrony kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="065b6-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="065b6-111">Pierwsze polecenie pobiera obiekt zasad przechowywania, a następnie zapisuje go w $RetPol danych.</span><span class="sxs-lookup"><span data-stu-id="065b6-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="065b6-112">Drugie polecenie ustawia czas trwania obiektu zasad przechowywania na 365 dni.</span><span class="sxs-lookup"><span data-stu-id="065b6-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="065b6-113">Trzecie polecenie pobiera obiekt zasad harmonogramu, a następnie przechowuje je w $SchPol zmienną.</span><span class="sxs-lookup"><span data-stu-id="065b6-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="065b6-114">Ostatnie polecenie tworzy zasady ochrony kopii zapasowej przy użyciu zasad przechowywania i zasad harmonogramu utworzonych za pomocą poprzednich poleceń.</span><span class="sxs-lookup"><span data-stu-id="065b6-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="065b6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="065b6-115">PARAMETERS</span></span>

### <span data-ttu-id="065b6-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="065b6-116">-BackupManagementType</span></span>
<span data-ttu-id="065b6-117">Klasa zasobów, które są chronione.</span><span class="sxs-lookup"><span data-stu-id="065b6-117">The class of resources being protected.</span></span> <span data-ttu-id="065b6-118">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="065b6-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="065b6-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="065b6-119">AzureVM</span></span> 
- <span data-ttu-id="065b6-120">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="065b6-120">AzureWorkload</span></span>
- <span data-ttu-id="065b6-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="065b6-121">AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="065b6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="065b6-122">-DefaultProfile</span></span>
<span data-ttu-id="065b6-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="065b6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="065b6-124">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="065b6-124">-WorkloadType</span></span>
<span data-ttu-id="065b6-125">Typ obciążenia zasobu.</span><span class="sxs-lookup"><span data-stu-id="065b6-125">Workload type of the resource.</span></span> <span data-ttu-id="065b6-126">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="065b6-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="065b6-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="065b6-127">AzureVM</span></span> 
- <span data-ttu-id="065b6-128">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="065b6-128">AzureFiles</span></span>
- <span data-ttu-id="065b6-129">MSSQL</span><span class="sxs-lookup"><span data-stu-id="065b6-129">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="065b6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="065b6-130">CommonParameters</span></span>
<span data-ttu-id="065b6-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="065b6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="065b6-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="065b6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="065b6-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="065b6-133">INPUTS</span></span>

### <span data-ttu-id="065b6-134">Brak</span><span class="sxs-lookup"><span data-stu-id="065b6-134">None</span></span>

## <span data-ttu-id="065b6-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="065b6-135">OUTPUTS</span></span>

### <span data-ttu-id="065b6-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="065b6-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="065b6-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="065b6-137">NOTES</span></span>

## <span data-ttu-id="065b6-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="065b6-138">RELATED LINKS</span></span>

[<span data-ttu-id="065b6-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="065b6-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="065b6-140">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="065b6-140">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)



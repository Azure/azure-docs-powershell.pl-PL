---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: 83ed9062c5ad4beb0dff9c9c89b79a443cc68a52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526697"
---
# <span data-ttu-id="ac315-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="ac315-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="ac315-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ac315-102">SYNOPSIS</span></span>
<span data-ttu-id="ac315-103">Pobiera podstawowy obiekt zasad przechowywania.</span><span class="sxs-lookup"><span data-stu-id="ac315-103">Gets a base retention policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac315-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ac315-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac315-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ac315-105">DESCRIPTION</span></span>
<span data-ttu-id="ac315-106">Polecenie cmdlet **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** pobiera **AzureRMRecoveryServicesRetentionPolicyObject** bazowy.</span><span class="sxs-lookup"><span data-stu-id="ac315-106">The **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="ac315-107">Ten obiekt nie jest utrwalony w systemie.</span><span class="sxs-lookup"><span data-stu-id="ac315-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="ac315-108">Jest to tymczasowy obiekt, który można manipulować i używać z poleceniem cmdlet New-AzureRmRecoveryServicesBackupProtectionPolicy, aby utworzyć nowe zasady tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="ac315-108">It is a temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="ac315-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ac315-109">EXAMPLES</span></span>

### <span data-ttu-id="ac315-110">Przykład 1. Tworzenie zasad ochrony kopii zapasowych</span><span class="sxs-lookup"><span data-stu-id="ac315-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="ac315-111">Pierwsze polecenie pobiera obiekt zasady przechowywania, a następnie zapisuje go w zmiennej $RetPol.</span><span class="sxs-lookup"><span data-stu-id="ac315-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="ac315-112">Drugie polecenie ustawia czas trwania obiektu zasady przechowywania na 365 dni.</span><span class="sxs-lookup"><span data-stu-id="ac315-112">The second command sets the duration for the retention policy object to 365 days.</span></span>

<span data-ttu-id="ac315-113">Trzecia komenda uzyskuje obiekt zasad harmonogramu, a następnie zapisuje go w zmiennej $SchPol.</span><span class="sxs-lookup"><span data-stu-id="ac315-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="ac315-114">Ostatnie polecenie tworzy zasady ochrony kopii zapasowej przy użyciu zasad przechowywania i harmonogramów utworzonych za pomocą poprzednich poleceń.</span><span class="sxs-lookup"><span data-stu-id="ac315-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="ac315-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac315-115">PARAMETERS</span></span>

### <span data-ttu-id="ac315-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="ac315-116">-BackupManagementType</span></span>
<span data-ttu-id="ac315-117">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="ac315-117">Specifies the Backup management type.</span></span>
<span data-ttu-id="ac315-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ac315-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ac315-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="ac315-119">AzureVM</span></span> 
- <span data-ttu-id="ac315-120">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="ac315-120">AzureSQLDatabase</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac315-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac315-121">-DefaultProfile</span></span>
<span data-ttu-id="ac315-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac315-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac315-123">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="ac315-123">-WorkloadType</span></span>
<span data-ttu-id="ac315-124">Określa typ obciążenia pracą.</span><span class="sxs-lookup"><span data-stu-id="ac315-124">Specifies the workload type.</span></span>
<span data-ttu-id="ac315-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ac315-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ac315-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="ac315-126">AzureVM</span></span> 
- <span data-ttu-id="ac315-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="ac315-127">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac315-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac315-128">CommonParameters</span></span>
<span data-ttu-id="ac315-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac315-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac315-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac315-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac315-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac315-131">INPUTS</span></span>

### <span data-ttu-id="ac315-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ac315-132">None</span></span>
<span data-ttu-id="ac315-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="ac315-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ac315-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ac315-134">OUTPUTS</span></span>

### <span data-ttu-id="ac315-135">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="ac315-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="ac315-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ac315-136">NOTES</span></span>

## <span data-ttu-id="ac315-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac315-137">RELATED LINKS</span></span>

[<span data-ttu-id="ac315-138">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="ac315-138">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="ac315-139">Nowe — AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ac315-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)



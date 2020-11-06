---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: d08bd0a02878b1b99b3243e80512df30eca6e1c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544923"
---
# <span data-ttu-id="2baed-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2baed-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="2baed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2baed-102">SYNOPSIS</span></span>
<span data-ttu-id="2baed-103">Pobiera zasady ochrony kopii zapasowej dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="2baed-103">Gets Backup protection policies for a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2baed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2baed-104">SYNTAX</span></span>

### <span data-ttu-id="2baed-105">NoParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2baed-105">NoParamSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2baed-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="2baed-106">PolicyNameParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2baed-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="2baed-107">WorkloadParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2baed-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="2baed-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2baed-109">Opis</span><span class="sxs-lookup"><span data-stu-id="2baed-109">DESCRIPTION</span></span>
<span data-ttu-id="2baed-110">Polecenie cmdlet **Get-AzureRmRecoveryServicesBackupProtectionPolicy** pobiera zasady ochrony kopii zapasowych Azure dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="2baed-110">The **Get-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="2baed-111">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="2baed-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="2baed-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2baed-112">EXAMPLES</span></span>

### <span data-ttu-id="2baed-113">Przykład 1: pobieranie wszystkich zasad w magazynie</span><span class="sxs-lookup"><span data-stu-id="2baed-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="2baed-114">To polecenie pobiera wszystkie zasady ochrony utworzone w magazynie.</span><span class="sxs-lookup"><span data-stu-id="2baed-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="2baed-115">Przykład 2: uzyskiwanie określonych zasad</span><span class="sxs-lookup"><span data-stu-id="2baed-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="2baed-116">To polecenie uzyskuje zasady ochrony o nazwie DefaultPolicy, a następnie zapisuje je w zmiennej $Pol.</span><span class="sxs-lookup"><span data-stu-id="2baed-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="2baed-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2baed-117">PARAMETERS</span></span>

### <span data-ttu-id="2baed-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="2baed-118">-BackupManagementType</span></span>
<span data-ttu-id="2baed-119">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="2baed-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="2baed-120">Obecnie obsługiwana jest tylko AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="2baed-120">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2baed-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2baed-121">-DefaultProfile</span></span>
<span data-ttu-id="2baed-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2baed-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2baed-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2baed-123">-Name</span></span>
<span data-ttu-id="2baed-124">Określa nazwę zasady.</span><span class="sxs-lookup"><span data-stu-id="2baed-124">Specifies the name of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2baed-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2baed-125">-VaultId</span></span>
<span data-ttu-id="2baed-126">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="2baed-126">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2baed-127">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="2baed-127">-WorkloadType</span></span>
<span data-ttu-id="2baed-128">Określa typ obciążenia pracą.</span><span class="sxs-lookup"><span data-stu-id="2baed-128">Specifies the workload type.</span></span>
<span data-ttu-id="2baed-129">Obecnie obsługiwana jest tylko AzureVM, AzureFiles.</span><span class="sxs-lookup"><span data-stu-id="2baed-129">Currently, only AzureVM, AzureFiles is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType]
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2baed-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2baed-130">CommonParameters</span></span>
<span data-ttu-id="2baed-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2baed-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2baed-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2baed-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2baed-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2baed-133">INPUTS</span></span>

### <span data-ttu-id="2baed-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2baed-134">System.String</span></span>
<span data-ttu-id="2baed-135">Parametry: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2baed-135">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="2baed-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2baed-136">OUTPUTS</span></span>

### <span data-ttu-id="2baed-137">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="2baed-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="2baed-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2baed-138">NOTES</span></span>

## <span data-ttu-id="2baed-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2baed-139">RELATED LINKS</span></span>

[<span data-ttu-id="2baed-140">Nowe — AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2baed-140">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="2baed-141">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2baed-141">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="2baed-142">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2baed-142">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)



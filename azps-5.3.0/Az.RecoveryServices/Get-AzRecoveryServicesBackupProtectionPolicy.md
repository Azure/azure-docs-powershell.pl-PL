---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 9595f3fc3062d6afdd5b5bbfab74f297b39b3f6c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376649"
---
# <span data-ttu-id="1e3e3-101">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1e3e3-101">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="1e3e3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1e3e3-102">SYNOPSIS</span></span>
<span data-ttu-id="1e3e3-103">Pobiera zasady ochrony kopii zapasowej dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="1e3e3-103">Gets Backup protection policies for a vault.</span></span>

## <span data-ttu-id="1e3e3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1e3e3-104">SYNTAX</span></span>

### <span data-ttu-id="1e3e3-105">NoParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1e3e3-105">NoParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e3e3-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="1e3e3-106">PolicyNameParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e3e3-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="1e3e3-107">WorkloadParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e3e3-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="1e3e3-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1e3e3-109">Opis</span><span class="sxs-lookup"><span data-stu-id="1e3e3-109">DESCRIPTION</span></span>
<span data-ttu-id="1e3e3-110">Polecenie cmdlet **Get-AzRecoveryServicesBackupProtectionPolicy** pobiera zasady ochrony kopii zapasowych Azure dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="1e3e3-110">The **Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="1e3e3-111">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="1e3e3-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="1e3e3-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1e3e3-112">EXAMPLES</span></span>

### <span data-ttu-id="1e3e3-113">Przykład 1: pobieranie wszystkich zasad w magazynie</span><span class="sxs-lookup"><span data-stu-id="1e3e3-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="1e3e3-114">To polecenie pobiera wszystkie zasady ochrony utworzone w magazynie.</span><span class="sxs-lookup"><span data-stu-id="1e3e3-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="1e3e3-115">Przykład 2: uzyskiwanie określonych zasad</span><span class="sxs-lookup"><span data-stu-id="1e3e3-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="1e3e3-116">To polecenie uzyskuje zasady ochrony o nazwie DefaultPolicy, a następnie zapisuje je w zmiennej $Pol.</span><span class="sxs-lookup"><span data-stu-id="1e3e3-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="1e3e3-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1e3e3-117">PARAMETERS</span></span>

### <span data-ttu-id="1e3e3-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="1e3e3-118">-BackupManagementType</span></span>
<span data-ttu-id="1e3e3-119">Klasa zasobów chronionych.</span><span class="sxs-lookup"><span data-stu-id="1e3e3-119">The class of resources being protected.</span></span> <span data-ttu-id="1e3e3-120">Obecnie obsługiwane są wartości dla tego polecenia cmdlet to AzureVM, AzureStorage, AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="1e3e3-120">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureStorage, AzureWorkload, MAB

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3e3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e3e3-121">-DefaultProfile</span></span>
<span data-ttu-id="1e3e3-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1e3e3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e3e3-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1e3e3-123">-Name</span></span>
<span data-ttu-id="1e3e3-124">Określa nazwę zasady.</span><span class="sxs-lookup"><span data-stu-id="1e3e3-124">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="1e3e3-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="1e3e3-125">-VaultId</span></span>
<span data-ttu-id="1e3e3-126">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="1e3e3-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="1e3e3-127">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="1e3e3-127">-WorkloadType</span></span>
<span data-ttu-id="1e3e3-128">Typ obciążenia pracą zasobu.</span><span class="sxs-lookup"><span data-stu-id="1e3e3-128">Workload type of the resource.</span></span> <span data-ttu-id="1e3e3-129">Bieżące obsługiwane wartości to AzureVM, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="1e3e3-129">The current supported values are AzureVM, AzureFiles, MSSQL</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType]
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3e3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e3e3-130">CommonParameters</span></span>
<span data-ttu-id="1e3e3-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e3e3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e3e3-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e3e3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e3e3-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e3e3-133">INPUTS</span></span>

### <span data-ttu-id="1e3e3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1e3e3-134">System.String</span></span>

## <span data-ttu-id="1e3e3-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1e3e3-135">OUTPUTS</span></span>

### <span data-ttu-id="1e3e3-136">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="1e3e3-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="1e3e3-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1e3e3-137">NOTES</span></span>

## <span data-ttu-id="1e3e3-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e3e3-138">RELATED LINKS</span></span>

[<span data-ttu-id="1e3e3-139">Nowe — AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1e3e3-139">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="1e3e3-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1e3e3-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="1e3e3-141">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1e3e3-141">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)



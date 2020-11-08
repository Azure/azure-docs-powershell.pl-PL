---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 1b29bcc12c92b08e1c21dff4bb8b239fcc8f2bf6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053698"
---
# <span data-ttu-id="df678-101">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="df678-101">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="df678-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df678-102">SYNOPSIS</span></span>
<span data-ttu-id="df678-103">Pobiera zasady ochrony kopii zapasowej dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="df678-103">Gets Backup protection policies for a vault.</span></span>

## <span data-ttu-id="df678-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df678-104">SYNTAX</span></span>

### <span data-ttu-id="df678-105">NoParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="df678-105">NoParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df678-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="df678-106">PolicyNameParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df678-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="df678-107">WorkloadParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df678-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="df678-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df678-109">Opis</span><span class="sxs-lookup"><span data-stu-id="df678-109">DESCRIPTION</span></span>
<span data-ttu-id="df678-110">Polecenie cmdlet **Get-AzRecoveryServicesBackupProtectionPolicy** pobiera zasady ochrony kopii zapasowych Azure dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="df678-110">The **Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="df678-111">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="df678-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="df678-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df678-112">EXAMPLES</span></span>

### <span data-ttu-id="df678-113">Przykład 1: pobieranie wszystkich zasad w magazynie</span><span class="sxs-lookup"><span data-stu-id="df678-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="df678-114">To polecenie pobiera wszystkie zasady ochrony utworzone w magazynie.</span><span class="sxs-lookup"><span data-stu-id="df678-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="df678-115">Przykład 2: uzyskiwanie określonych zasad</span><span class="sxs-lookup"><span data-stu-id="df678-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="df678-116">To polecenie uzyskuje zasady ochrony o nazwie DefaultPolicy, a następnie zapisuje je w zmiennej $Pol.</span><span class="sxs-lookup"><span data-stu-id="df678-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="df678-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df678-117">PARAMETERS</span></span>

### <span data-ttu-id="df678-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="df678-118">-BackupManagementType</span></span>
<span data-ttu-id="df678-119">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="df678-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="df678-120">Obecnie obsługiwana jest tylko AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="df678-120">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df678-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df678-121">-DefaultProfile</span></span>
<span data-ttu-id="df678-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df678-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df678-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="df678-123">-Name</span></span>
<span data-ttu-id="df678-124">Określa nazwę zasady.</span><span class="sxs-lookup"><span data-stu-id="df678-124">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="df678-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="df678-125">-VaultId</span></span>
<span data-ttu-id="df678-126">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="df678-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="df678-127">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="df678-127">-WorkloadType</span></span>
<span data-ttu-id="df678-128">Określa typ obciążenia pracą.</span><span class="sxs-lookup"><span data-stu-id="df678-128">Specifies the workload type.</span></span>
<span data-ttu-id="df678-129">Obecnie obsługiwana jest tylko AzureVM, AzureFiles.</span><span class="sxs-lookup"><span data-stu-id="df678-129">Currently, only AzureVM, AzureFiles is supported.</span></span>

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

### <span data-ttu-id="df678-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df678-130">CommonParameters</span></span>
<span data-ttu-id="df678-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df678-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df678-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df678-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df678-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df678-133">INPUTS</span></span>

### <span data-ttu-id="df678-134">System. String</span><span class="sxs-lookup"><span data-stu-id="df678-134">System.String</span></span>

## <span data-ttu-id="df678-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df678-135">OUTPUTS</span></span>

### <span data-ttu-id="df678-136">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="df678-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="df678-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df678-137">NOTES</span></span>

## <span data-ttu-id="df678-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df678-138">RELATED LINKS</span></span>

[<span data-ttu-id="df678-139">Nowe — AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="df678-139">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="df678-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="df678-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="df678-141">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="df678-141">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)



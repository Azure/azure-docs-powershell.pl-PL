---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 8268c6037464c48d2492093c5b363acdc5f5ac5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719001"
---
# <span data-ttu-id="b7ab8-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b7ab8-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="b7ab8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7ab8-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ab8-103">Pobiera zasady ochrony kopii zapasowej dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="b7ab8-103">Gets Backup protection policies for a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7ab8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7ab8-104">SYNTAX</span></span>

### <span data-ttu-id="b7ab8-105">NoParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b7ab8-105">NoParamSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7ab8-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="b7ab8-106">PolicyNameParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7ab8-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="b7ab8-107">WorkloadParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7ab8-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="b7ab8-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7ab8-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b7ab8-109">DESCRIPTION</span></span>
<span data-ttu-id="b7ab8-110">Polecenie cmdlet **Get-AzureRmRecoveryServicesBackupProtectionPolicy** pobiera zasady ochrony kopii zapasowych Azure dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="b7ab8-110">The **Get-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>

<span data-ttu-id="b7ab8-111">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="b7ab8-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="b7ab8-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7ab8-112">EXAMPLES</span></span>

### <span data-ttu-id="b7ab8-113">Przykład 1: pobieranie wszystkich zasad w magazynie</span><span class="sxs-lookup"><span data-stu-id="b7ab8-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="b7ab8-114">To polecenie pobiera wszystkie zasady ochrony utworzone w magazynie.</span><span class="sxs-lookup"><span data-stu-id="b7ab8-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="b7ab8-115">Przykład 2: uzyskiwanie określonych zasad</span><span class="sxs-lookup"><span data-stu-id="b7ab8-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="b7ab8-116">To polecenie uzyskuje zasady ochrony o nazwie DefaultPolicy, a następnie zapisuje je w zmiennej $Pol.</span><span class="sxs-lookup"><span data-stu-id="b7ab8-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="b7ab8-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7ab8-117">PARAMETERS</span></span>

### <span data-ttu-id="b7ab8-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="b7ab8-118">-BackupManagementType</span></span>
<span data-ttu-id="b7ab8-119">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="b7ab8-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="b7ab8-120">Obecnie obsługiwana jest tylko AzureVM.</span><span class="sxs-lookup"><span data-stu-id="b7ab8-120">Currently, only AzureVM is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ab8-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b7ab8-121">-Name</span></span>
<span data-ttu-id="b7ab8-122">Określa nazwę zasady.</span><span class="sxs-lookup"><span data-stu-id="b7ab8-122">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="b7ab8-123">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="b7ab8-123">-WorkloadType</span></span>
<span data-ttu-id="b7ab8-124">Określa typ obciążenia pracą.</span><span class="sxs-lookup"><span data-stu-id="b7ab8-124">Specifies the workload type.</span></span>
<span data-ttu-id="b7ab8-125">Obecnie obsługiwana jest tylko AzureVM.</span><span class="sxs-lookup"><span data-stu-id="b7ab8-125">Currently, only AzureVM is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType]
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ab8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ab8-126">-DefaultProfile</span></span>
<span data-ttu-id="b7ab8-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7ab8-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7ab8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ab8-128">CommonParameters</span></span>
<span data-ttu-id="b7ab8-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7ab8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ab8-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7ab8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ab8-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7ab8-131">INPUTS</span></span>

## <span data-ttu-id="b7ab8-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7ab8-132">OUTPUTS</span></span>

### <span data-ttu-id="b7ab8-133">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="b7ab8-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="b7ab8-134">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. modele. PolicyBase]</span><span class="sxs-lookup"><span data-stu-id="b7ab8-134">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase]</span></span>

## <span data-ttu-id="b7ab8-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7ab8-135">NOTES</span></span>

## <span data-ttu-id="b7ab8-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7ab8-136">RELATED LINKS</span></span>

[<span data-ttu-id="b7ab8-137">Nowe — AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b7ab8-137">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="b7ab8-138">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b7ab8-138">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="b7ab8-139">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b7ab8-139">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)



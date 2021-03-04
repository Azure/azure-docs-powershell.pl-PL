---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 83a0e4edd82bd77358df1d95b53e388bb35a9e9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953297"
---
# <span data-ttu-id="62620-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="62620-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="62620-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62620-102">SYNOPSIS</span></span>
<span data-ttu-id="62620-103">Polecenie cmdlet **Register-AzRecoveryServicesBackupContainer** rejestruje maszynę wirtualną platformy Azure dla usługi AzureWorkloads z określonym typem obciążenia pracą.</span><span class="sxs-lookup"><span data-stu-id="62620-103">The **Register-AzRecoveryServicesBackupContainer** cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="62620-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="62620-104">SYNTAX</span></span>

### <span data-ttu-id="62620-105">Zarejestruj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="62620-105">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62620-106">ReRegister</span><span class="sxs-lookup"><span data-stu-id="62620-106">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62620-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="62620-107">DESCRIPTION</span></span>
<span data-ttu-id="62620-108">To polecenie umożliwia usłudze Azure Backup konwertowanie zasobu na kontener kopii zapasowej, który jest następnie rejestrowany w danym magazynie usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="62620-108">This command allows Azure Backup to convert the Resource to a Backup Container which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="62620-109">Usługa kopia zapasowa Azure może następnie wykrywać obciążenia danego typu obciążenia pracą w tym kontenerze, aby być później chronione.</span><span class="sxs-lookup"><span data-stu-id="62620-109">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="62620-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="62620-110">EXAMPLES</span></span>

### <span data-ttu-id="62620-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="62620-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="62620-112">Polecenie cmdlet rejestruje maszynę wirtualnej azure jako kontener dla msSQL obciążenia pracą.</span><span class="sxs-lookup"><span data-stu-id="62620-112">The cmdlet registers an azure VM as a container for the workload MSSQL.</span></span>

## <span data-ttu-id="62620-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62620-113">PARAMETERS</span></span>

### <span data-ttu-id="62620-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="62620-114">-BackupManagementType</span></span>
<span data-ttu-id="62620-115">Klasa zasobów, które są chronione.</span><span class="sxs-lookup"><span data-stu-id="62620-115">The class of resources being protected.</span></span> <span data-ttu-id="62620-116">Obecnie wartość obsługiwana dla tego polecenia cmdlet to AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="62620-116">Currently the value supported for this cmdlet is AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62620-117">— Kontener</span><span class="sxs-lookup"><span data-stu-id="62620-117">-Container</span></span>
<span data-ttu-id="62620-118">Kontener, w którym znajduje się element</span><span class="sxs-lookup"><span data-stu-id="62620-118">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: ReRegister
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62620-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62620-119">-DefaultProfile</span></span>
<span data-ttu-id="62620-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="62620-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62620-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="62620-121">-Force</span></span>
<span data-ttu-id="62620-122">Wymuszanie rejestrowania kontenera (uniemożliwia okno dialogowe potwierdzenia).</span><span class="sxs-lookup"><span data-stu-id="62620-122">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="62620-123">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="62620-123">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62620-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62620-124">-ResourceId</span></span>
<span data-ttu-id="62620-125">Identyfikator zasobu Azure, którego element reprezentatywny musi zostać sprawdzony, jeśli jest już chroniony przez niektóre magazyny usługi odzyskiwania w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="62620-125">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Register
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62620-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="62620-126">-VaultId</span></span>
<span data-ttu-id="62620-127">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="62620-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="62620-128">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="62620-128">-WorkloadType</span></span>
<span data-ttu-id="62620-129">Typ obciążenia zasobu.</span><span class="sxs-lookup"><span data-stu-id="62620-129">Workload type of the resource.</span></span> <span data-ttu-id="62620-130">Bieżąca obsługiwana wartość to AzureVM, WindowsServer, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="62620-130">The current supported value is AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62620-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="62620-131">-Confirm</span></span>
<span data-ttu-id="62620-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="62620-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62620-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62620-133">-WhatIf</span></span>
<span data-ttu-id="62620-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62620-134">Shows what would happen if the cmdlet runs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62620-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62620-135">CommonParameters</span></span>
<span data-ttu-id="62620-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62620-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62620-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62620-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62620-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62620-138">INPUTS</span></span>

### <span data-ttu-id="62620-139">System.String</span><span class="sxs-lookup"><span data-stu-id="62620-139">System.String</span></span>

## <span data-ttu-id="62620-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62620-140">OUTPUTS</span></span>

### <span data-ttu-id="62620-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="62620-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="62620-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="62620-142">NOTES</span></span>

## <span data-ttu-id="62620-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62620-143">RELATED LINKS</span></span>

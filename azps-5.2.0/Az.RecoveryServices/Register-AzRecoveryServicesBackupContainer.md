---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: cfa8abf93fcb7eb4cd3848b1a5f69cf28a5fe6ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355705"
---
# <span data-ttu-id="2fa2b-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="2fa2b-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="2fa2b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2fa2b-102">SYNOPSIS</span></span>
<span data-ttu-id="2fa2b-103">Polecenie cmdlet **register-AzRecoveryServicesBackupContainer** rejestruje maszynę wirtualną platformy Azure dla AzureWorkloads przy użyciu określonego elementu obciążeniatype.</span><span class="sxs-lookup"><span data-stu-id="2fa2b-103">The **Register-AzRecoveryServicesBackupContainer** cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="2fa2b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2fa2b-104">SYNTAX</span></span>

### <span data-ttu-id="2fa2b-105">Zarejestruj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="2fa2b-105">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fa2b-106">Ponowne rejestrowanie</span><span class="sxs-lookup"><span data-stu-id="2fa2b-106">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fa2b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2fa2b-107">DESCRIPTION</span></span>
<span data-ttu-id="2fa2b-108">To polecenie umożliwia usłudze Kopia zapasowa Azure przekonwertowanie zasobu na kontener kopii zapasowej, który jest następnie rejestrowany w danym magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="2fa2b-108">This command allows Azure Backup to convert the Resource to a Backup Container which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="2fa2b-109">Usługa Kopia zapasowa Azure może następnie wykryć obciążenia pracą danego typu obciążenia w tym kontenerze, aby móc je później chronić.</span><span class="sxs-lookup"><span data-stu-id="2fa2b-109">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="2fa2b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2fa2b-110">EXAMPLES</span></span>

### <span data-ttu-id="2fa2b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2fa2b-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="2fa2b-112">Polecenie cmdlet rejestruje maszynę wirtualną platformy Azure jako kontener dla usługi MSSQL do obsługi obciążeń.</span><span class="sxs-lookup"><span data-stu-id="2fa2b-112">The cmdlet registers an azure VM as a container for the workload MSSQL.</span></span>

## <span data-ttu-id="2fa2b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2fa2b-113">PARAMETERS</span></span>

### <span data-ttu-id="2fa2b-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="2fa2b-114">-BackupManagementType</span></span>
<span data-ttu-id="2fa2b-115">Klasa zasobów chronionych.</span><span class="sxs-lookup"><span data-stu-id="2fa2b-115">The class of resources being protected.</span></span> <span data-ttu-id="2fa2b-116">Obecnie dla tego polecenia cmdlet jest obsługiwana wartość AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="2fa2b-116">Currently the value supported for this cmdlet is AzureWorkload</span></span>

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

### <span data-ttu-id="2fa2b-117">-Kontener</span><span class="sxs-lookup"><span data-stu-id="2fa2b-117">-Container</span></span>
<span data-ttu-id="2fa2b-118">Kontener, w którym znajduje się element</span><span class="sxs-lookup"><span data-stu-id="2fa2b-118">Container where the item resides</span></span>

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

### <span data-ttu-id="2fa2b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fa2b-119">-DefaultProfile</span></span>
<span data-ttu-id="2fa2b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2fa2b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fa2b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2fa2b-121">-Force</span></span>
<span data-ttu-id="2fa2b-122">Kontener rejestrów wymuszonych (zapobiega wyświetlaniu okna dialogowego potwierdzenia).</span><span class="sxs-lookup"><span data-stu-id="2fa2b-122">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="2fa2b-123">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2fa2b-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="2fa2b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fa2b-124">-ResourceId</span></span>
<span data-ttu-id="2fa2b-125">Identyfikator zasobu platformy Azure, którego element reprezentatywny musi zostać sprawdzony, jeśli jest już chroniony przez jakiś magazyn RecoveryServices w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2fa2b-125">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="2fa2b-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2fa2b-126">-VaultId</span></span>
<span data-ttu-id="2fa2b-127">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="2fa2b-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2fa2b-128">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="2fa2b-128">-WorkloadType</span></span>
<span data-ttu-id="2fa2b-129">Typ obciążenia pracą zasobu.</span><span class="sxs-lookup"><span data-stu-id="2fa2b-129">Workload type of the resource.</span></span> <span data-ttu-id="2fa2b-130">Bieżąca obsługiwana wartość to AzureVM, WindowsServer, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="2fa2b-130">The current supported value is AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="2fa2b-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2fa2b-131">-Confirm</span></span>
<span data-ttu-id="2fa2b-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fa2b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fa2b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fa2b-133">-WhatIf</span></span>
<span data-ttu-id="2fa2b-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fa2b-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="2fa2b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fa2b-135">CommonParameters</span></span>
<span data-ttu-id="2fa2b-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fa2b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fa2b-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fa2b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fa2b-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2fa2b-138">INPUTS</span></span>

### <span data-ttu-id="2fa2b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2fa2b-139">System.String</span></span>

## <span data-ttu-id="2fa2b-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2fa2b-140">OUTPUTS</span></span>

### <span data-ttu-id="2fa2b-141">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="2fa2b-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="2fa2b-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2fa2b-142">NOTES</span></span>

## <span data-ttu-id="2fa2b-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2fa2b-143">RELATED LINKS</span></span>

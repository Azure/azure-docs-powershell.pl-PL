---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: eeffbbd62a4c161b95004c6f4bd40d31fbd02517
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886665"
---
# <span data-ttu-id="7f6b4-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="7f6b4-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="7f6b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f6b4-102">SYNOPSIS</span></span>
<span data-ttu-id="7f6b4-103">To polecenie umożliwia usłudze Kopia zapasowa Azure przekonwertowanie zasobu na kontener kopii zapasowej, który jest następnie rejestrowany w danym magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-103">This command allows Azure Backup to convert the �Resource� to a �Backup Container� which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="7f6b4-104">Usługa Kopia zapasowa Azure może następnie wykryć obciążenia pracą danego typu obciążenia w tym kontenerze, aby móc je później chronić.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-104">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="7f6b4-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f6b4-105">SYNTAX</span></span>

### <span data-ttu-id="7f6b4-106">Zarejestruj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7f6b4-106">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f6b4-107">Ponowne rejestrowanie</span><span class="sxs-lookup"><span data-stu-id="7f6b4-107">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f6b4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7f6b4-108">DESCRIPTION</span></span>
<span data-ttu-id="7f6b4-109">Polecenie cmdlet rejestruje maszynę wirtualną platformy Azure dla AzureWorkloads przy użyciu określonego elementu obciążeniatype.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-109">The cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="7f6b4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f6b4-110">EXAMPLES</span></span>

### <span data-ttu-id="7f6b4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7f6b4-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="7f6b4-112">Polecenie cmdlet rejestruje maszynę wirtualną platformy Azure w celu obsługi obciążeń.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-112">The cmdlet registers an azure VM for the workload MSSQL.</span></span>

## <span data-ttu-id="7f6b4-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f6b4-113">PARAMETERS</span></span>

### <span data-ttu-id="7f6b4-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="7f6b4-114">-BackupManagementType</span></span>
<span data-ttu-id="7f6b4-115">Typ zarządzania kopią zapasową kontenera kopii zapasowych Azure</span><span class="sxs-lookup"><span data-stu-id="7f6b4-115">The backup management type of the Azure Backup container</span></span>

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

### <span data-ttu-id="7f6b4-116">-Kontener</span><span class="sxs-lookup"><span data-stu-id="7f6b4-116">-Container</span></span>
<span data-ttu-id="7f6b4-117">Kontener, w którym znajduje się element</span><span class="sxs-lookup"><span data-stu-id="7f6b4-117">Container where the item resides</span></span>

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

### <span data-ttu-id="7f6b4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f6b4-118">-DefaultProfile</span></span>
<span data-ttu-id="7f6b4-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f6b4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7f6b4-120">-Force</span></span>
<span data-ttu-id="7f6b4-121">Kontener rejestrów wymuszonych (zapobiega wyświetlaniu okna dialogowego potwierdzenia).</span><span class="sxs-lookup"><span data-stu-id="7f6b4-121">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="7f6b4-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="7f6b4-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f6b4-123">-ResourceId</span></span>
<span data-ttu-id="7f6b4-124">Identyfikator zasobu platformy Azure, którego element reprezentatywny musi zostać sprawdzony, jeśli jest już chroniony przez jakiś magazyn RecoveryServices w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-124">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="7f6b4-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7f6b4-125">-VaultId</span></span>
<span data-ttu-id="7f6b4-126">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7f6b4-127">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="7f6b4-127">-WorkloadType</span></span>
<span data-ttu-id="7f6b4-128">Typ obciążenia pracą zasobu (na przykład: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="7f6b4-128">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

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

### <span data-ttu-id="7f6b4-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f6b4-129">-Confirm</span></span>
<span data-ttu-id="7f6b4-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f6b4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f6b4-131">-WhatIf</span></span>
<span data-ttu-id="7f6b4-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f6b4-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f6b4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f6b4-134">CommonParameters</span></span>
<span data-ttu-id="7f6b4-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f6b4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f6b4-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f6b4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f6b4-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f6b4-137">INPUTS</span></span>

### <span data-ttu-id="7f6b4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7f6b4-138">System.String</span></span>

## <span data-ttu-id="7f6b4-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f6b4-139">OUTPUTS</span></span>

### <span data-ttu-id="7f6b4-140">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="7f6b4-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="7f6b4-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f6b4-141">NOTES</span></span>

## <span data-ttu-id="7f6b4-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f6b4-142">RELATED LINKS</span></span>
---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: b92d483689c94e6dd9f9af69e47f5b17ea1ab795
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233105"
---
# <span data-ttu-id="69143-101">New-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="69143-101">New-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="69143-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69143-102">SYNOPSIS</span></span>
<span data-ttu-id="69143-103">Operacja tworzenia mapowania kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="69143-103">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="69143-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69143-104">SYNTAX</span></span>

```
New-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-PolicyId <String>]
 [-ProviderSpecificInput <IReplicationProviderSpecificContainerMappingInput>]
 [-TargetProtectionContainerId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="69143-105">Opis</span><span class="sxs-lookup"><span data-stu-id="69143-105">DESCRIPTION</span></span>
<span data-ttu-id="69143-106">Operacja tworzenia mapowania kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="69143-106">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="69143-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69143-107">EXAMPLES</span></span>

### <span data-ttu-id="69143-108">Przykład 1. Tworzenie mapowania</span><span class="sxs-lookup"><span data-stu-id="69143-108">Example 1: Create a mapping</span></span>
```powershell
PS C:\> $providerSpecificInput = [Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtContainerMappingInput]::new()
PS C:\> $providerSpecificInput.InstanceType = "VMwareCbt"
PS C:\> $providerSpecificInput.KeyVaultId = "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.KeyVault/vaults/migratekv846827101"
PS C:\> $providerSpecificInput.KeyVaultUri = "https://migratekv846827101.vault.azure.net"
PS C:\> $providerSpecificInput.ServiceBusConnectionStringSecretName = "ServiceBusConnectionString"
PS C:\> $providerSpecificInput.StorageAccountId = "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Storage/storageAccounts/migrategwsa846827101"
PS C:\> $providerSpecificInput.StorageAccountSasSecretName = "migrategwsa846827101-gwySas"
PS C:\> $providerSpecificInput.TargetLocation = "centraluseuap"

PS C:\> New-AzMigrateReplicationProtectionContainerMapping -FabricName "AzMigratePWSHTc8d1replicationfabric" -MappingName "containermapping" -ProtectionContainerName "AzMigratePWSHTc8d1replicationcontainer" -ResourceGroupName "azmigratepwshtestasr13072020" -ResourceName "AzMigrateTestProjectPWSH02aarsvault"  -PolicyId "/subscriptionsxxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy"  -ProviderSpecificInput $providerSpecificInput -TargetProtectionContainerId  "Microsoft Azure"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="69143-109">Tworzenie mapowania</span><span class="sxs-lookup"><span data-stu-id="69143-109">Create a mapping</span></span>

## <span data-ttu-id="69143-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69143-110">PARAMETERS</span></span>

### <span data-ttu-id="69143-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69143-111">-AsJob</span></span>
<span data-ttu-id="69143-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="69143-112">Run the command as a job</span></span>

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

### <span data-ttu-id="69143-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69143-113">-DefaultProfile</span></span>
<span data-ttu-id="69143-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="69143-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69143-115">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="69143-115">-FabricName</span></span>
<span data-ttu-id="69143-116">Nazwa sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="69143-116">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69143-117">-MappingName</span><span class="sxs-lookup"><span data-stu-id="69143-117">-MappingName</span></span>
<span data-ttu-id="69143-118">Nazwa mapowania kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="69143-118">Protection container mapping name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69143-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="69143-119">-NoWait</span></span>
<span data-ttu-id="69143-120">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="69143-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="69143-121">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="69143-121">-PolicyId</span></span>
<span data-ttu-id="69143-122">Stosowane zasady.</span><span class="sxs-lookup"><span data-stu-id="69143-122">Applicable policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69143-123">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="69143-123">-ProtectionContainerName</span></span>
<span data-ttu-id="69143-124">Nazwa kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="69143-124">Protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69143-125">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="69143-125">-ProviderSpecificInput</span></span>
<span data-ttu-id="69143-126">Specyficzne dla dostawcy dane wejściowe parowania.</span><span class="sxs-lookup"><span data-stu-id="69143-126">Provider specific input for pairing.</span></span>
<span data-ttu-id="69143-127">Aby skonstruować, zobacz sekcję notatki dla właściwości PROVIDERSPECIFICINPUT i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="69143-127">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IReplicationProviderSpecificContainerMappingInput
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69143-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69143-128">-ResourceGroupName</span></span>
<span data-ttu-id="69143-129">Nazwa grupy zasobów, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="69143-129">The name of the resource group where the recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69143-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="69143-130">-ResourceName</span></span>
<span data-ttu-id="69143-131">Nazwa magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="69143-131">The name of the recovery services vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69143-132">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="69143-132">-SubscriptionId</span></span>
<span data-ttu-id="69143-133">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="69143-133">The subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69143-134">-TargetProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="69143-134">-TargetProtectionContainerId</span></span>
<span data-ttu-id="69143-135">Nazwa docelowej unikatowego kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="69143-135">The target unique protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69143-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69143-136">-Confirm</span></span>
<span data-ttu-id="69143-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69143-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69143-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69143-138">-WhatIf</span></span>
<span data-ttu-id="69143-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69143-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69143-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="69143-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69143-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69143-141">CommonParameters</span></span>
<span data-ttu-id="69143-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69143-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69143-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69143-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69143-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69143-144">INPUTS</span></span>

## <span data-ttu-id="69143-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69143-145">OUTPUTS</span></span>

### <span data-ttu-id="69143-146">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180110. IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="69143-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="69143-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69143-147">NOTES</span></span>

<span data-ttu-id="69143-148">PISUJE</span><span class="sxs-lookup"><span data-stu-id="69143-148">ALIASES</span></span>

<span data-ttu-id="69143-149">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69143-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="69143-150">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="69143-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="69143-151">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="69143-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="69143-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput> : dane wejściowe konkretnego dostawcy w celu parowania.</span><span class="sxs-lookup"><span data-stu-id="69143-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput>: Provider specific input for pairing.</span></span>
  - <span data-ttu-id="69143-153">`[InstanceType <String>]`: Typ zajęć.</span><span class="sxs-lookup"><span data-stu-id="69143-153">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="69143-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69143-154">RELATED LINKS</span></span>


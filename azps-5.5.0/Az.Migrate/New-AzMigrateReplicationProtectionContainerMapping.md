---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: 996f33a967aaedc66bc0ed9b41cba09401f1dde4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194107"
---
# <span data-ttu-id="93302-101">New-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="93302-101">New-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="93302-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93302-102">SYNOPSIS</span></span>
<span data-ttu-id="93302-103">Operacja tworzenia mapowania kontenerów ochrony.</span><span class="sxs-lookup"><span data-stu-id="93302-103">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="93302-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="93302-104">SYNTAX</span></span>

```
New-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-PolicyId <String>]
 [-ProviderSpecificInput <IReplicationProviderSpecificContainerMappingInput>]
 [-TargetProtectionContainerId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="93302-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="93302-105">DESCRIPTION</span></span>
<span data-ttu-id="93302-106">Operacja tworzenia mapowania kontenerów ochrony.</span><span class="sxs-lookup"><span data-stu-id="93302-106">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="93302-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="93302-107">EXAMPLES</span></span>

### <span data-ttu-id="93302-108">Przykład 1. Tworzenie mapowania</span><span class="sxs-lookup"><span data-stu-id="93302-108">Example 1: Create a mapping</span></span>
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

<span data-ttu-id="93302-109">Tworzenie mapowania</span><span class="sxs-lookup"><span data-stu-id="93302-109">Create a mapping</span></span>

## <span data-ttu-id="93302-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93302-110">PARAMETERS</span></span>

### <span data-ttu-id="93302-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="93302-111">-AsJob</span></span>
<span data-ttu-id="93302-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="93302-112">Run the command as a job</span></span>

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

### <span data-ttu-id="93302-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93302-113">-DefaultProfile</span></span>
<span data-ttu-id="93302-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="93302-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93302-115">- FabricName</span><span class="sxs-lookup"><span data-stu-id="93302-115">-FabricName</span></span>
<span data-ttu-id="93302-116">Nazwa materiału.</span><span class="sxs-lookup"><span data-stu-id="93302-116">Fabric name.</span></span>

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

### <span data-ttu-id="93302-117">-MappingName</span><span class="sxs-lookup"><span data-stu-id="93302-117">-MappingName</span></span>
<span data-ttu-id="93302-118">Nazwa mapowania kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="93302-118">Protection container mapping name.</span></span>

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

### <span data-ttu-id="93302-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="93302-119">-NoWait</span></span>
<span data-ttu-id="93302-120">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="93302-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="93302-121">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="93302-121">-PolicyId</span></span>
<span data-ttu-id="93302-122">Zasady obowiązujące.</span><span class="sxs-lookup"><span data-stu-id="93302-122">Applicable policy.</span></span>

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

### <span data-ttu-id="93302-123">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="93302-123">-ProtectionContainerName</span></span>
<span data-ttu-id="93302-124">Nazwa kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="93302-124">Protection container name.</span></span>

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

### <span data-ttu-id="93302-125">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="93302-125">-ProviderSpecificInput</span></span>
<span data-ttu-id="93302-126">Dane wejściowe dostawcy dotyczące parowania.</span><span class="sxs-lookup"><span data-stu-id="93302-126">Provider specific input for pairing.</span></span>
<span data-ttu-id="93302-127">Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach PROVIDERSPECIFICINPUT i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="93302-127">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

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

### <span data-ttu-id="93302-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93302-128">-ResourceGroupName</span></span>
<span data-ttu-id="93302-129">Nazwa grupy zasobów, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="93302-129">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="93302-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="93302-130">-ResourceName</span></span>
<span data-ttu-id="93302-131">Nazwa magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="93302-131">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="93302-132">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93302-132">-SubscriptionId</span></span>
<span data-ttu-id="93302-133">Identyfikator subskrypcji platformy Azure, w którym utworzono projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="93302-133">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="93302-134">-TargetProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="93302-134">-TargetProtectionContainerId</span></span>
<span data-ttu-id="93302-135">Nazwa docelowego unikatowego kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="93302-135">The target unique protection container name.</span></span>

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

### <span data-ttu-id="93302-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="93302-136">-Confirm</span></span>
<span data-ttu-id="93302-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="93302-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93302-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93302-138">-WhatIf</span></span>
<span data-ttu-id="93302-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93302-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93302-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="93302-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93302-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93302-141">CommonParameters</span></span>
<span data-ttu-id="93302-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93302-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93302-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93302-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93302-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93302-144">INPUTS</span></span>

## <span data-ttu-id="93302-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93302-145">OUTPUTS</span></span>

### <span data-ttu-id="93302-146">Microsoft.Azure.PowerShell.cmdlet.migrate.models.api20180110.IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="93302-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="93302-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="93302-147">NOTES</span></span>

<span data-ttu-id="93302-148">ALIASY</span><span class="sxs-lookup"><span data-stu-id="93302-148">ALIASES</span></span>

<span data-ttu-id="93302-149">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="93302-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="93302-150">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="93302-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="93302-151">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="93302-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="93302-152">PROVIDERSPECIFICINPUT: <IReplicationProviderSpecificContainerMappingInput> Dane wejściowe dostawcy dotyczące parowania.</span><span class="sxs-lookup"><span data-stu-id="93302-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput>: Provider specific input for pairing.</span></span>
  - <span data-ttu-id="93302-153">`[InstanceType <String>]`: Typ zajęć.</span><span class="sxs-lookup"><span data-stu-id="93302-153">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="93302-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93302-154">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 7f9b78a6c287f7135f2463a6cfe63b2963ffe362
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982673"
---
# <span data-ttu-id="8053a-101">New-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="8053a-101">New-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="8053a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8053a-102">SYNOPSIS</span></span>
<span data-ttu-id="8053a-103">Operacja tworzenia zasad replikacji</span><span class="sxs-lookup"><span data-stu-id="8053a-103">The operation to create a replication policy</span></span>

## <span data-ttu-id="8053a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8053a-104">SYNTAX</span></span>

```
New-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-ProviderSpecificInput <IPolicyProviderSpecificInput>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8053a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8053a-105">DESCRIPTION</span></span>
<span data-ttu-id="8053a-106">Operacja tworzenia zasad replikacji</span><span class="sxs-lookup"><span data-stu-id="8053a-106">The operation to create a replication policy</span></span>

## <span data-ttu-id="8053a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8053a-107">EXAMPLES</span></span>

### <span data-ttu-id="8053a-108">Przykład 1. Tworzenie zasad replikacji</span><span class="sxs-lookup"><span data-stu-id="8053a-108">Example 1: Create a replication policy</span></span>
```powershell
PS C:\> $providerSpecificPolicy = [Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtPolicyCreationInput]::new()
PS C:\> $providerSpecificPolicy.AppConsistentFrequencyInMinute = 240
PS C:\> $providerSpecificPolicy.InstanceType = "VMwareCbt"
PS C:\> $providerSpecificPolicy.RecoveryPointHistoryInMinute = 4320
PS C:\> $providerSpecificPolicy.CrashConsistentFrequencyInMinute = 60
PS C:\> New-AzMigrateReplicationPolicy -PolicyName TestPolicy -ResourceGroupName ResourceGroup -ResourceName VaultName -SubscriptionId SubscriptionId -ProviderSpecificInput $providerSpecificPolicy

Location Name       Type
-------- ----       ----
         TestPolicy Microsoft.RecoveryServices/vaults/replicationPolicies
         
```

<span data-ttu-id="8053a-109">Tworzy zasady dla usługi VmWare Cbt</span><span class="sxs-lookup"><span data-stu-id="8053a-109">Creates a policy for VmWare Cbt</span></span>

## <span data-ttu-id="8053a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8053a-110">PARAMETERS</span></span>

### <span data-ttu-id="8053a-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8053a-111">-AsJob</span></span>
<span data-ttu-id="8053a-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="8053a-112">Run the command as a job</span></span>

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

### <span data-ttu-id="8053a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8053a-113">-DefaultProfile</span></span>
<span data-ttu-id="8053a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8053a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8053a-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8053a-115">-NoWait</span></span>
<span data-ttu-id="8053a-116">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="8053a-116">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8053a-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="8053a-117">-PolicyName</span></span>
<span data-ttu-id="8053a-118">Nazwa zasad replikacji</span><span class="sxs-lookup"><span data-stu-id="8053a-118">Replication policy name</span></span>

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

### <span data-ttu-id="8053a-119">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="8053a-119">-ProviderSpecificInput</span></span>
<span data-ttu-id="8053a-120">Zestawy replikacji (ReplicationProviderSettings).</span><span class="sxs-lookup"><span data-stu-id="8053a-120">The ReplicationProviderSettings.</span></span>
<span data-ttu-id="8053a-121">Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach PROVIDERSPECIFICINPUT i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="8053a-121">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicyProviderSpecificInput
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8053a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8053a-122">-ResourceGroupName</span></span>
<span data-ttu-id="8053a-123">Nazwa grupy zasobów, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="8053a-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="8053a-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8053a-124">-ResourceName</span></span>
<span data-ttu-id="8053a-125">Nazwa magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="8053a-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="8053a-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8053a-126">-SubscriptionId</span></span>
<span data-ttu-id="8053a-127">Identyfikator subskrypcji platformy Azure, w którym utworzono projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="8053a-127">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="8053a-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8053a-128">-Confirm</span></span>
<span data-ttu-id="8053a-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8053a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8053a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8053a-130">-WhatIf</span></span>
<span data-ttu-id="8053a-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8053a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8053a-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8053a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8053a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8053a-133">CommonParameters</span></span>
<span data-ttu-id="8053a-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8053a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8053a-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8053a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8053a-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8053a-136">INPUTS</span></span>

## <span data-ttu-id="8053a-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8053a-137">OUTPUTS</span></span>

### <span data-ttu-id="8053a-138">Microsoft.Azure.PowerShell.cmdlet.migrate.models.api20180110.iPolicy</span><span class="sxs-lookup"><span data-stu-id="8053a-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="8053a-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8053a-139">NOTES</span></span>

<span data-ttu-id="8053a-140">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8053a-140">ALIASES</span></span>

<span data-ttu-id="8053a-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8053a-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8053a-142">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8053a-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8053a-143">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8053a-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8053a-144">PROVIDERSPECIFICINPUT: <IPolicyProviderSpecificInput> The ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="8053a-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput>: The ReplicationProviderSettings.</span></span>
  - <span data-ttu-id="8053a-145">`[InstanceType <String>]`: Typ zajęć.</span><span class="sxs-lookup"><span data-stu-id="8053a-145">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="8053a-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8053a-146">RELATED LINKS</span></span>


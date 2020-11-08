---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 5978c247f14507934662f5a5d1846a02180cd812
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231785"
---
# <span data-ttu-id="4a033-101">New-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="4a033-101">New-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="4a033-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a033-102">SYNOPSIS</span></span>
<span data-ttu-id="4a033-103">Operacja tworzenia zasad replikacji</span><span class="sxs-lookup"><span data-stu-id="4a033-103">The operation to create a replication policy</span></span>

## <span data-ttu-id="4a033-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a033-104">SYNTAX</span></span>

```
New-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-ProviderSpecificInput <IPolicyProviderSpecificInput>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4a033-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4a033-105">DESCRIPTION</span></span>
<span data-ttu-id="4a033-106">Operacja tworzenia zasad replikacji</span><span class="sxs-lookup"><span data-stu-id="4a033-106">The operation to create a replication policy</span></span>

## <span data-ttu-id="4a033-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a033-107">EXAMPLES</span></span>

### <span data-ttu-id="4a033-108">Przykład 1. Tworzenie zasad replikacji</span><span class="sxs-lookup"><span data-stu-id="4a033-108">Example 1: Create a replication policy</span></span>
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

<span data-ttu-id="4a033-109">Tworzy zasady dla usługi VmWare CBT</span><span class="sxs-lookup"><span data-stu-id="4a033-109">Creates a policy for VmWare Cbt</span></span>

## <span data-ttu-id="4a033-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a033-110">PARAMETERS</span></span>

### <span data-ttu-id="4a033-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a033-111">-AsJob</span></span>
<span data-ttu-id="4a033-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="4a033-112">Run the command as a job</span></span>

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

### <span data-ttu-id="4a033-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a033-113">-DefaultProfile</span></span>
<span data-ttu-id="4a033-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a033-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a033-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="4a033-115">-NoWait</span></span>
<span data-ttu-id="4a033-116">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="4a033-116">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4a033-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="4a033-117">-PolicyName</span></span>
<span data-ttu-id="4a033-118">Nazwa zasad replikacji</span><span class="sxs-lookup"><span data-stu-id="4a033-118">Replication policy name</span></span>

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

### <span data-ttu-id="4a033-119">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="4a033-119">-ProviderSpecificInput</span></span>
<span data-ttu-id="4a033-120">ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="4a033-120">The ReplicationProviderSettings.</span></span>
<span data-ttu-id="4a033-121">Aby skonstruować, zobacz sekcję notatki dla właściwości PROVIDERSPECIFICINPUT i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="4a033-121">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4a033-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a033-122">-ResourceGroupName</span></span>
<span data-ttu-id="4a033-123">Nazwa grupy zasobów, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="4a033-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="4a033-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4a033-124">-ResourceName</span></span>
<span data-ttu-id="4a033-125">Nazwa magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="4a033-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="4a033-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4a033-126">-SubscriptionId</span></span>
<span data-ttu-id="4a033-127">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="4a033-127">The subscription Id.</span></span>

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

### <span data-ttu-id="4a033-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4a033-128">-Confirm</span></span>
<span data-ttu-id="4a033-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a033-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a033-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a033-130">-WhatIf</span></span>
<span data-ttu-id="4a033-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a033-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a033-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4a033-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a033-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a033-133">CommonParameters</span></span>
<span data-ttu-id="4a033-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a033-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a033-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a033-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a033-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a033-136">INPUTS</span></span>

## <span data-ttu-id="4a033-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a033-137">OUTPUTS</span></span>

### <span data-ttu-id="4a033-138">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180110. IPolicy</span><span class="sxs-lookup"><span data-stu-id="4a033-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="4a033-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a033-139">NOTES</span></span>

<span data-ttu-id="4a033-140">PISUJE</span><span class="sxs-lookup"><span data-stu-id="4a033-140">ALIASES</span></span>

<span data-ttu-id="4a033-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a033-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4a033-142">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4a033-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4a033-143">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4a033-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4a033-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput> : ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="4a033-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput>: The ReplicationProviderSettings.</span></span>
  - <span data-ttu-id="4a033-145">`[InstanceType <String>]`: Typ zajęć.</span><span class="sxs-lookup"><span data-stu-id="4a033-145">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="4a033-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a033-146">RELATED LINKS</span></span>


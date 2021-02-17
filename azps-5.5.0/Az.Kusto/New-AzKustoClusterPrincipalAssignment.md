---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: fafc31700477de968c453002e903b52aa73967d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243299"
---
# <span data-ttu-id="aec45-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="aec45-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="aec45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aec45-102">SYNOPSIS</span></span>
<span data-ttu-id="aec45-103">Tworzenie przypisania głównego klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="aec45-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="aec45-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="aec45-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aec45-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="aec45-105">DESCRIPTION</span></span>
<span data-ttu-id="aec45-106">Tworzenie przypisania głównego klastra Kusto.</span><span class="sxs-lookup"><span data-stu-id="aec45-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="aec45-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="aec45-107">EXAMPLES</span></span>

### <span data-ttu-id="aec45-108">Przykład 1. Tworzenie przypisania głównego klastra Kusto</span><span class="sxs-lookup"><span data-stu-id="aec45-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="aec45-109">Powyższe polecenie tworzy przypisanie główne grupowania Kusto</span><span class="sxs-lookup"><span data-stu-id="aec45-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="aec45-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aec45-110">PARAMETERS</span></span>

### <span data-ttu-id="aec45-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="aec45-111">-AsJob</span></span>
<span data-ttu-id="aec45-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="aec45-112">Run the command as a job</span></span>

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

### <span data-ttu-id="aec45-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="aec45-113">-ClusterName</span></span>
<span data-ttu-id="aec45-114">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="aec45-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="aec45-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aec45-115">-DefaultProfile</span></span>
<span data-ttu-id="aec45-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="aec45-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aec45-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="aec45-117">-NoWait</span></span>
<span data-ttu-id="aec45-118">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="aec45-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="aec45-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="aec45-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="aec45-120">Nazwa dopisu głównego( Kusto principalAssignment).</span><span class="sxs-lookup"><span data-stu-id="aec45-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="aec45-121">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="aec45-121">-PrincipalId</span></span>
<span data-ttu-id="aec45-122">Identyfikator dyrektora przypisany do podmiotu zabezpieczeń klastrów.</span><span class="sxs-lookup"><span data-stu-id="aec45-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="aec45-123">Może to być adres e-mail użytkownika, identyfikator aplikacji lub nazwa grupy zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="aec45-123">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="aec45-124">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="aec45-124">-PrincipalType</span></span>
<span data-ttu-id="aec45-125">Typ dyrektora.</span><span class="sxs-lookup"><span data-stu-id="aec45-125">Principal type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.PrincipalType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aec45-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aec45-126">-ResourceGroupName</span></span>
<span data-ttu-id="aec45-127">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="aec45-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="aec45-128">— Rola</span><span class="sxs-lookup"><span data-stu-id="aec45-128">-Role</span></span>
<span data-ttu-id="aec45-129">Rola główna klastrów.</span><span class="sxs-lookup"><span data-stu-id="aec45-129">Cluster principal role.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.ClusterPrincipalRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aec45-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aec45-130">-SubscriptionId</span></span>
<span data-ttu-id="aec45-131">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aec45-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="aec45-132">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="aec45-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="aec45-133">- TenantId</span><span class="sxs-lookup"><span data-stu-id="aec45-133">-TenantId</span></span>
<span data-ttu-id="aec45-134">Identyfikator dzierżawy dyrektora</span><span class="sxs-lookup"><span data-stu-id="aec45-134">The tenant id of the principal</span></span>

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

### <span data-ttu-id="aec45-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aec45-135">-Confirm</span></span>
<span data-ttu-id="aec45-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="aec45-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aec45-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aec45-137">-WhatIf</span></span>
<span data-ttu-id="aec45-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aec45-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aec45-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="aec45-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aec45-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec45-140">CommonParameters</span></span>
<span data-ttu-id="aec45-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aec45-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec45-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aec45-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec45-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aec45-143">INPUTS</span></span>

## <span data-ttu-id="aec45-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aec45-144">OUTPUTS</span></span>

### <span data-ttu-id="aec45-145">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="aec45-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="aec45-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="aec45-146">NOTES</span></span>

<span data-ttu-id="aec45-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="aec45-147">ALIASES</span></span>

## <span data-ttu-id="aec45-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aec45-148">RELATED LINKS</span></span>


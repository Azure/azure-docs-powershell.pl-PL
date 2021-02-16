---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 80ab75e2361cf052e88377e9d7a393fb36627ae7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203785"
---
# <span data-ttu-id="0c5a4-101">New-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="0c5a4-101">New-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="0c5a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c5a4-102">SYNOPSIS</span></span>
<span data-ttu-id="0c5a4-103">Tworzy główne przypisanie bazy danych klastrów Kusto.</span><span class="sxs-lookup"><span data-stu-id="0c5a4-103">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="0c5a4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0c5a4-104">SYNTAX</span></span>

```
New-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-PrincipalId <String>] [-PrincipalType <PrincipalType>] [-Role <DatabasePrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0c5a4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0c5a4-105">DESCRIPTION</span></span>
<span data-ttu-id="0c5a4-106">Tworzy główne przypisanie bazy danych klastrów Kusto.</span><span class="sxs-lookup"><span data-stu-id="0c5a4-106">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="0c5a4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0c5a4-107">EXAMPLES</span></span>

### <span data-ttu-id="0c5a4-108">Przykład 1. Tworzenie dyrektora bazy danych klastrów Kusto</span><span class="sxs-lookup"><span data-stu-id="0c5a4-108">Example 1: Create a Kusto cluster database principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role Admin

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="0c5a4-109">Powyższe polecenie tworzy przypisanie podmiotu bazy danych klastrów Kusto</span><span class="sxs-lookup"><span data-stu-id="0c5a4-109">The above command creates a Kusto cluster database principalAssignment</span></span>

## <span data-ttu-id="0c5a4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c5a4-110">PARAMETERS</span></span>

### <span data-ttu-id="0c5a4-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0c5a4-111">-AsJob</span></span>
<span data-ttu-id="0c5a4-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="0c5a4-112">Run the command as a job</span></span>

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

### <span data-ttu-id="0c5a4-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0c5a4-113">-ClusterName</span></span>
<span data-ttu-id="0c5a4-114">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="0c5a4-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="0c5a4-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0c5a4-115">-DatabaseName</span></span>
<span data-ttu-id="0c5a4-116">Nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="0c5a4-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="0c5a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c5a4-117">-DefaultProfile</span></span>
<span data-ttu-id="0c5a4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c5a4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c5a4-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0c5a4-119">-NoWait</span></span>
<span data-ttu-id="0c5a4-120">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="0c5a4-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0c5a4-121">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="0c5a4-121">-PrincipalAssignmentName</span></span>
<span data-ttu-id="0c5a4-122">Nazwa dopisu głównego Kusto.</span><span class="sxs-lookup"><span data-stu-id="0c5a4-122">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="0c5a4-123">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="0c5a4-123">-PrincipalId</span></span>
<span data-ttu-id="0c5a4-124">Identyfikator dyrektora przypisany do podmiotu zabezpieczeń bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0c5a4-124">The principal ID assigned to the database principal.</span></span>
<span data-ttu-id="0c5a4-125">Może to być adres e-mail użytkownika, identyfikator aplikacji lub nazwa grupy zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="0c5a4-125">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="0c5a4-126">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="0c5a4-126">-PrincipalType</span></span>
<span data-ttu-id="0c5a4-127">Typ dyrektora.</span><span class="sxs-lookup"><span data-stu-id="0c5a4-127">Principal type.</span></span>

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

### <span data-ttu-id="0c5a4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c5a4-128">-ResourceGroupName</span></span>
<span data-ttu-id="0c5a4-129">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0c5a4-129">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="0c5a4-130">- Rola</span><span class="sxs-lookup"><span data-stu-id="0c5a4-130">-Role</span></span>
<span data-ttu-id="0c5a4-131">Rola główna bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0c5a4-131">Database principal role.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DatabasePrincipalRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c5a4-132">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c5a4-132">-SubscriptionId</span></span>
<span data-ttu-id="0c5a4-133">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0c5a4-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0c5a4-134">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="0c5a4-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0c5a4-135">- TenantId</span><span class="sxs-lookup"><span data-stu-id="0c5a4-135">-TenantId</span></span>
<span data-ttu-id="0c5a4-136">Identyfikator dzierżawy dyrektora</span><span class="sxs-lookup"><span data-stu-id="0c5a4-136">The tenant id of the principal</span></span>

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

### <span data-ttu-id="0c5a4-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c5a4-137">-Confirm</span></span>
<span data-ttu-id="0c5a4-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0c5a4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c5a4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c5a4-139">-WhatIf</span></span>
<span data-ttu-id="0c5a4-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c5a4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c5a4-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0c5a4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c5a4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c5a4-142">CommonParameters</span></span>
<span data-ttu-id="0c5a4-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c5a4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c5a4-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c5a4-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c5a4-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c5a4-145">INPUTS</span></span>

## <span data-ttu-id="0c5a4-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0c5a4-146">OUTPUTS</span></span>

### <span data-ttu-id="0c5a4-147">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="0c5a4-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="0c5a4-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0c5a4-148">NOTES</span></span>

<span data-ttu-id="0c5a4-149">ALIASY</span><span class="sxs-lookup"><span data-stu-id="0c5a4-149">ALIASES</span></span>

## <span data-ttu-id="0c5a4-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c5a4-150">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 9fd729a85babf1440516c52f0e7737f4c0d0d281
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970689"
---
# <span data-ttu-id="cd480-101">New-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="cd480-101">New-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="cd480-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd480-102">SYNOPSIS</span></span>
<span data-ttu-id="cd480-103">Tworzy główne przypisanie bazy danych klastrów Kusto.</span><span class="sxs-lookup"><span data-stu-id="cd480-103">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="cd480-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cd480-104">SYNTAX</span></span>

```
New-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-PrincipalId <String>] [-PrincipalType <PrincipalType>] [-Role <DatabasePrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd480-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cd480-105">DESCRIPTION</span></span>
<span data-ttu-id="cd480-106">Tworzy główne przypisanie bazy danych klastrów Kusto.</span><span class="sxs-lookup"><span data-stu-id="cd480-106">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="cd480-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cd480-107">EXAMPLES</span></span>

### <span data-ttu-id="cd480-108">Przykład 1. Tworzenie dyrektora bazy danych klastrów Kusto</span><span class="sxs-lookup"><span data-stu-id="cd480-108">Example 1: Create a Kusto cluster database principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role Admin

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="cd480-109">Powyższe polecenie tworzy przypisanie podmiotu bazy danych klastrów Kusto</span><span class="sxs-lookup"><span data-stu-id="cd480-109">The above command creates a Kusto cluster database principalAssignment</span></span>

## <span data-ttu-id="cd480-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd480-110">PARAMETERS</span></span>

### <span data-ttu-id="cd480-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="cd480-111">-AsJob</span></span>
<span data-ttu-id="cd480-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="cd480-112">Run the command as a job</span></span>

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

### <span data-ttu-id="cd480-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cd480-113">-ClusterName</span></span>
<span data-ttu-id="cd480-114">Nazwa klastru Kusto.</span><span class="sxs-lookup"><span data-stu-id="cd480-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="cd480-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cd480-115">-DatabaseName</span></span>
<span data-ttu-id="cd480-116">Nazwa bazy danych w klastrze Kusto.</span><span class="sxs-lookup"><span data-stu-id="cd480-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="cd480-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd480-117">-DefaultProfile</span></span>
<span data-ttu-id="cd480-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd480-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd480-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cd480-119">-NoWait</span></span>
<span data-ttu-id="cd480-120">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="cd480-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cd480-121">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="cd480-121">-PrincipalAssignmentName</span></span>
<span data-ttu-id="cd480-122">Nazwa dopisu głównego( Kusto principalAssignment).</span><span class="sxs-lookup"><span data-stu-id="cd480-122">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="cd480-123">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="cd480-123">-PrincipalId</span></span>
<span data-ttu-id="cd480-124">Identyfikator dyrektora przypisany do podmiotu zabezpieczeń bazy danych.</span><span class="sxs-lookup"><span data-stu-id="cd480-124">The principal ID assigned to the database principal.</span></span>
<span data-ttu-id="cd480-125">Może to być adres e-mail użytkownika, identyfikator aplikacji lub nazwa grupy zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="cd480-125">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="cd480-126">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="cd480-126">-PrincipalType</span></span>
<span data-ttu-id="cd480-127">Typ dyrektora.</span><span class="sxs-lookup"><span data-stu-id="cd480-127">Principal type.</span></span>

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

### <span data-ttu-id="cd480-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd480-128">-ResourceGroupName</span></span>
<span data-ttu-id="cd480-129">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="cd480-129">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="cd480-130">- Rola</span><span class="sxs-lookup"><span data-stu-id="cd480-130">-Role</span></span>
<span data-ttu-id="cd480-131">Rola główna bazy danych.</span><span class="sxs-lookup"><span data-stu-id="cd480-131">Database principal role.</span></span>

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

### <span data-ttu-id="cd480-132">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd480-132">-SubscriptionId</span></span>
<span data-ttu-id="cd480-133">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cd480-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cd480-134">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="cd480-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cd480-135">- TenantId</span><span class="sxs-lookup"><span data-stu-id="cd480-135">-TenantId</span></span>
<span data-ttu-id="cd480-136">Identyfikator dzierżawy dyrektora</span><span class="sxs-lookup"><span data-stu-id="cd480-136">The tenant id of the principal</span></span>

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

### <span data-ttu-id="cd480-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd480-137">-Confirm</span></span>
<span data-ttu-id="cd480-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cd480-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd480-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd480-139">-WhatIf</span></span>
<span data-ttu-id="cd480-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd480-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd480-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cd480-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd480-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd480-142">CommonParameters</span></span>
<span data-ttu-id="cd480-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd480-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd480-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd480-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd480-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd480-145">INPUTS</span></span>

## <span data-ttu-id="cd480-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd480-146">OUTPUTS</span></span>

### <span data-ttu-id="cd480-147">Microsoft.Azure.PowerShell.Cmdlet.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="cd480-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="cd480-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cd480-148">NOTES</span></span>

<span data-ttu-id="cd480-149">ALIASY</span><span class="sxs-lookup"><span data-stu-id="cd480-149">ALIASES</span></span>

## <span data-ttu-id="cd480-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd480-150">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 80ab75e2361cf052e88377e9d7a393fb36627ae7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386295"
---
# <span data-ttu-id="7730b-101">New-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="7730b-101">New-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="7730b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7730b-102">SYNOPSIS</span></span>
<span data-ttu-id="7730b-103">Tworzy principalAssignment bazy danych Kusto klastra.</span><span class="sxs-lookup"><span data-stu-id="7730b-103">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="7730b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7730b-104">SYNTAX</span></span>

```
New-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-PrincipalId <String>] [-PrincipalType <PrincipalType>] [-Role <DatabasePrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7730b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7730b-105">DESCRIPTION</span></span>
<span data-ttu-id="7730b-106">Tworzy principalAssignment bazy danych Kusto klastra.</span><span class="sxs-lookup"><span data-stu-id="7730b-106">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="7730b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7730b-107">EXAMPLES</span></span>

### <span data-ttu-id="7730b-108">Przykład 1: Tworzenie Kusto bazy danych klastra principalAssignment</span><span class="sxs-lookup"><span data-stu-id="7730b-108">Example 1: Create a Kusto cluster database principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role Admin

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="7730b-109">Powyższe polecenie tworzy Kusto bazy danych klastra principalAssignment</span><span class="sxs-lookup"><span data-stu-id="7730b-109">The above command creates a Kusto cluster database principalAssignment</span></span>

## <span data-ttu-id="7730b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7730b-110">PARAMETERS</span></span>

### <span data-ttu-id="7730b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7730b-111">-AsJob</span></span>
<span data-ttu-id="7730b-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="7730b-112">Run the command as a job</span></span>

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

### <span data-ttu-id="7730b-113">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="7730b-113">-ClusterName</span></span>
<span data-ttu-id="7730b-114">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="7730b-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="7730b-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7730b-115">-DatabaseName</span></span>
<span data-ttu-id="7730b-116">Nazwa bazy danych w klastrze usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="7730b-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="7730b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7730b-117">-DefaultProfile</span></span>
<span data-ttu-id="7730b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7730b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7730b-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="7730b-119">-NoWait</span></span>
<span data-ttu-id="7730b-120">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="7730b-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7730b-121">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="7730b-121">-PrincipalAssignmentName</span></span>
<span data-ttu-id="7730b-122">Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="7730b-122">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="7730b-123">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="7730b-123">-PrincipalId</span></span>
<span data-ttu-id="7730b-124">Identyfikator podmiotu zabezpieczeń przypisany do podmiotu zabezpieczeń bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7730b-124">The principal ID assigned to the database principal.</span></span>
<span data-ttu-id="7730b-125">Może to być adres e-mail użytkownika, identyfikator aplikacji lub nazwa grupy zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="7730b-125">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="7730b-126">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="7730b-126">-PrincipalType</span></span>
<span data-ttu-id="7730b-127">Typ podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="7730b-127">Principal type.</span></span>

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

### <span data-ttu-id="7730b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7730b-128">-ResourceGroupName</span></span>
<span data-ttu-id="7730b-129">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="7730b-129">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="7730b-130">-Rola</span><span class="sxs-lookup"><span data-stu-id="7730b-130">-Role</span></span>
<span data-ttu-id="7730b-131">Rola główna bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7730b-131">Database principal role.</span></span>

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

### <span data-ttu-id="7730b-132">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7730b-132">-SubscriptionId</span></span>
<span data-ttu-id="7730b-133">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7730b-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7730b-134">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="7730b-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7730b-135">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="7730b-135">-TenantId</span></span>
<span data-ttu-id="7730b-136">Identyfikator dzierżawy głównej</span><span class="sxs-lookup"><span data-stu-id="7730b-136">The tenant id of the principal</span></span>

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

### <span data-ttu-id="7730b-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7730b-137">-Confirm</span></span>
<span data-ttu-id="7730b-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7730b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7730b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7730b-139">-WhatIf</span></span>
<span data-ttu-id="7730b-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7730b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7730b-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7730b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7730b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7730b-142">CommonParameters</span></span>
<span data-ttu-id="7730b-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7730b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7730b-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7730b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7730b-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7730b-145">INPUTS</span></span>

## <span data-ttu-id="7730b-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7730b-146">OUTPUTS</span></span>

### <span data-ttu-id="7730b-147">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200918. IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="7730b-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="7730b-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7730b-148">NOTES</span></span>

<span data-ttu-id="7730b-149">PISUJE</span><span class="sxs-lookup"><span data-stu-id="7730b-149">ALIASES</span></span>

## <span data-ttu-id="7730b-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7730b-150">RELATED LINKS</span></span>


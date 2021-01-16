---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 8f2a0cd576c3fe7f184d3f016f6666aa8749b5c2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336970"
---
# <span data-ttu-id="6e35e-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="6e35e-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="6e35e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e35e-102">SYNOPSIS</span></span>
<span data-ttu-id="6e35e-103">Utwórz Kusto klastra principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="6e35e-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="6e35e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e35e-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6e35e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6e35e-105">DESCRIPTION</span></span>
<span data-ttu-id="6e35e-106">Utwórz Kusto klastra principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="6e35e-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="6e35e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e35e-107">EXAMPLES</span></span>

### <span data-ttu-id="6e35e-108">Przykład 1: Tworzenie Kusto klastra principalAssignment</span><span class="sxs-lookup"><span data-stu-id="6e35e-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="6e35e-109">Powyższe polecenie tworzy principalAssignment klastra Kusto</span><span class="sxs-lookup"><span data-stu-id="6e35e-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="6e35e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e35e-110">PARAMETERS</span></span>

### <span data-ttu-id="6e35e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e35e-111">-AsJob</span></span>
<span data-ttu-id="6e35e-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="6e35e-112">Run the command as a job</span></span>

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

### <span data-ttu-id="6e35e-113">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="6e35e-113">-ClusterName</span></span>
<span data-ttu-id="6e35e-114">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="6e35e-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="6e35e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e35e-115">-DefaultProfile</span></span>
<span data-ttu-id="6e35e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e35e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e35e-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6e35e-117">-NoWait</span></span>
<span data-ttu-id="6e35e-118">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="6e35e-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6e35e-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="6e35e-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="6e35e-120">Nazwa Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="6e35e-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="6e35e-121">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="6e35e-121">-PrincipalId</span></span>
<span data-ttu-id="6e35e-122">Identyfikator podmiotu zabezpieczeń przypisany do podmiotu zabezpieczeń klastra.</span><span class="sxs-lookup"><span data-stu-id="6e35e-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="6e35e-123">Może to być adres e-mail użytkownika, identyfikator aplikacji lub nazwa grupy zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="6e35e-123">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="6e35e-124">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="6e35e-124">-PrincipalType</span></span>
<span data-ttu-id="6e35e-125">Typ podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="6e35e-125">Principal type.</span></span>

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

### <span data-ttu-id="6e35e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e35e-126">-ResourceGroupName</span></span>
<span data-ttu-id="6e35e-127">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="6e35e-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="6e35e-128">-Rola</span><span class="sxs-lookup"><span data-stu-id="6e35e-128">-Role</span></span>
<span data-ttu-id="6e35e-129">Rola główna klastra.</span><span class="sxs-lookup"><span data-stu-id="6e35e-129">Cluster principal role.</span></span>

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

### <span data-ttu-id="6e35e-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6e35e-130">-SubscriptionId</span></span>
<span data-ttu-id="6e35e-131">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6e35e-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6e35e-132">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="6e35e-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6e35e-133">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="6e35e-133">-TenantId</span></span>
<span data-ttu-id="6e35e-134">Identyfikator dzierżawy głównej</span><span class="sxs-lookup"><span data-stu-id="6e35e-134">The tenant id of the principal</span></span>

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

### <span data-ttu-id="6e35e-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6e35e-135">-Confirm</span></span>
<span data-ttu-id="6e35e-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e35e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e35e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e35e-137">-WhatIf</span></span>
<span data-ttu-id="6e35e-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e35e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e35e-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6e35e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e35e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e35e-140">CommonParameters</span></span>
<span data-ttu-id="6e35e-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e35e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e35e-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e35e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e35e-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e35e-143">INPUTS</span></span>

## <span data-ttu-id="6e35e-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e35e-144">OUTPUTS</span></span>

### <span data-ttu-id="6e35e-145">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="6e35e-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="6e35e-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e35e-146">NOTES</span></span>

<span data-ttu-id="6e35e-147">PISUJE</span><span class="sxs-lookup"><span data-stu-id="6e35e-147">ALIASES</span></span>

## <span data-ttu-id="6e35e-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e35e-148">RELATED LINKS</span></span>


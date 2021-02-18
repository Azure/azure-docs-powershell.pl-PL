---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
ms.openlocfilehash: 44c12e08ca66c19cf3541f4abb200e1ba0663208
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193163"
---
# <span data-ttu-id="b803c-101">Get-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="b803c-101">Get-AzPolicyRemediation</span></span>

## <span data-ttu-id="b803c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b803c-102">SYNOPSIS</span></span>
<span data-ttu-id="b803c-103">Pobiera działania naprawcze dotyczące zasad.</span><span class="sxs-lookup"><span data-stu-id="b803c-103">Gets policy remediations.</span></span>

## <span data-ttu-id="b803c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b803c-104">SYNTAX</span></span>

### <span data-ttu-id="b803c-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b803c-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b803c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b803c-106">ByName</span></span>
```
Get-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b803c-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="b803c-107">GenericScope</span></span>
```
Get-AzPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b803c-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="b803c-108">ManagementGroupScope</span></span>
```
Get-AzPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b803c-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="b803c-109">ResourceGroupScope</span></span>
```
Get-AzPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b803c-110">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b803c-110">ByResourceId</span></span>
```
Get-AzPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b803c-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="b803c-111">DESCRIPTION</span></span>
<span data-ttu-id="b803c-112">Polecenie **cmdlet Get-AzPolicyRemediation** pobiera wszystkie działania naprawcze dotyczące zasad w zakresie lub w określonym działaniach naprawczych.</span><span class="sxs-lookup"><span data-stu-id="b803c-112">The **Get-AzPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="b803c-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b803c-113">EXAMPLES</span></span>

### <span data-ttu-id="b803c-114">Przykład 1. Uzyskiwanie wszystkich działań naprawczych w ramach bieżącej subskrypcji zasad</span><span class="sxs-lookup"><span data-stu-id="b803c-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Get-AzPolicyRemediation
```

<span data-ttu-id="b803c-115">To polecenie pobiera wszystkie działania naprawcze utworzone w ramach subskrypcji o nazwie "Moja subskrypcja" lub pod nią.</span><span class="sxs-lookup"><span data-stu-id="b803c-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="b803c-116">Przykład 2. Uzyskiwanie określonych środków zaradczych dotyczących zasad i szczegółów wdrożenia</span><span class="sxs-lookup"><span data-stu-id="b803c-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="b803c-117">To polecenie pobiera działania naprawcze o nazwie "remediation1" z grupy zasobów "myResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="b803c-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="b803c-118">Zostaną uwzględnione szczegóły zasobów, których działania naprawcze zostaną uwzględnione.</span><span class="sxs-lookup"><span data-stu-id="b803c-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="b803c-119">Przykład 3. Uzyskiwanie 10 środków zaradczych zasad w grupie zarządzania z filtrami opcjonalnymi</span><span class="sxs-lookup"><span data-stu-id="b803c-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="b803c-120">To polecenie otrzymuje maksymalnie 10 działań naprawczych w zasadach od grupy zarządzania o nazwie "mg1".</span><span class="sxs-lookup"><span data-stu-id="b803c-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="b803c-121">Zostaną pobrane tylko działania naprawcze dotyczące zasad dla danego przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="b803c-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="b803c-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b803c-122">PARAMETERS</span></span>

### <span data-ttu-id="b803c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b803c-123">-DefaultProfile</span></span>
<span data-ttu-id="b803c-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b803c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b803c-125">— Filtr</span><span class="sxs-lookup"><span data-stu-id="b803c-125">-Filter</span></span>
<span data-ttu-id="b803c-126">Wyrażenie filtru przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="b803c-126">Filter expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, GenericScope, ManagementGroupScope, ResourceGroupScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b803c-127">- IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="b803c-127">-IncludeDetail</span></span>
<span data-ttu-id="b803c-128">Uwzględnij szczegóły wdrożeń utworzonych w działaniach naprawczych.</span><span class="sxs-lookup"><span data-stu-id="b803c-128">Include details of the deployments created by the remediation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b803c-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="b803c-129">-ManagementGroupName</span></span>
<span data-ttu-id="b803c-130">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="b803c-130">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b803c-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b803c-131">-Name</span></span>
<span data-ttu-id="b803c-132">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="b803c-132">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b803c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b803c-133">-ResourceGroupName</span></span>
<span data-ttu-id="b803c-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b803c-134">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b803c-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b803c-135">-ResourceId</span></span>
<span data-ttu-id="b803c-136">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="b803c-136">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b803c-137">— Zakres</span><span class="sxs-lookup"><span data-stu-id="b803c-137">-Scope</span></span>
<span data-ttu-id="b803c-138">Zakres zasobu.</span><span class="sxs-lookup"><span data-stu-id="b803c-138">Scope of the resource.</span></span> <span data-ttu-id="b803c-139">Na przykład'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="b803c-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GenericScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b803c-140">— Na górze</span><span class="sxs-lookup"><span data-stu-id="b803c-140">-Top</span></span>
<span data-ttu-id="b803c-141">Maksymalna liczba rekordów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="b803c-141">Maximum number of records to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b803c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b803c-142">CommonParameters</span></span>
<span data-ttu-id="b803c-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b803c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b803c-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b803c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b803c-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b803c-145">INPUTS</span></span>

### <span data-ttu-id="b803c-146">System.String</span><span class="sxs-lookup"><span data-stu-id="b803c-146">System.String</span></span>

## <span data-ttu-id="b803c-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b803c-147">OUTPUTS</span></span>

### <span data-ttu-id="b803c-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="b803c-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="b803c-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b803c-149">NOTES</span></span>

## <span data-ttu-id="b803c-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b803c-150">RELATED LINKS</span></span>

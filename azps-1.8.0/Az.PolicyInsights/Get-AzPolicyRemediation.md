---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
ms.openlocfilehash: 44f7d3331d32092636c53850b0315f34b7df7808
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708794"
---
# <span data-ttu-id="85306-101">Get-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="85306-101">Get-AzPolicyRemediation</span></span>

## <span data-ttu-id="85306-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85306-102">SYNOPSIS</span></span>
<span data-ttu-id="85306-103">Pobiera korygowanie zasad.</span><span class="sxs-lookup"><span data-stu-id="85306-103">Gets policy remediations.</span></span>

## <span data-ttu-id="85306-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85306-104">SYNTAX</span></span>

### <span data-ttu-id="85306-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="85306-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85306-106">ByName</span><span class="sxs-lookup"><span data-stu-id="85306-106">ByName</span></span>
```
Get-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85306-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="85306-107">GenericScope</span></span>
```
Get-AzPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85306-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="85306-108">ManagementGroupScope</span></span>
```
Get-AzPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85306-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="85306-109">ResourceGroupScope</span></span>
```
Get-AzPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85306-110">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="85306-110">ByResourceId</span></span>
```
Get-AzPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85306-111">Opis</span><span class="sxs-lookup"><span data-stu-id="85306-111">DESCRIPTION</span></span>
<span data-ttu-id="85306-112">Polecenie cmdlet **Get-AzPolicyRemediation** pobiera wszystkie korygowanie zasad w zakresie lub korygowanie.</span><span class="sxs-lookup"><span data-stu-id="85306-112">The **Get-AzPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="85306-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85306-113">EXAMPLES</span></span>

### <span data-ttu-id="85306-114">Przykład 1: uzyskiwanie wszystkich korekt zasad w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="85306-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Get-AzPolicyRemediation
```

<span data-ttu-id="85306-115">To polecenie umożliwia pobieranie wszystkich korekt utworzonych w ramach abonamentu o nazwie "Moja subskrypcja" lub pod nim.</span><span class="sxs-lookup"><span data-stu-id="85306-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="85306-116">Przykład 2: uzyskiwanie określonych korekt zasad i szczegółów wdrożenia</span><span class="sxs-lookup"><span data-stu-id="85306-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="85306-117">To polecenie pobiera korygowanie o nazwie "remediation1" z grupy zasobów "Moja zasobów".</span><span class="sxs-lookup"><span data-stu-id="85306-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="85306-118">Zostaną uwzględnione dane dotyczące korygowanych zasobów.</span><span class="sxs-lookup"><span data-stu-id="85306-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="85306-119">Przykład 3: Uzyskaj 10 korekt zasad w grupie zarządzania z filtrami opcjonalnymi</span><span class="sxs-lookup"><span data-stu-id="85306-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="85306-120">To polecenie pobiera maksymalnie 10 korekt zasad z grupy zarządzania o nazwie "MG1".</span><span class="sxs-lookup"><span data-stu-id="85306-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="85306-121">Zostaną pobrane tylko korygowanie zasad dla danego przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="85306-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="85306-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85306-122">PARAMETERS</span></span>

### <span data-ttu-id="85306-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85306-123">-DefaultProfile</span></span>
<span data-ttu-id="85306-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85306-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85306-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="85306-125">-Filter</span></span>
<span data-ttu-id="85306-126">Wyrażenie filtru przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="85306-126">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="85306-127">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="85306-127">-IncludeDetail</span></span>
<span data-ttu-id="85306-128">Uwzględnij szczegóły wdrożeń utworzonych przez korygowanie.</span><span class="sxs-lookup"><span data-stu-id="85306-128">Include details of the deployments created by the remediation.</span></span>

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

### <span data-ttu-id="85306-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="85306-129">-ManagementGroupName</span></span>
<span data-ttu-id="85306-130">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="85306-130">Management group ID.</span></span>

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

### <span data-ttu-id="85306-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="85306-131">-Name</span></span>
<span data-ttu-id="85306-132">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="85306-132">Resource name.</span></span>

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

### <span data-ttu-id="85306-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85306-133">-ResourceGroupName</span></span>
<span data-ttu-id="85306-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="85306-134">Resource group name.</span></span>

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

### <span data-ttu-id="85306-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85306-135">-ResourceId</span></span>
<span data-ttu-id="85306-136">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="85306-136">Resource ID.</span></span>

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

### <span data-ttu-id="85306-137">-Zakres</span><span class="sxs-lookup"><span data-stu-id="85306-137">-Scope</span></span>
<span data-ttu-id="85306-138">Zakres zasobu.</span><span class="sxs-lookup"><span data-stu-id="85306-138">Scope of the resource.</span></span> <span data-ttu-id="85306-139">Na przykład "/subscriptions/{subscriptionId}/resourceGroups/{rgName}".</span><span class="sxs-lookup"><span data-stu-id="85306-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="85306-140">-Początek</span><span class="sxs-lookup"><span data-stu-id="85306-140">-Top</span></span>
<span data-ttu-id="85306-141">Maksymalna liczba rekordów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="85306-141">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="85306-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85306-142">CommonParameters</span></span>
<span data-ttu-id="85306-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85306-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85306-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85306-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85306-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85306-145">INPUTS</span></span>

### <span data-ttu-id="85306-146">System. String</span><span class="sxs-lookup"><span data-stu-id="85306-146">System.String</span></span>

## <span data-ttu-id="85306-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85306-147">OUTPUTS</span></span>

### <span data-ttu-id="85306-148">Microsoft. Azure. Commands. PolicyInsights. MODELES. remediacja. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="85306-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="85306-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85306-149">NOTES</span></span>

## <span data-ttu-id="85306-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85306-150">RELATED LINKS</span></span>
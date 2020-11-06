---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyRemediation.md
ms.openlocfilehash: e69ad25800dbf6aada7111a1093b4c878f3c0f9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551147"
---
# <span data-ttu-id="a18eb-101">Get-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="a18eb-101">Get-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="a18eb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a18eb-102">SYNOPSIS</span></span>
<span data-ttu-id="a18eb-103">Pobiera korygowanie zasad.</span><span class="sxs-lookup"><span data-stu-id="a18eb-103">Gets policy remediations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a18eb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a18eb-104">SYNTAX</span></span>

### <span data-ttu-id="a18eb-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a18eb-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a18eb-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a18eb-106">ByName</span></span>
```
Get-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a18eb-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="a18eb-107">GenericScope</span></span>
```
Get-AzureRmPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a18eb-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="a18eb-108">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a18eb-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="a18eb-109">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a18eb-110">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a18eb-110">ByResourceId</span></span>
```
Get-AzureRmPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a18eb-111">Opis</span><span class="sxs-lookup"><span data-stu-id="a18eb-111">DESCRIPTION</span></span>
<span data-ttu-id="a18eb-112">Polecenie cmdlet **Get-AzureRmPolicyRemediation** pobiera wszystkie korygowanie zasad w zakresie lub korygowanie.</span><span class="sxs-lookup"><span data-stu-id="a18eb-112">The **Get-AzureRmPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="a18eb-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a18eb-113">EXAMPLES</span></span>

### <span data-ttu-id="a18eb-114">Przykład 1: uzyskiwanie wszystkich korekt zasad w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a18eb-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzureRmSubscription -Subscription "My Subscription"
PS C:\> Get-AzureRmPolicyRemediation
```

<span data-ttu-id="a18eb-115">To polecenie umożliwia pobieranie wszystkich korekt utworzonych w ramach abonamentu o nazwie "Moja subskrypcja" lub pod nim.</span><span class="sxs-lookup"><span data-stu-id="a18eb-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="a18eb-116">Przykład 2: uzyskiwanie określonych korekt zasad i szczegółów wdrożenia</span><span class="sxs-lookup"><span data-stu-id="a18eb-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzureRmPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="a18eb-117">To polecenie pobiera korygowanie o nazwie "remediation1" z grupy zasobów "Moja zasobów".</span><span class="sxs-lookup"><span data-stu-id="a18eb-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="a18eb-118">Zostaną uwzględnione dane dotyczące korygowanych zasobów.</span><span class="sxs-lookup"><span data-stu-id="a18eb-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="a18eb-119">Przykład 3: Uzyskaj 10 korekt zasad w grupie zarządzania z filtrami opcjonalnymi</span><span class="sxs-lookup"><span data-stu-id="a18eb-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzureRmPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="a18eb-120">To polecenie pobiera maksymalnie 10 korekt zasad z grupy zarządzania o nazwie "MG1".</span><span class="sxs-lookup"><span data-stu-id="a18eb-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="a18eb-121">Zostaną pobrane tylko korygowanie zasad dla danego przydziału zasad.</span><span class="sxs-lookup"><span data-stu-id="a18eb-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="a18eb-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a18eb-122">PARAMETERS</span></span>

### <span data-ttu-id="a18eb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a18eb-123">-DefaultProfile</span></span>
<span data-ttu-id="a18eb-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a18eb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a18eb-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="a18eb-125">-Filter</span></span>
<span data-ttu-id="a18eb-126">Wyrażenie filtru przy użyciu notacji OData.</span><span class="sxs-lookup"><span data-stu-id="a18eb-126">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="a18eb-127">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="a18eb-127">-IncludeDetail</span></span>
<span data-ttu-id="a18eb-128">Uwzględnij szczegóły wdrożeń utworzonych przez korygowanie.</span><span class="sxs-lookup"><span data-stu-id="a18eb-128">Include details of the deployments created by the remediation.</span></span>

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

### <span data-ttu-id="a18eb-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a18eb-129">-ManagementGroupName</span></span>
<span data-ttu-id="a18eb-130">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="a18eb-130">Management group ID.</span></span>

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

### <span data-ttu-id="a18eb-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a18eb-131">-Name</span></span>
<span data-ttu-id="a18eb-132">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a18eb-132">Resource name.</span></span>

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

### <span data-ttu-id="a18eb-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a18eb-133">-ResourceGroupName</span></span>
<span data-ttu-id="a18eb-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a18eb-134">Resource group name.</span></span>

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

### <span data-ttu-id="a18eb-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a18eb-135">-ResourceId</span></span>
<span data-ttu-id="a18eb-136">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="a18eb-136">Resource ID.</span></span>

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

### <span data-ttu-id="a18eb-137">-Zakres</span><span class="sxs-lookup"><span data-stu-id="a18eb-137">-Scope</span></span>
<span data-ttu-id="a18eb-138">Zakres zasobu.</span><span class="sxs-lookup"><span data-stu-id="a18eb-138">Scope of the resource.</span></span> <span data-ttu-id="a18eb-139">Na przykład "/subscriptions/{subscriptionId}/resourceGroups/{rgName}".</span><span class="sxs-lookup"><span data-stu-id="a18eb-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="a18eb-140">-Początek</span><span class="sxs-lookup"><span data-stu-id="a18eb-140">-Top</span></span>
<span data-ttu-id="a18eb-141">Maksymalna liczba rekordów do zwrócenia.</span><span class="sxs-lookup"><span data-stu-id="a18eb-141">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="a18eb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a18eb-142">CommonParameters</span></span>
<span data-ttu-id="a18eb-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a18eb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a18eb-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a18eb-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a18eb-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a18eb-145">INPUTS</span></span>

### <span data-ttu-id="a18eb-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a18eb-146">System.String</span></span>

## <span data-ttu-id="a18eb-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a18eb-147">OUTPUTS</span></span>

### <span data-ttu-id="a18eb-148">Microsoft. Azure. Commands. PolicyInsights. MODELES. remediacja. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="a18eb-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="a18eb-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a18eb-149">NOTES</span></span>

## <span data-ttu-id="a18eb-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a18eb-150">RELATED LINKS</span></span>

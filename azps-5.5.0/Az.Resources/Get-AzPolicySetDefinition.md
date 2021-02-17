---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 4ec965e63a779a5b0ebb606819e5e9f7f20b035e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192779"
---
# <span data-ttu-id="c3299-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="c3299-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="c3299-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3299-102">SYNOPSIS</span></span>
<span data-ttu-id="c3299-103">Pobiera definicje zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="c3299-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="c3299-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c3299-104">SYNTAX</span></span>

### <span data-ttu-id="c3299-105">NameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c3299-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3299-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3299-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3299-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3299-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3299-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3299-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3299-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3299-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3299-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3299-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3299-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="c3299-111">DESCRIPTION</span></span>
<span data-ttu-id="c3299-112">Polecenie **cmdlet Get-AzPolicySetDefinition** pobiera kolekcję definicji zestawu zasad lub określoną definicję zestawu zasad określoną za pomocą nazwy lub identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="c3299-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="c3299-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c3299-113">EXAMPLES</span></span>

### <span data-ttu-id="c3299-114">Przykład 1. Pobierz wszystkie definicje zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="c3299-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="c3299-115">To polecenie pobiera wszystkie definicje zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="c3299-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="c3299-116">Przykład 2. Uzyskiwanie definicji zestawu zasad z bieżącej subskrypcji według nazwy</span><span class="sxs-lookup"><span data-stu-id="c3299-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="c3299-117">To polecenie pobiera definicję zestawu zasad o nazwie VMPolicySetDefinition z bieżącej subskrypcji domyślnej.</span><span class="sxs-lookup"><span data-stu-id="c3299-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="c3299-118">Przykład 3. Uzyskiwanie definicji zestawu zasad z subskrypcji według nazwy</span><span class="sxs-lookup"><span data-stu-id="c3299-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="c3299-119">To polecenie pobiera definicję zasad o nazwie VMPolicySetDefinition z subskrypcji o identyfikatorze 3bf44b72-c631-427a-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="c3299-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="c3299-120">Przykład 4. Uzyskiwanie wszystkich definicji niestandardowych zestawu zasad z grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="c3299-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="c3299-121">To polecenie pobiera wszystkie definicje niestandardowych zestawu zasad z grupy zarządzania o nazwie Sprz42.</span><span class="sxs-lookup"><span data-stu-id="c3299-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

### <span data-ttu-id="c3299-122">Przykład 5. Uzyskiwanie definicji zestawu zasad z danej kategorii</span><span class="sxs-lookup"><span data-stu-id="c3299-122">Example 5: Get policy set definitions from a given category</span></span>
```
PS C:\> Get-AzPolicySetDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="c3299-123">To polecenie pobiera wszystkie definicje zestawu zasad w kategorii "Maszyny wirtualnej".</span><span class="sxs-lookup"><span data-stu-id="c3299-123">This command gets all policy set definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="c3299-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3299-124">PARAMETERS</span></span>

### <span data-ttu-id="c3299-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c3299-125">-ApiVersion</span></span>
<span data-ttu-id="c3299-126">Po jego skonfigurowaniu wskazuje wersję interfejsu API dostawcy zasobów, która ma być dostępna.</span><span class="sxs-lookup"><span data-stu-id="c3299-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c3299-127">Jeśli nie zostanie określona, wersja interfejsu API jest automatycznie określana jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="c3299-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c3299-128">— wbudowane</span><span class="sxs-lookup"><span data-stu-id="c3299-128">-Builtin</span></span>
<span data-ttu-id="c3299-129">Ogranicza listę wyników tylko do wbudowanych definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="c3299-129">Limits list of results to only built-in policy set definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BuiltinFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3299-130">— Niestandardowe</span><span class="sxs-lookup"><span data-stu-id="c3299-130">-Custom</span></span>
<span data-ttu-id="c3299-131">Ograniczenie listy wyników tylko do definicji niestandardowych zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="c3299-131">Limits list of results to only custom policy set definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CustomFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3299-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3299-132">-DefaultProfile</span></span>
<span data-ttu-id="c3299-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c3299-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3299-134">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="c3299-134">-Id</span></span>
<span data-ttu-id="c3299-135">W pełni kwalifikowany identyfikator definicji zestawu zasad, łącznie z subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="c3299-135">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="c3299-136">np. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="c3299-136">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3299-137">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="c3299-137">-ManagementGroupName</span></span>
<span data-ttu-id="c3299-138">Nazwa grupy zarządzania, do których mają być ustawione definicje zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="c3299-138">The name of the management group of the policy set definition(s) to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3299-139">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c3299-139">-Name</span></span>
<span data-ttu-id="c3299-140">Nazwa definicji ustawiona przez zasady.</span><span class="sxs-lookup"><span data-stu-id="c3299-140">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3299-141">— Przed</span><span class="sxs-lookup"><span data-stu-id="c3299-141">-Pre</span></span>
<span data-ttu-id="c3299-142">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="c3299-142">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c3299-143">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c3299-143">-SubscriptionId</span></span>
<span data-ttu-id="c3299-144">Identyfikator subskrypcji definicji zestawu zasad do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="c3299-144">The subscription ID of the policy set definition(s) to get.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3299-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3299-145">CommonParameters</span></span>
<span data-ttu-id="c3299-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3299-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3299-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3299-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3299-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3299-148">INPUTS</span></span>

### <span data-ttu-id="c3299-149">System.String</span><span class="sxs-lookup"><span data-stu-id="c3299-149">System.String</span></span>

### <span data-ttu-id="c3299-150">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c3299-150">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c3299-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3299-151">OUTPUTS</span></span>

### <span data-ttu-id="c3299-152">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="c3299-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c3299-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c3299-153">NOTES</span></span>

## <span data-ttu-id="c3299-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3299-154">RELATED LINKS</span></span>

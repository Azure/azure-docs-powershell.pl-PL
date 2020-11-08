---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 4ec965e63a779a5b0ebb606819e5e9f7f20b035e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062139"
---
# <span data-ttu-id="11396-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="11396-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="11396-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11396-102">SYNOPSIS</span></span>
<span data-ttu-id="11396-103">Pobiera definicje zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="11396-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="11396-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11396-104">SYNTAX</span></span>

### <span data-ttu-id="11396-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="11396-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11396-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="11396-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11396-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11396-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11396-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11396-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="11396-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="11396-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11396-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="11396-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11396-111">Opis</span><span class="sxs-lookup"><span data-stu-id="11396-111">DESCRIPTION</span></span>
<span data-ttu-id="11396-112">Polecenie cmdlet **Get-AzPolicySetDefinition** Pobiera kolekcję definicji zestawu zasad lub określoną definicję zestawu zasad zidentyfikowaną według nazwy lub identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="11396-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="11396-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11396-113">EXAMPLES</span></span>

### <span data-ttu-id="11396-114">Przykład 1: pobieranie wszystkich definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="11396-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="11396-115">To polecenie umożliwia pobieranie wszystkich definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="11396-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="11396-116">Przykład 2: uzyskiwanie definicji zestawu zasad z bieżącego abonamentu według nazwy</span><span class="sxs-lookup"><span data-stu-id="11396-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="11396-117">To polecenie pobiera definicję zestawu zasad o nazwie VMPolicySetDefinition z bieżącej subskrypcji domyślnej.</span><span class="sxs-lookup"><span data-stu-id="11396-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="11396-118">Przykład 3: uzyskiwanie definicji zestawu zasad z subskrypcji według nazwy</span><span class="sxs-lookup"><span data-stu-id="11396-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="11396-119">To polecenie pobiera definicję zasad o nazwie VMPolicySetDefinition z subskrypcji z IDENTYFIKATORem 3bf44b72-c631-427A-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="11396-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="11396-120">Przykład 4: pobieranie wszystkich definicji zestawu zasad niestandardowych z grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="11396-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="11396-121">To polecenie pobiera wszystkie definicje niestandardowych zestawów zasad z grupy zarządzania o nazwie Dept42.</span><span class="sxs-lookup"><span data-stu-id="11396-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

### <span data-ttu-id="11396-122">Przykład 5: uzyskiwanie definicji zestawu zasad z danej kategorii</span><span class="sxs-lookup"><span data-stu-id="11396-122">Example 5: Get policy set definitions from a given category</span></span>
```
PS C:\> Get-AzPolicySetDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="11396-123">To polecenie pobiera wszystkie definicje zestawu zasad w kategorii "maszyna wirtualna".</span><span class="sxs-lookup"><span data-stu-id="11396-123">This command gets all policy set definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="11396-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11396-124">PARAMETERS</span></span>

### <span data-ttu-id="11396-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="11396-125">-ApiVersion</span></span>
<span data-ttu-id="11396-126">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="11396-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="11396-127">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="11396-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="11396-128">-Wbudowane</span><span class="sxs-lookup"><span data-stu-id="11396-128">-Builtin</span></span>
<span data-ttu-id="11396-129">Ograniczenie listy wyników tylko do wbudowanych definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="11396-129">Limits list of results to only built-in policy set definitions.</span></span>

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

### <span data-ttu-id="11396-130">-Custom</span><span class="sxs-lookup"><span data-stu-id="11396-130">-Custom</span></span>
<span data-ttu-id="11396-131">Ogranicza listę wyników tylko do definicji niestandardowych zestawów zasad.</span><span class="sxs-lookup"><span data-stu-id="11396-131">Limits list of results to only custom policy set definitions.</span></span>

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

### <span data-ttu-id="11396-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11396-132">-DefaultProfile</span></span>
<span data-ttu-id="11396-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="11396-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11396-134">-ID</span><span class="sxs-lookup"><span data-stu-id="11396-134">-Id</span></span>
<span data-ttu-id="11396-135">W pełni kwalifikowany identyfikator definicji zestawu zasad, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="11396-135">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="11396-136">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="11396-136">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="11396-137">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="11396-137">-ManagementGroupName</span></span>
<span data-ttu-id="11396-138">Nazwa grupy zarządzania definicji zestawu zasad do pobrania.</span><span class="sxs-lookup"><span data-stu-id="11396-138">The name of the management group of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="11396-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="11396-139">-Name</span></span>
<span data-ttu-id="11396-140">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="11396-140">The policy set definition name.</span></span>

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

### <span data-ttu-id="11396-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="11396-141">-Pre</span></span>
<span data-ttu-id="11396-142">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="11396-142">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="11396-143">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="11396-143">-SubscriptionId</span></span>
<span data-ttu-id="11396-144">Identyfikator subskrypcji definicji zestawu zasad do pobrania.</span><span class="sxs-lookup"><span data-stu-id="11396-144">The subscription ID of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="11396-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11396-145">CommonParameters</span></span>
<span data-ttu-id="11396-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11396-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11396-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11396-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11396-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11396-148">INPUTS</span></span>

### <span data-ttu-id="11396-149">System. String</span><span class="sxs-lookup"><span data-stu-id="11396-149">System.String</span></span>

### <span data-ttu-id="11396-150">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="11396-150">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="11396-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11396-151">OUTPUTS</span></span>

### <span data-ttu-id="11396-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="11396-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="11396-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11396-153">NOTES</span></span>

## <span data-ttu-id="11396-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11396-154">RELATED LINKS</span></span>

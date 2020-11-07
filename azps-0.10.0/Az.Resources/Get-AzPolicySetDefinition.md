---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 100eb4f58a9fe946c17485b34b9cb8ffaacab6c5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892590"
---
# <span data-ttu-id="68f5b-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="68f5b-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="68f5b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68f5b-102">SYNOPSIS</span></span>
<span data-ttu-id="68f5b-103">Pobiera definicje zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="68f5b-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="68f5b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68f5b-104">SYNTAX</span></span>

### <span data-ttu-id="68f5b-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="68f5b-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68f5b-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="68f5b-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68f5b-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68f5b-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68f5b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68f5b-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68f5b-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="68f5b-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68f5b-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="68f5b-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68f5b-111">Opis</span><span class="sxs-lookup"><span data-stu-id="68f5b-111">DESCRIPTION</span></span>
<span data-ttu-id="68f5b-112">Polecenie cmdlet **Get-AzPolicySetDefinition** Pobiera kolekcję definicji zestawu zasad lub określoną definicję zestawu zasad zidentyfikowaną według nazwy lub identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="68f5b-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="68f5b-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68f5b-113">EXAMPLES</span></span>

### <span data-ttu-id="68f5b-114">Przykład 1: pobieranie wszystkich definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="68f5b-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="68f5b-115">To polecenie umożliwia pobieranie wszystkich definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="68f5b-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="68f5b-116">Przykład 2: uzyskiwanie definicji zestawu zasad z bieżącego abonamentu według nazwy</span><span class="sxs-lookup"><span data-stu-id="68f5b-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="68f5b-117">To polecenie pobiera definicję zestawu zasad o nazwie VMPolicySetDefinition z bieżącej subskrypcji domyślnej.</span><span class="sxs-lookup"><span data-stu-id="68f5b-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="68f5b-118">Przykład 3: uzyskiwanie definicji zestawu zasad z subskrypcji według nazwy</span><span class="sxs-lookup"><span data-stu-id="68f5b-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="68f5b-119">To polecenie pobiera definicję zasad o nazwie VMPolicySetDefinition z subskrypcji z IDENTYFIKATORem 3bf44b72-c631-427A-b8c8-53e2595398ca.</span><span class="sxs-lookup"><span data-stu-id="68f5b-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="68f5b-120">Przykład 4: pobieranie wszystkich definicji zestawu zasad niestandardowych z grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="68f5b-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="68f5b-121">To polecenie pobiera wszystkie definicje niestandardowych zestawów zasad z grupy zarządzania o nazwie Dept42.</span><span class="sxs-lookup"><span data-stu-id="68f5b-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

## <span data-ttu-id="68f5b-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68f5b-122">PARAMETERS</span></span>

### <span data-ttu-id="68f5b-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="68f5b-123">-ApiVersion</span></span>
<span data-ttu-id="68f5b-124">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="68f5b-124">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="68f5b-125">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="68f5b-125">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="68f5b-126">-Wbudowane</span><span class="sxs-lookup"><span data-stu-id="68f5b-126">-Builtin</span></span>
<span data-ttu-id="68f5b-127">Ograniczenie listy wyników tylko do wbudowanych definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="68f5b-127">Limits list of results to only built-in policy set definitions.</span></span>

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

### <span data-ttu-id="68f5b-128">-Custom</span><span class="sxs-lookup"><span data-stu-id="68f5b-128">-Custom</span></span>
<span data-ttu-id="68f5b-129">Ogranicza listę wyników tylko do definicji niestandardowych zestawów zasad.</span><span class="sxs-lookup"><span data-stu-id="68f5b-129">Limits list of results to only custom policy set definitions.</span></span>

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

### <span data-ttu-id="68f5b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68f5b-130">-DefaultProfile</span></span>
<span data-ttu-id="68f5b-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="68f5b-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f5b-132">-ID</span><span class="sxs-lookup"><span data-stu-id="68f5b-132">-Id</span></span>
<span data-ttu-id="68f5b-133">W pełni kwalifikowany identyfikator definicji zestawu zasad, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="68f5b-133">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="68f5b-134">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="68f5b-134">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="68f5b-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="68f5b-135">-ManagementGroupName</span></span>
<span data-ttu-id="68f5b-136">Nazwa grupy zarządzania definicji zestawu zasad do pobrania.</span><span class="sxs-lookup"><span data-stu-id="68f5b-136">The name of the management group of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="68f5b-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="68f5b-137">-Name</span></span>
<span data-ttu-id="68f5b-138">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="68f5b-138">The policy set definition name.</span></span>

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

### <span data-ttu-id="68f5b-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="68f5b-139">-Pre</span></span>
<span data-ttu-id="68f5b-140">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="68f5b-140">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="68f5b-141">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="68f5b-141">-SubscriptionId</span></span>
<span data-ttu-id="68f5b-142">Identyfikator subskrypcji definicji zestawu zasad do pobrania.</span><span class="sxs-lookup"><span data-stu-id="68f5b-142">The subscription ID of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="68f5b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68f5b-143">CommonParameters</span></span>
<span data-ttu-id="68f5b-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68f5b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68f5b-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68f5b-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68f5b-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68f5b-146">INPUTS</span></span>

### <span data-ttu-id="68f5b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="68f5b-147">System.String</span></span>

### <span data-ttu-id="68f5b-148">System. Nullable "1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="68f5b-148">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="68f5b-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68f5b-149">OUTPUTS</span></span>

### <span data-ttu-id="68f5b-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="68f5b-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="68f5b-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68f5b-151">NOTES</span></span>

## <span data-ttu-id="68f5b-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68f5b-152">RELATED LINKS</span></span>

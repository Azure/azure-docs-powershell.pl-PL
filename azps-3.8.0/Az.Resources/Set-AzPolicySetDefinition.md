---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: 8a8559058b0bb5e1b33d93451bed35182a44783b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050700"
---
# <span data-ttu-id="b79e8-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b79e8-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="b79e8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b79e8-102">SYNOPSIS</span></span>
<span data-ttu-id="b79e8-103">Modyfikowanie definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="b79e8-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="b79e8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b79e8-104">SYNTAX</span></span>

### <span data-ttu-id="b79e8-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b79e8-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b79e8-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b79e8-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b79e8-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b79e8-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b79e8-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b79e8-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b79e8-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b79e8-109">DESCRIPTION</span></span>
<span data-ttu-id="b79e8-110">Polecenie cmdlet **Set-AzPolicySetDefinition** modyfikuje definicję zasad.</span><span class="sxs-lookup"><span data-stu-id="b79e8-110">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="b79e8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b79e8-111">EXAMPLES</span></span>

### <span data-ttu-id="b79e8-112">Przykład 1: aktualizowanie opisu definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="b79e8-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="b79e8-113">Pierwsze polecenie pobiera definicję zestawu zasad za pomocą polecenia cmdlet Get-AzPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="b79e8-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="b79e8-114">Polecenie zapisuje ten obiekt w zmiennej $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="b79e8-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="b79e8-115">Drugie polecenie aktualizuje opis definicji zestawu zasad określonego przez właściwość **ResourceId** $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="b79e8-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="b79e8-116">Przykład 2: aktualizowanie metadanych definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="b79e8-116">Example 2: Update the metadata of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}'


Name                  : VMPolicySetDefinition
ResourceId            : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
ResourceName          : VMPolicySetDefinition
ResourceType          : Microsoft.Authorization/policySetDefinitions
SubscriptionId        : 11111111-1111-1111-1111-111111111111
Properties            : @{displayName=VMPolicySetDefinition; policyType=Custom; metadata=; parameters=; policyDefinitions=System.Object[]}
PolicySetDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
```

<span data-ttu-id="b79e8-117">To polecenie powoduje zaktualizowanie metadanych definicji zestawu zasad o nazwie VMPolicySetDefinition w celu wskazania jej kategorii "maszyna wirtualna".</span><span class="sxs-lookup"><span data-stu-id="b79e8-117">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="b79e8-118">Przykład 3: aktualizowanie grup definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="b79e8-118">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="b79e8-119">To polecenie aktualizuje grupy definicji zestawu zasad o nazwie VMPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="b79e8-119">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="b79e8-120">Przykład 4: aktualizowanie grup definicji zestawu zasad przy użyciu tabeli skrótów</span><span class="sxs-lookup"><span data-stu-id="b79e8-120">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="b79e8-121">To polecenie aktualizuje grupy definicji zestawu zasad o nazwie VMPolicySetDefinition przy użyciu tablicy skrótów do konstruowania grup.</span><span class="sxs-lookup"><span data-stu-id="b79e8-121">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="b79e8-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b79e8-122">PARAMETERS</span></span>

### <span data-ttu-id="b79e8-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b79e8-123">-ApiVersion</span></span>
<span data-ttu-id="b79e8-124">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="b79e8-124">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b79e8-125">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="b79e8-125">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b79e8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b79e8-126">-DefaultProfile</span></span>
<span data-ttu-id="b79e8-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b79e8-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b79e8-128">— Opis</span><span class="sxs-lookup"><span data-stu-id="b79e8-128">-Description</span></span>
<span data-ttu-id="b79e8-129">Opis definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="b79e8-129">The description for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b79e8-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b79e8-130">-DisplayName</span></span>
<span data-ttu-id="b79e8-131">Nazwa wyświetlana definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="b79e8-131">The display name for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b79e8-132">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="b79e8-132">-GroupDefinition</span></span>
<span data-ttu-id="b79e8-133">Grupy definicji zasad zaktualizowanej definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="b79e8-133">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="b79e8-134">Może to być ścieżka do pliku zawierającego grupy lub grupy jako ciąg JSON.</span><span class="sxs-lookup"><span data-stu-id="b79e8-134">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b79e8-135">-ID</span><span class="sxs-lookup"><span data-stu-id="b79e8-135">-Id</span></span>
<span data-ttu-id="b79e8-136">Identyfikator definicji zasad w pełni kwalifikowany, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="b79e8-136">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="b79e8-137">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="b79e8-137">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="b79e8-138">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="b79e8-138">-ManagementGroupName</span></span>
<span data-ttu-id="b79e8-139">Nazwa grupy zarządzania definicji zestawu zasad do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="b79e8-139">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="b79e8-140">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b79e8-140">-Metadata</span></span>
<span data-ttu-id="b79e8-141">Metadane zaktualizowanej definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="b79e8-141">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="b79e8-142">Może to być ścieżka do nazwy pliku zawierającego metadane lub metadane jako ciąg JSON.</span><span class="sxs-lookup"><span data-stu-id="b79e8-142">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b79e8-143">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b79e8-143">-Name</span></span>
<span data-ttu-id="b79e8-144">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="b79e8-144">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b79e8-145">-Parameter</span><span class="sxs-lookup"><span data-stu-id="b79e8-145">-Parameter</span></span>
<span data-ttu-id="b79e8-146">Deklaracja parametrów zaktualizowanej definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="b79e8-146">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="b79e8-147">Może to być ścieżka do nazwy pliku lub identyfikatora URI zawierającego deklarację Parameters lub deklaracji Parameters jako ciągu JSON.</span><span class="sxs-lookup"><span data-stu-id="b79e8-147">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b79e8-148">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b79e8-148">-PolicyDefinition</span></span>
<span data-ttu-id="b79e8-149">Definicje zasad.</span><span class="sxs-lookup"><span data-stu-id="b79e8-149">The policy definitions.</span></span> <span data-ttu-id="b79e8-150">Może to być ścieżka do nazwy pliku zawierającego definicje zasad lub definicje zasad jako ciąg JSON.</span><span class="sxs-lookup"><span data-stu-id="b79e8-150">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b79e8-151">-Pre</span><span class="sxs-lookup"><span data-stu-id="b79e8-151">-Pre</span></span>
<span data-ttu-id="b79e8-152">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="b79e8-152">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b79e8-153">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b79e8-153">-SubscriptionId</span></span>
<span data-ttu-id="b79e8-154">Identyfikator subskrypcji definicji zestawu zasad do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="b79e8-154">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="b79e8-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b79e8-155">-Confirm</span></span>
<span data-ttu-id="b79e8-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b79e8-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b79e8-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b79e8-157">-WhatIf</span></span>
<span data-ttu-id="b79e8-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b79e8-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b79e8-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b79e8-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b79e8-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b79e8-160">CommonParameters</span></span>
<span data-ttu-id="b79e8-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b79e8-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b79e8-162">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b79e8-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b79e8-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b79e8-163">INPUTS</span></span>

### <span data-ttu-id="b79e8-164">System. String</span><span class="sxs-lookup"><span data-stu-id="b79e8-164">System.String</span></span>

### <span data-ttu-id="b79e8-165">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b79e8-165">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b79e8-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b79e8-166">OUTPUTS</span></span>

### <span data-ttu-id="b79e8-167">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b79e8-167">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b79e8-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b79e8-168">NOTES</span></span>

## <span data-ttu-id="b79e8-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b79e8-169">RELATED LINKS</span></span>

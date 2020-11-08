---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: 1a4a2579b05c60133fa1b0f7ab057be602965eaa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220388"
---
# <span data-ttu-id="38b16-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="38b16-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="38b16-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38b16-102">SYNOPSIS</span></span>
<span data-ttu-id="38b16-103">Tworzy definicję zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="38b16-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="38b16-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38b16-104">SYNTAX</span></span>

### <span data-ttu-id="38b16-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="38b16-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38b16-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="38b16-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38b16-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38b16-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38b16-108">Opis</span><span class="sxs-lookup"><span data-stu-id="38b16-108">DESCRIPTION</span></span>
<span data-ttu-id="38b16-109">Polecenie cmdlet **New-AzPolicySetDefinition** umożliwia utworzenie definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="38b16-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="38b16-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38b16-110">EXAMPLES</span></span>

### <span data-ttu-id="38b16-111">Przykład 1: Tworzenie definicji zestawu zasad za pomocą metadanych przy użyciu pliku zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="38b16-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "Finance"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="38b16-112">To polecenie tworzy definicję zestawu zasad o nazwie VMPolicySetDefinition z metadanymi wskazującymi jego kategorię "maszyna wirtualna", która zawiera definicje zasad określone w C:\VMPolicy.json.</span><span class="sxs-lookup"><span data-stu-id="38b16-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="38b16-113">Przykładowa zawartość VMPolicy.jsjest podana powyżej.</span><span class="sxs-lookup"><span data-stu-id="38b16-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="38b16-114">Przykład 2: Tworzenie definicji zestawu zasad sparametryzowanych</span><span class="sxs-lookup"><span data-stu-id="38b16-114">Example 2: Create a parameterized policy set definition</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "[parameters('buTagValue')]"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="38b16-115">To polecenie tworzy definicję zestawu zasad sparametryzowanego o nazwie VMPolicySetDefinition zawierającą definicje zasad określone w C:\VMPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="38b16-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="38b16-116">Przykładowa zawartość VMPolicy.jsjest podana powyżej.</span><span class="sxs-lookup"><span data-stu-id="38b16-116">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="38b16-117">Przykład 3: Tworzenie definicji zestawu zasad przy użyciu grup definicji zasad</span><span class="sxs-lookup"><span data-stu-id="38b16-117">Example 3: Create a policy set definition with policy definition groups</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "groupNames": [ "group1" ]
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf",
      "groupNames": [ "group2" ]
   }
]
```

```
$groupsJson = ConvertTo-Json @{ name = "group1" }, @{ name = "group2" }
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="38b16-118">To polecenie tworzy definicję zestawu zasad o nazwie VMPolicySetDefinition z zasadami grupowania definicji zasad określonymi w C:\VMPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="38b16-118">This command creates a policy set definition named VMPolicySetDefinition with grouping of policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="38b16-119">Przykładowa zawartość VMPolicy.jsjest podana powyżej.</span><span class="sxs-lookup"><span data-stu-id="38b16-119">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="38b16-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38b16-120">PARAMETERS</span></span>

### <span data-ttu-id="38b16-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="38b16-121">-ApiVersion</span></span>
<span data-ttu-id="38b16-122">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="38b16-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="38b16-123">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="38b16-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="38b16-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b16-124">-DefaultProfile</span></span>
<span data-ttu-id="38b16-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="38b16-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38b16-126">— Opis</span><span class="sxs-lookup"><span data-stu-id="38b16-126">-Description</span></span>
<span data-ttu-id="38b16-127">Opis definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="38b16-127">The description for policy set definition.</span></span>

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

### <span data-ttu-id="38b16-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="38b16-128">-DisplayName</span></span>
<span data-ttu-id="38b16-129">Nazwa wyświetlana definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="38b16-129">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="38b16-130">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="38b16-130">-GroupDefinition</span></span>
<span data-ttu-id="38b16-131">Grupy definicji zasad dla nowej definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="38b16-131">The policy definition groups for the new policy set definition.</span></span> <span data-ttu-id="38b16-132">Może to być ścieżka do pliku zawierającego grupy lub grupy jako ciąg JSON.</span><span class="sxs-lookup"><span data-stu-id="38b16-132">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="38b16-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="38b16-133">-ManagementGroupName</span></span>
<span data-ttu-id="38b16-134">Nazwa grupy zarządzania nowej definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="38b16-134">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="38b16-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="38b16-135">-Metadata</span></span>
<span data-ttu-id="38b16-136">Metadane dotyczące definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="38b16-136">The metadata for policy set definition.</span></span> <span data-ttu-id="38b16-137">Może to być ścieżka do nazwy pliku zawierającego metadane lub metadane jako ciąg JSON.</span><span class="sxs-lookup"><span data-stu-id="38b16-137">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="38b16-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="38b16-138">-Name</span></span>
<span data-ttu-id="38b16-139">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="38b16-139">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b16-140">-Parameter</span><span class="sxs-lookup"><span data-stu-id="38b16-140">-Parameter</span></span>
<span data-ttu-id="38b16-141">Deklaracja Parameters dla definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="38b16-141">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="38b16-142">Może to być ścieżka do nazwy pliku zawierającej deklarację Parameters lub deklaracji Parameters jako ciągu JSON.</span><span class="sxs-lookup"><span data-stu-id="38b16-142">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="38b16-143">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="38b16-143">-PolicyDefinition</span></span>
<span data-ttu-id="38b16-144">Definicje zasad.</span><span class="sxs-lookup"><span data-stu-id="38b16-144">The policy definitions.</span></span> <span data-ttu-id="38b16-145">Może to być ścieżka do nazwy pliku zawierającego definicje zasad lub definicje zasad jako ciąg JSON.</span><span class="sxs-lookup"><span data-stu-id="38b16-145">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b16-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="38b16-146">-Pre</span></span>
<span data-ttu-id="38b16-147">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="38b16-147">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="38b16-148">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="38b16-148">-SubscriptionId</span></span>
<span data-ttu-id="38b16-149">Identyfikator subskrypcji nowej definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="38b16-149">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="38b16-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="38b16-150">-Confirm</span></span>
<span data-ttu-id="38b16-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38b16-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38b16-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38b16-152">-WhatIf</span></span>
<span data-ttu-id="38b16-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38b16-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38b16-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="38b16-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38b16-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b16-155">CommonParameters</span></span>
<span data-ttu-id="38b16-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38b16-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b16-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38b16-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b16-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38b16-158">INPUTS</span></span>

### <span data-ttu-id="38b16-159">System. String</span><span class="sxs-lookup"><span data-stu-id="38b16-159">System.String</span></span>

### <span data-ttu-id="38b16-160">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="38b16-160">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="38b16-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38b16-161">OUTPUTS</span></span>

### <span data-ttu-id="38b16-162">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="38b16-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="38b16-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38b16-163">NOTES</span></span>

## <span data-ttu-id="38b16-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38b16-164">RELATED LINKS</span></span>

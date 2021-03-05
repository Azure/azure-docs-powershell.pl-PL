---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: ae1cc96cd617ec74a69fc2c95ec50973e688ebe9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995226"
---
# <span data-ttu-id="6789c-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="6789c-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="6789c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6789c-102">SYNOPSIS</span></span>
<span data-ttu-id="6789c-103">Tworzy definicję zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="6789c-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="6789c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6789c-104">SYNTAX</span></span>

### <span data-ttu-id="6789c-105">NameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6789c-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6789c-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6789c-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6789c-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6789c-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6789c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6789c-108">DESCRIPTION</span></span>
<span data-ttu-id="6789c-109">Polecenie **cmdlet New-AzPolicySetDefinition** tworzy definicję zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="6789c-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="6789c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6789c-110">EXAMPLES</span></span>

### <span data-ttu-id="6789c-111">Przykład 1. Tworzenie definicji zestawu zasad z metadanymi przy użyciu pliku zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="6789c-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
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

<span data-ttu-id="6789c-112">To polecenie tworzy definicję zestawu zasad o nazwie VIRTUALPolicySetDefinition z metadanymi wskazującymi, że jej kategoria to "Maszyny wirtualne", która zawiera definicje zasad określone w C:\VMPolicy.jsna.</span><span class="sxs-lookup"><span data-stu-id="6789c-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="6789c-113">Przykładowa zawartość VMPolicy.jsjest podany powyżej.</span><span class="sxs-lookup"><span data-stu-id="6789c-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="6789c-114">Przykład 2. Tworzenie definicji zestawu parametrów zasad</span><span class="sxs-lookup"><span data-stu-id="6789c-114">Example 2: Create a parameterized policy set definition</span></span>
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

<span data-ttu-id="6789c-115">To polecenie tworzy parametryzowane definicje zestawu zasad o nazwie VMPolicySetDefinition, która zawiera definicje zasad określone w C:\VMPolicy.jszasad.</span><span class="sxs-lookup"><span data-stu-id="6789c-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="6789c-116">Przykładowa zawartość VMPolicy.jsjest podany powyżej.</span><span class="sxs-lookup"><span data-stu-id="6789c-116">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="6789c-117">Przykład 3. Tworzenie definicji zestawu zasad za pomocą grup definicji zasad</span><span class="sxs-lookup"><span data-stu-id="6789c-117">Example 3: Create a policy set definition with policy definition groups</span></span>
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

<span data-ttu-id="6789c-118">To polecenie tworzy definicję zestawu zasad o nazwie VMPolicySetDefinition z grupowanie definicji zasad określonych w C:\VMPolicy.jszasad.</span><span class="sxs-lookup"><span data-stu-id="6789c-118">This command creates a policy set definition named VMPolicySetDefinition with grouping of policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="6789c-119">Przykładowa zawartość VMPolicy.jsjest podany powyżej.</span><span class="sxs-lookup"><span data-stu-id="6789c-119">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="6789c-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6789c-120">PARAMETERS</span></span>

### <span data-ttu-id="6789c-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6789c-121">-ApiVersion</span></span>
<span data-ttu-id="6789c-122">Po jego skonfigurowaniu wskazuje wersję interfejsu API dostawcy zasobów, która ma być dostępna.</span><span class="sxs-lookup"><span data-stu-id="6789c-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="6789c-123">Jeśli nie zostanie określona, wersja interfejsu API jest automatycznie określana jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="6789c-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="6789c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6789c-124">-DefaultProfile</span></span>
<span data-ttu-id="6789c-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="6789c-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6789c-126">— Opis</span><span class="sxs-lookup"><span data-stu-id="6789c-126">-Description</span></span>
<span data-ttu-id="6789c-127">Opis definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="6789c-127">The description for policy set definition.</span></span>

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

### <span data-ttu-id="6789c-128">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="6789c-128">-DisplayName</span></span>
<span data-ttu-id="6789c-129">Nazwa wyświetlana definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="6789c-129">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="6789c-130">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="6789c-130">-GroupDefinition</span></span>
<span data-ttu-id="6789c-131">Grupy definicji zasad dla nowej definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="6789c-131">The policy definition groups for the new policy set definition.</span></span> <span data-ttu-id="6789c-132">Może to być ścieżka do pliku zawierającego grupy lub grupy w postaci ciągu JSON.</span><span class="sxs-lookup"><span data-stu-id="6789c-132">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="6789c-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="6789c-133">-ManagementGroupName</span></span>
<span data-ttu-id="6789c-134">Nazwa grupy zarządzania nowej definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="6789c-134">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="6789c-135">— Metadane</span><span class="sxs-lookup"><span data-stu-id="6789c-135">-Metadata</span></span>
<span data-ttu-id="6789c-136">Metadane dla definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="6789c-136">The metadata for policy set definition.</span></span> <span data-ttu-id="6789c-137">Może to być ścieżka do nazwy pliku zawierającej metadane lub metadane jako ciąg JSON.</span><span class="sxs-lookup"><span data-stu-id="6789c-137">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="6789c-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6789c-138">-Name</span></span>
<span data-ttu-id="6789c-139">Nazwa definicji ustawiona przez zasady.</span><span class="sxs-lookup"><span data-stu-id="6789c-139">The policy set definition name.</span></span>

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

### <span data-ttu-id="6789c-140">- Parametr</span><span class="sxs-lookup"><span data-stu-id="6789c-140">-Parameter</span></span>
<span data-ttu-id="6789c-141">Deklaracja parametrów dla definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="6789c-141">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="6789c-142">Może to być ścieżka do nazwy pliku zawierającej deklarację parametrów lub deklaracja parametrów jako ciąg JSON.</span><span class="sxs-lookup"><span data-stu-id="6789c-142">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="6789c-143">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6789c-143">-PolicyDefinition</span></span>
<span data-ttu-id="6789c-144">Definicje zasad.</span><span class="sxs-lookup"><span data-stu-id="6789c-144">The policy definitions.</span></span> <span data-ttu-id="6789c-145">Może to być ścieżka do nazwy pliku zawierającej definicje zasad lub definicje zasad jako ciąg JSON.</span><span class="sxs-lookup"><span data-stu-id="6789c-145">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="6789c-146">— Przed</span><span class="sxs-lookup"><span data-stu-id="6789c-146">-Pre</span></span>
<span data-ttu-id="6789c-147">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="6789c-147">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6789c-148">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6789c-148">-SubscriptionId</span></span>
<span data-ttu-id="6789c-149">Identyfikator subskrypcji definicji nowego zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="6789c-149">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="6789c-150">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6789c-150">-Confirm</span></span>
<span data-ttu-id="6789c-151">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6789c-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6789c-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6789c-152">-WhatIf</span></span>
<span data-ttu-id="6789c-153">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6789c-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6789c-154">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6789c-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6789c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6789c-155">CommonParameters</span></span>
<span data-ttu-id="6789c-156">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6789c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6789c-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6789c-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6789c-158">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6789c-158">INPUTS</span></span>

### <span data-ttu-id="6789c-159">System.String</span><span class="sxs-lookup"><span data-stu-id="6789c-159">System.String</span></span>

### <span data-ttu-id="6789c-160">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6789c-160">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6789c-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6789c-161">OUTPUTS</span></span>

### <span data-ttu-id="6789c-162">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="6789c-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6789c-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6789c-163">NOTES</span></span>

## <span data-ttu-id="6789c-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6789c-164">RELATED LINKS</span></span>

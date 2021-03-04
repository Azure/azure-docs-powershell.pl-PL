---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/new-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
ms.openlocfilehash: 82d0d3667371485d079785dbdb2f87eb8284aa94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954858"
---
# <span data-ttu-id="c9e6d-101">New-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="c9e6d-101">New-AzBlueprintArtifact</span></span>

## <span data-ttu-id="c9e6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="c9e6d-103">Utwórz nowy artefakt i zapisz go w definicji planu.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-103">Create a new artifact and save it within a blueprint definition.</span></span>

## <span data-ttu-id="c9e6d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c9e6d-104">SYNTAX</span></span>

### <span data-ttu-id="c9e6d-105">CreateTemplateArtifact (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c9e6d-105">CreateTemplateArtifact (Default)</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9e6d-106">CreateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="c9e6d-106">CreateArtifactByInputFile</span></span>
```
New-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9e6d-107">CreateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="c9e6d-107">CreateRoleAssignmentArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9e6d-108">CreatePolicyArtifact</span><span class="sxs-lookup"><span data-stu-id="c9e6d-108">CreatePolicyArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9e6d-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="c9e6d-109">DESCRIPTION</span></span>
<span data-ttu-id="c9e6d-110">Utwórz nowy artefakt.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-110">Create a new artifact.</span></span> <span data-ttu-id="c9e6d-111">Istnieją dwa sposoby tworzenia artefaktu: za pomocą artefaktu JSON jako pliku wejściowego lub przez podanie parametrów w tekście tego artefaktu.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-111">There are two ways to create an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="c9e6d-112">Mimo że metoda JSON nie wymaga podania typu artefaktu w metody parametru wbudowanej, użytkownik musi podać typ artefaktu za pomocą parametru -Type.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="c9e6d-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c9e6d-113">EXAMPLES</span></span>

### <span data-ttu-id="c9e6d-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c9e6d-114">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Name PolicyStorage -Blueprint $bp -ArtifactFile C:\PolicyAssignmentStorageTag.json

DisplayName        :
Description        : Apply storage tag and the parameter also used by the template to resource groups
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/PolicyAssignmentStorageTag
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : PolicyAssignmentStorageTag
```

<span data-ttu-id="c9e6d-115">Utwórz nowy artefakt za pomocą pliku JSON artefaktu.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-115">Create a new artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="c9e6d-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c9e6d-116">Example 2</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type PolicyAssignmentArtifact -Name "ApplyTag-RG" -Blueprint $bp -PolicyDefinitionId "/providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71" -PolicyDefinitionParameter @{tagName="[parameters('tagName')]"; tagValue="[parameters('tagValue')]"} -ResourceGroupName storageRG

DisplayName        : ApplyTag-RG
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagName,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : storageRG
Id                 : /subscriptions/28cbf98f-381d-4425-9ac4-cf342dab9753/providers/Microsoft.Blueprint/blueprints/AppNetwork/
                     artifacts/ApplyTag-RG
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : ApplyTag-RG
```

<span data-ttu-id="c9e6d-117">Tworzenie nowego artefaktu przy użyciu parametrów w tekście.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-117">Create a new artifact through inline parameters.</span></span>

### <span data-ttu-id="c9e6d-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c9e6d-118">Example 3</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type TemplateArtifact -Name storage-account -Blueprint $bp -TemplateFile C:\StorageAccountArmTemplate.json -ResourceGroup "storageRG" -TemplateParameterFile C:\Workspace\BlueprintTemplates\RestTemplatesSomeInline\StorageAccountParameters.json

DisplayName   : storage-account
Description   :
DependsOn     :
Template      : {$schema, contentVersion, parameters, variables...}
Parameters    : {}
ResourceGroup : storageRG
Id            : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/storage-account
Type          : Microsoft.Blueprint/blueprints/artifacts
Name          : storage-account
```

<span data-ttu-id="c9e6d-119">Utwórz nowy artefakt za pomocą pliku ARM szablonu.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-119">Create a new artifact through an ARM template file.</span></span>

## <span data-ttu-id="c9e6d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9e6d-120">PARAMETERS</span></span>

### <span data-ttu-id="c9e6d-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="c9e6d-121">-ArtifactFile</span></span>
<span data-ttu-id="c9e6d-122">Lokalizacja pliku artefaktu w formacie JSON na dysku.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e6d-123">—Plan</span><span class="sxs-lookup"><span data-stu-id="c9e6d-123">-Blueprint</span></span>
<span data-ttu-id="c9e6d-124">Obiekt planu.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-124">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e6d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9e6d-125">-DefaultProfile</span></span>
<span data-ttu-id="c9e6d-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9e6d-127">- DependsOn</span><span class="sxs-lookup"><span data-stu-id="c9e6d-127">-DependsOn</span></span>
<span data-ttu-id="c9e6d-128">Lista nazw artefaktów, które muszą zostać utworzone przed utworzeniem bieżącego artefaktu.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e6d-129">— Opis</span><span class="sxs-lookup"><span data-stu-id="c9e6d-129">-Description</span></span>
<span data-ttu-id="c9e6d-130">Opis artefaktu.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-130">Description of the artifact.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e6d-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c9e6d-131">-Name</span></span>
<span data-ttu-id="c9e6d-132">Nazwa artefaktu</span><span class="sxs-lookup"><span data-stu-id="c9e6d-132">Name of the artifact</span></span>

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

### <span data-ttu-id="c9e6d-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="c9e6d-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="c9e6d-134">Identyfikator definicji definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-134">Definition Id of the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e6d-135">-PolicyDefinitionParameters</span><span class="sxs-lookup"><span data-stu-id="c9e6d-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="c9e6d-136">Hashtable of parameters to pass to the policy definition artifact.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e6d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9e6d-137">-ResourceGroupName</span></span>
<span data-ttu-id="c9e6d-138">Nazwa grupy zasobów, pod która ma się znaleźć artefakt.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e6d-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="c9e6d-139">-RoleDefinitionId</span></span>
<span data-ttu-id="c9e6d-140">Lista definicji roli</span><span class="sxs-lookup"><span data-stu-id="c9e6d-140">List of role definition</span></span>

```yaml
Type: System.String
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e6d-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="c9e6d-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="c9e6d-142">Lista identyfikatorów głównych definicji ról.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-142">List of role definition principal ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e6d-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="c9e6d-143">-TemplateFile</span></span>
<span data-ttu-id="c9e6d-144">Lokalizacja pliku szablonu ARM na dysku.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e6d-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="c9e6d-145">-TemplateParameterFile</span></span>
<span data-ttu-id="c9e6d-146">Lokalizacja pliku ARM na dysku.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e6d-147">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="c9e6d-147">-Type</span></span>
<span data-ttu-id="c9e6d-148">Typ artefaktu.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-148">Type of the artifact.</span></span>
<span data-ttu-id="c9e6d-149">Obsługiwane są 3 typy: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e6d-150">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9e6d-150">-Confirm</span></span>
<span data-ttu-id="c9e6d-151">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9e6d-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9e6d-152">-WhatIf</span></span>
<span data-ttu-id="c9e6d-153">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9e6d-154">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9e6d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9e6d-155">CommonParameters</span></span>
<span data-ttu-id="c9e6d-156">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9e6d-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9e6d-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9e6d-158">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9e6d-158">INPUTS</span></span>

### <span data-ttu-id="c9e6d-159">System.String</span><span class="sxs-lookup"><span data-stu-id="c9e6d-159">System.String</span></span>

### <span data-ttu-id="c9e6d-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="c9e6d-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="c9e6d-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="c9e6d-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="c9e6d-162">System.Collections.Generic.List'1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c9e6d-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="c9e6d-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c9e6d-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c9e6d-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c9e6d-164">System.String[]</span></span>

## <span data-ttu-id="c9e6d-165">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9e6d-165">OUTPUTS</span></span>

### <span data-ttu-id="c9e6d-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span><span class="sxs-lookup"><span data-stu-id="c9e6d-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="c9e6d-167">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c9e6d-167">NOTES</span></span>

## <span data-ttu-id="c9e6d-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9e6d-168">RELATED LINKS</span></span>

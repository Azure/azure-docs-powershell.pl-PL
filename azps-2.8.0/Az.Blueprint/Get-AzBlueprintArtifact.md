---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: 94a0ff1d4e16748b769f51303fb397da7e029026
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706614"
---
# <span data-ttu-id="6079f-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="6079f-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="6079f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6079f-102">SYNOPSIS</span></span>
<span data-ttu-id="6079f-103">Pobieranie artefaktów z definicji planów.</span><span class="sxs-lookup"><span data-stu-id="6079f-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="6079f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6079f-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6079f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6079f-105">DESCRIPTION</span></span>
<span data-ttu-id="6079f-106">Pobieranie artefaktów z definicji planów.</span><span class="sxs-lookup"><span data-stu-id="6079f-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="6079f-107">Jeśli nie podano wersji definicji plany, zostanie pobrana wersja robocza.</span><span class="sxs-lookup"><span data-stu-id="6079f-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="6079f-108">W przypadku braku wersji roboczej jest zwracana Najnowsza opublikowana definicja.</span><span class="sxs-lookup"><span data-stu-id="6079f-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="6079f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6079f-109">EXAMPLES</span></span>

### <span data-ttu-id="6079f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6079f-110">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Get-AzBlueprintArtifact -Blueprint $bp 

DisplayName        : Audit use of classic virtual machines
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1d84d5fb-01f6-4d12-ba4f-4a26081d403d
Parameters         : {[effect, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : SimpleBlueprintRG
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/3ab44511-0228-4275-9641-7e93e6f34178
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 3ab44511-0228-4275-9641-7e93e6f34178

DisplayName        : Enforce tag and its value
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1e30110a-5ceb-460c-a204-c1c3969c6d62
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/0e1593da-47d5-4b75-800c-9a797dd23192
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 0e1593da-47d5-4b75-800c-9a797dd23192

```

<span data-ttu-id="6079f-111">Pobieranie artefaktów z definicji planów.</span><span class="sxs-lookup"><span data-stu-id="6079f-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="6079f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6079f-112">PARAMETERS</span></span>

### <span data-ttu-id="6079f-113">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="6079f-113">-ArtifactFile</span></span>
<span data-ttu-id="6079f-114">Lokalizacja pliku artefaktu w formacie JSON na dysku.</span><span class="sxs-lookup"><span data-stu-id="6079f-114">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6079f-115">-Plan</span><span class="sxs-lookup"><span data-stu-id="6079f-115">-Blueprint</span></span>
<span data-ttu-id="6079f-116">Obiekt plan.</span><span class="sxs-lookup"><span data-stu-id="6079f-116">Blueprint object.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: ArtifactsByBlueprint, UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSBlueprintBase
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6079f-117">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="6079f-117">-BlueprintVersion</span></span>
<span data-ttu-id="6079f-118">Wersja programu plan, z którego mają być pozyskane artefakty.</span><span class="sxs-lookup"><span data-stu-id="6079f-118">Version of the blueprint to get the artifacts from.</span></span>

```yaml
Type: String
Parameter Sets: ArtifactsByBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6079f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6079f-119">-DefaultProfile</span></span>
<span data-ttu-id="6079f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6079f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6079f-121">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="6079f-121">-DependsOn</span></span>
<span data-ttu-id="6079f-122">Lista nazw artefaktów, które należy utworzyć przed utworzeniem bieżącego artefaktu.</span><span class="sxs-lookup"><span data-stu-id="6079f-122">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6079f-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="6079f-123">-Description</span></span>
<span data-ttu-id="6079f-124">Opis artefaktu.</span><span class="sxs-lookup"><span data-stu-id="6079f-124">Description of the artifact.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6079f-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6079f-125">-Name</span></span>
<span data-ttu-id="6079f-126">Imię i nazwisko artefaktu</span><span class="sxs-lookup"><span data-stu-id="6079f-126">Name of the artifact</span></span>

```yaml
Type: String
Parameter Sets: ArtifactsByBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: CreateArtifactByInputFile, UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6079f-127">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="6079f-127">-PolicyDefinitionId</span></span>
<span data-ttu-id="6079f-128">Identyfikator definicji definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="6079f-128">Definition Id of the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6079f-129">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="6079f-129">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="6079f-130">Obiekt Hashtable parametrów do przekazania do artefaktu definicji zasad.</span><span class="sxs-lookup"><span data-stu-id="6079f-130">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6079f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6079f-131">-ResourceGroupName</span></span>
<span data-ttu-id="6079f-132">Nazwa grupy zasobów, w której ma się pojawić artefakt.</span><span class="sxs-lookup"><span data-stu-id="6079f-132">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6079f-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="6079f-133">-RoleDefinitionId</span></span>
<span data-ttu-id="6079f-134">Lista definicji ról</span><span class="sxs-lookup"><span data-stu-id="6079f-134">List of role definition</span></span>

```yaml
Type: String
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6079f-135">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="6079f-135">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="6079f-136">Lista identyfikatorów głównych definicji ról.</span><span class="sxs-lookup"><span data-stu-id="6079f-136">List of role definition principal ids.</span></span>

```yaml
Type: String[]
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6079f-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="6079f-137">-TemplateFile</span></span>
<span data-ttu-id="6079f-138">Lokalizacja pliku szablonu ARM na dysku.</span><span class="sxs-lookup"><span data-stu-id="6079f-138">Location of the ARM template file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6079f-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="6079f-139">-TemplateParameterFile</span></span>
<span data-ttu-id="6079f-140">Lokalizacja pliku parametrów szablonu ARM na dysku.</span><span class="sxs-lookup"><span data-stu-id="6079f-140">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6079f-141">-Type</span><span class="sxs-lookup"><span data-stu-id="6079f-141">-Type</span></span>
<span data-ttu-id="6079f-142">Typ artefaktu.</span><span class="sxs-lookup"><span data-stu-id="6079f-142">Type of the artifact.</span></span>
<span data-ttu-id="6079f-143">Obsługiwane są 3 typy: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="6079f-143">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: PSArtifactKind
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6079f-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6079f-144">-Confirm</span></span>
<span data-ttu-id="6079f-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6079f-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6079f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6079f-146">-WhatIf</span></span>
<span data-ttu-id="6079f-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6079f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6079f-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6079f-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6079f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6079f-149">CommonParameters</span></span>
<span data-ttu-id="6079f-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6079f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6079f-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6079f-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6079f-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6079f-152">INPUTS</span></span>

### <span data-ttu-id="6079f-153">System. String</span><span class="sxs-lookup"><span data-stu-id="6079f-153">System.String</span></span>

### <span data-ttu-id="6079f-154">Microsoft. Azure. Commands. plan. modele. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="6079f-154">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="6079f-155">Microsoft. Azure. Commands. plan. modele. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="6079f-155">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="6079f-156">System. Collections. Generic. list "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6079f-156">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="6079f-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6079f-157">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6079f-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="6079f-158">System.String[]</span></span>

## <span data-ttu-id="6079f-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6079f-159">OUTPUTS</span></span>

### <span data-ttu-id="6079f-160">Microsoft. Azure. Commands. plan. modele. PSBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="6079f-160">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="6079f-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6079f-161">NOTES</span></span>

## <span data-ttu-id="6079f-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6079f-162">RELATED LINKS</span></span>

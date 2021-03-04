---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: d64f77bc8662ec4d03619333beaa124eaf90e309
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959706"
---
# <span data-ttu-id="492bb-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="492bb-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="492bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="492bb-102">SYNOPSIS</span></span>
<span data-ttu-id="492bb-103">Pobieranie artefaktów z definicji planu.</span><span class="sxs-lookup"><span data-stu-id="492bb-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="492bb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="492bb-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="492bb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="492bb-105">DESCRIPTION</span></span>
<span data-ttu-id="492bb-106">Pobieranie artefaktów z definicji planu.</span><span class="sxs-lookup"><span data-stu-id="492bb-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="492bb-107">Jeśli wersja definicji planu nie jest określona, jest pobierana wersja robocza.</span><span class="sxs-lookup"><span data-stu-id="492bb-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="492bb-108">W przypadku, gdy nie ma wersji roboczej, jest zwracana najnowsza opublikowana definicja planu.</span><span class="sxs-lookup"><span data-stu-id="492bb-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="492bb-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="492bb-109">EXAMPLES</span></span>

### <span data-ttu-id="492bb-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="492bb-110">Example 1</span></span>
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

<span data-ttu-id="492bb-111">Pobieranie artefaktów z definicji planu.</span><span class="sxs-lookup"><span data-stu-id="492bb-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="492bb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="492bb-112">PARAMETERS</span></span>

### <span data-ttu-id="492bb-113">—Plan</span><span class="sxs-lookup"><span data-stu-id="492bb-113">-Blueprint</span></span>
<span data-ttu-id="492bb-114">Obiekt planu.</span><span class="sxs-lookup"><span data-stu-id="492bb-114">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="492bb-115">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="492bb-115">-BlueprintVersion</span></span>
<span data-ttu-id="492bb-116">Wersja planu, z których mają pochodzić artefakty.</span><span class="sxs-lookup"><span data-stu-id="492bb-116">Version of the blueprint to get the artifacts from.</span></span>

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

### <span data-ttu-id="492bb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="492bb-117">-DefaultProfile</span></span>
<span data-ttu-id="492bb-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="492bb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="492bb-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="492bb-119">-Name</span></span>
<span data-ttu-id="492bb-120">Nazwa artefaktu</span><span class="sxs-lookup"><span data-stu-id="492bb-120">Name of the artifact</span></span>

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

### <span data-ttu-id="492bb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="492bb-121">CommonParameters</span></span>
<span data-ttu-id="492bb-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="492bb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="492bb-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="492bb-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="492bb-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="492bb-124">INPUTS</span></span>

### <span data-ttu-id="492bb-125">System.String</span><span class="sxs-lookup"><span data-stu-id="492bb-125">System.String</span></span>

### <span data-ttu-id="492bb-126">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="492bb-126">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="492bb-127">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="492bb-127">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="492bb-128">System.Collections.Generic.List'1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="492bb-128">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="492bb-129">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="492bb-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="492bb-130">System.String[]</span><span class="sxs-lookup"><span data-stu-id="492bb-130">System.String[]</span></span>

## <span data-ttu-id="492bb-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="492bb-131">OUTPUTS</span></span>

### <span data-ttu-id="492bb-132">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="492bb-132">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="492bb-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="492bb-133">NOTES</span></span>

## <span data-ttu-id="492bb-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="492bb-134">RELATED LINKS</span></span>

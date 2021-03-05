---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
ms.openlocfilehash: cd79d9315c6352b604a40269286073792596a41e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992139"
---
# <span data-ttu-id="9e77d-101">Set-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="9e77d-101">Set-AzSynapsePipeline</span></span>

## <span data-ttu-id="9e77d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e77d-102">SYNOPSIS</span></span>
<span data-ttu-id="9e77d-103">Tworzy potok w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="9e77d-103">Creates a pipeline in workspace.</span></span>

## <span data-ttu-id="9e77d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9e77d-104">SYNTAX</span></span>

### <span data-ttu-id="9e77d-105">SetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="9e77d-105">SetByName (Default)</span></span>
```
Set-AzSynapsePipeline -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e77d-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="9e77d-106">SetByObject</span></span>
```
Set-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e77d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9e77d-107">DESCRIPTION</span></span>
<span data-ttu-id="9e77d-108">Polecenie **cmdlet Set-AzSynapsePipeline** tworzy potok w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="9e77d-108">The **Set-AzSynapsePipeline** cmdlet creates a pipeline in workspace.</span></span>

## <span data-ttu-id="9e77d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9e77d-109">EXAMPLES</span></span>

### <span data-ttu-id="9e77d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9e77d-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="9e77d-111">To polecenie tworzy w obszarze roboczym potok o nazwie ContosoPipeline o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="9e77d-111">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="9e77d-112">Polecenie bazuje na informacjach w pliku pipeline.jsplikach.</span><span class="sxs-lookup"><span data-stu-id="9e77d-112">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="9e77d-113">Ten plik zawiera informacje o działaniach.</span><span class="sxs-lookup"><span data-stu-id="9e77d-113">This file includes information about activities.</span></span>

### <span data-ttu-id="9e77d-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9e77d-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapsePipeline -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="9e77d-115">To polecenie tworzy w obszarze roboczym potok o nazwie ContosoPipeline potok o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="9e77d-115">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>
<span data-ttu-id="9e77d-116">Polecenie bazuje na informacjach w pliku pipeline.jsplikach.</span><span class="sxs-lookup"><span data-stu-id="9e77d-116">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="9e77d-117">Ten plik zawiera informacje o działaniach.</span><span class="sxs-lookup"><span data-stu-id="9e77d-117">This file includes information about activities.</span></span>

## <span data-ttu-id="9e77d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e77d-118">PARAMETERS</span></span>

### <span data-ttu-id="9e77d-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9e77d-119">-AsJob</span></span>
<span data-ttu-id="9e77d-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9e77d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e77d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e77d-121">-DefaultProfile</span></span>
<span data-ttu-id="9e77d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e77d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e77d-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="9e77d-123">-DefinitionFile</span></span>
<span data-ttu-id="9e77d-124">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="9e77d-124">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e77d-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9e77d-125">-Name</span></span>
<span data-ttu-id="9e77d-126">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="9e77d-126">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e77d-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9e77d-127">-WorkspaceName</span></span>
<span data-ttu-id="9e77d-128">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="9e77d-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e77d-129">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9e77d-129">-WorkspaceObject</span></span>
<span data-ttu-id="9e77d-130">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="9e77d-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e77d-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9e77d-131">-Confirm</span></span>
<span data-ttu-id="9e77d-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9e77d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e77d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e77d-133">-WhatIf</span></span>
<span data-ttu-id="9e77d-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e77d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e77d-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9e77d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e77d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e77d-136">CommonParameters</span></span>
<span data-ttu-id="9e77d-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e77d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e77d-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e77d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e77d-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e77d-139">INPUTS</span></span>

### <span data-ttu-id="9e77d-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9e77d-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9e77d-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e77d-141">OUTPUTS</span></span>

### <span data-ttu-id="9e77d-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="9e77d-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="9e77d-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9e77d-143">NOTES</span></span>

## <span data-ttu-id="9e77d-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e77d-144">RELATED LINKS</span></span>

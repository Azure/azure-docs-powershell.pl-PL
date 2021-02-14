---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
ms.openlocfilehash: 2bce821f55b5f8ff39f56fa8a6960cb1f99b47d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188771"
---
# <span data-ttu-id="d6905-101">Set-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="d6905-101">Set-AzSynapsePipeline</span></span>

## <span data-ttu-id="d6905-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6905-102">SYNOPSIS</span></span>
<span data-ttu-id="d6905-103">Tworzy potok w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="d6905-103">Creates a pipeline in workspace.</span></span>

## <span data-ttu-id="d6905-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d6905-104">SYNTAX</span></span>

### <span data-ttu-id="d6905-105">SetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="d6905-105">SetByName (Default)</span></span>
```
Set-AzSynapsePipeline -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6905-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="d6905-106">SetByObject</span></span>
```
Set-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6905-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d6905-107">DESCRIPTION</span></span>
<span data-ttu-id="d6905-108">Polecenie **cmdlet Set-AzSynapsePipeline** tworzy potok w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="d6905-108">The **Set-AzSynapsePipeline** cmdlet creates a pipeline in workspace.</span></span>

## <span data-ttu-id="d6905-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d6905-109">EXAMPLES</span></span>

### <span data-ttu-id="d6905-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d6905-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="d6905-111">To polecenie tworzy w obszarze roboczym potok o nazwie ContosoPipeline o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d6905-111">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="d6905-112">Polecenie bazuje na informacjach w pliku pipeline.jsplikach.</span><span class="sxs-lookup"><span data-stu-id="d6905-112">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="d6905-113">Ten plik zawiera informacje o działaniach.</span><span class="sxs-lookup"><span data-stu-id="d6905-113">This file includes information about activities.</span></span>

### <span data-ttu-id="d6905-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d6905-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapsePipeline -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="d6905-115">To polecenie tworzy w obszarze roboczym potok o nazwie ContosoPipeline potok o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d6905-115">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>
<span data-ttu-id="d6905-116">Polecenie bazuje na informacjach z pipeline.jspliku.</span><span class="sxs-lookup"><span data-stu-id="d6905-116">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="d6905-117">Ten plik zawiera informacje o działaniach.</span><span class="sxs-lookup"><span data-stu-id="d6905-117">This file includes information about activities.</span></span>

## <span data-ttu-id="d6905-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6905-118">PARAMETERS</span></span>

### <span data-ttu-id="d6905-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d6905-119">-AsJob</span></span>
<span data-ttu-id="d6905-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d6905-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6905-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6905-121">-DefaultProfile</span></span>
<span data-ttu-id="d6905-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6905-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6905-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="d6905-123">-DefinitionFile</span></span>
<span data-ttu-id="d6905-124">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="d6905-124">The JSON file path.</span></span>

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

### <span data-ttu-id="d6905-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d6905-125">-Name</span></span>
<span data-ttu-id="d6905-126">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="d6905-126">The pipeline name.</span></span>

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

### <span data-ttu-id="d6905-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d6905-127">-WorkspaceName</span></span>
<span data-ttu-id="d6905-128">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="d6905-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d6905-129">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d6905-129">-WorkspaceObject</span></span>
<span data-ttu-id="d6905-130">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="d6905-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d6905-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d6905-131">-Confirm</span></span>
<span data-ttu-id="d6905-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d6905-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6905-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6905-133">-WhatIf</span></span>
<span data-ttu-id="d6905-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6905-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6905-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d6905-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6905-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6905-136">CommonParameters</span></span>
<span data-ttu-id="d6905-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6905-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6905-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6905-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6905-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6905-139">INPUTS</span></span>

### <span data-ttu-id="d6905-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d6905-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d6905-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d6905-141">OUTPUTS</span></span>

### <span data-ttu-id="d6905-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="d6905-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="d6905-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d6905-143">NOTES</span></span>

## <span data-ttu-id="d6905-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6905-144">RELATED LINKS</span></span>

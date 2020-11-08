---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
ms.openlocfilehash: 2bce821f55b5f8ff39f56fa8a6960cb1f99b47d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232375"
---
# <span data-ttu-id="8385f-101">Set-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="8385f-101">Set-AzSynapsePipeline</span></span>

## <span data-ttu-id="8385f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8385f-102">SYNOPSIS</span></span>
<span data-ttu-id="8385f-103">Tworzy potok w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="8385f-103">Creates a pipeline in workspace.</span></span>

## <span data-ttu-id="8385f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8385f-104">SYNTAX</span></span>

### <span data-ttu-id="8385f-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8385f-105">SetByName (Default)</span></span>
```
Set-AzSynapsePipeline -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8385f-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="8385f-106">SetByObject</span></span>
```
Set-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8385f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8385f-107">DESCRIPTION</span></span>
<span data-ttu-id="8385f-108">Polecenie cmdlet **Set-AzSynapsePipeline** tworzy potok w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="8385f-108">The **Set-AzSynapsePipeline** cmdlet creates a pipeline in workspace.</span></span>

## <span data-ttu-id="8385f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8385f-109">EXAMPLES</span></span>

### <span data-ttu-id="8385f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8385f-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="8385f-111">To polecenie tworzy potok o nazwie ContosoPipeline w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="8385f-111">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="8385f-112">Polecenie opiera się na potoku informacji w pipeline.jspliku.</span><span class="sxs-lookup"><span data-stu-id="8385f-112">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="8385f-113">Ten plik zawiera informacje o działaniach.</span><span class="sxs-lookup"><span data-stu-id="8385f-113">This file includes information about activities.</span></span>

### <span data-ttu-id="8385f-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8385f-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapsePipeline -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="8385f-115">To polecenie tworzy potok o nazwie ContosoPipeline w obszarze roboczym o nazwie ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="8385f-115">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>
<span data-ttu-id="8385f-116">Polecenie opiera się na potoku informacji w pipeline.jspliku.</span><span class="sxs-lookup"><span data-stu-id="8385f-116">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="8385f-117">Ten plik zawiera informacje o działaniach.</span><span class="sxs-lookup"><span data-stu-id="8385f-117">This file includes information about activities.</span></span>

## <span data-ttu-id="8385f-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8385f-118">PARAMETERS</span></span>

### <span data-ttu-id="8385f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8385f-119">-AsJob</span></span>
<span data-ttu-id="8385f-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8385f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8385f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8385f-121">-DefaultProfile</span></span>
<span data-ttu-id="8385f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8385f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8385f-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="8385f-123">-DefinitionFile</span></span>
<span data-ttu-id="8385f-124">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="8385f-124">The JSON file path.</span></span>

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

### <span data-ttu-id="8385f-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8385f-125">-Name</span></span>
<span data-ttu-id="8385f-126">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="8385f-126">The pipeline name.</span></span>

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

### <span data-ttu-id="8385f-127">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="8385f-127">-WorkspaceName</span></span>
<span data-ttu-id="8385f-128">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="8385f-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8385f-129">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="8385f-129">-WorkspaceObject</span></span>
<span data-ttu-id="8385f-130">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="8385f-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8385f-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8385f-131">-Confirm</span></span>
<span data-ttu-id="8385f-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8385f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8385f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8385f-133">-WhatIf</span></span>
<span data-ttu-id="8385f-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8385f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8385f-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8385f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8385f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8385f-136">CommonParameters</span></span>
<span data-ttu-id="8385f-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8385f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8385f-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8385f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8385f-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8385f-139">INPUTS</span></span>

### <span data-ttu-id="8385f-140">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8385f-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8385f-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8385f-141">OUTPUTS</span></span>

### <span data-ttu-id="8385f-142">Microsoft. Azure. Commands. Synapse. models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="8385f-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="8385f-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8385f-143">NOTES</span></span>

## <span data-ttu-id="8385f-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8385f-144">RELATED LINKS</span></span>

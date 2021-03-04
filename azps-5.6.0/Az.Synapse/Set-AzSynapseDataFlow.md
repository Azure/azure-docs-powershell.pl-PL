---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
ms.openlocfilehash: 4254a301e599dac542a099b9c4f2ebace8929ab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952977"
---
# <span data-ttu-id="1d434-101">Set-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="1d434-101">Set-AzSynapseDataFlow</span></span>

## <span data-ttu-id="1d434-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d434-102">SYNOPSIS</span></span>
<span data-ttu-id="1d434-103">Tworzy lub aktualizuje przepływ danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="1d434-103">Creates or updates a data flow in workspace.</span></span>

## <span data-ttu-id="1d434-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1d434-104">SYNTAX</span></span>

### <span data-ttu-id="1d434-105">SetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="1d434-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataFlow -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d434-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="1d434-106">SetByObject</span></span>
```
Set-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d434-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1d434-107">DESCRIPTION</span></span>
<span data-ttu-id="1d434-108">Polecenie **cmdlet Set-AzSynapseDataFlow** tworzy przepływ danych lub aktualizuje istniejący przepływ danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="1d434-108">The **Set-AzSynapseDataFlow** cmdlet creates a data flow or updates an existing data flow in workspace.</span></span>

## <span data-ttu-id="1d434-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1d434-109">EXAMPLES</span></span>

### <span data-ttu-id="1d434-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1d434-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow -DefinitionFile "C:\\samples\\DataFlow.json"
```

<span data-ttu-id="1d434-111">To polecenie tworzy przepływ danych o nazwie ContosoDataFlow w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1d434-111">This command creates a data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="1d434-112">To polecenie bazuje na przepływie danych na podstawie informacji DataFlow.jspliku.</span><span class="sxs-lookup"><span data-stu-id="1d434-112">The command bases the data flow on information in the DataFlow.json file.</span></span>

## <span data-ttu-id="1d434-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d434-113">PARAMETERS</span></span>

### <span data-ttu-id="1d434-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1d434-114">-AsJob</span></span>
<span data-ttu-id="1d434-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1d434-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d434-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d434-116">-DefaultProfile</span></span>
<span data-ttu-id="1d434-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d434-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d434-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="1d434-118">-DefinitionFile</span></span>
<span data-ttu-id="1d434-119">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="1d434-119">The JSON file path.</span></span>

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

### <span data-ttu-id="1d434-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1d434-120">-Name</span></span>
<span data-ttu-id="1d434-121">Nazwa przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="1d434-121">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d434-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1d434-122">-WorkspaceName</span></span>
<span data-ttu-id="1d434-123">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="1d434-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1d434-124">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1d434-124">-WorkspaceObject</span></span>
<span data-ttu-id="1d434-125">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="1d434-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1d434-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1d434-126">-Confirm</span></span>
<span data-ttu-id="1d434-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1d434-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d434-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d434-128">-WhatIf</span></span>
<span data-ttu-id="1d434-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d434-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d434-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1d434-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d434-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d434-131">CommonParameters</span></span>
<span data-ttu-id="1d434-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d434-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d434-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d434-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d434-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d434-134">INPUTS</span></span>

### <span data-ttu-id="1d434-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1d434-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1d434-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d434-136">OUTPUTS</span></span>

### <span data-ttu-id="1d434-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="1d434-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="1d434-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1d434-138">NOTES</span></span>

## <span data-ttu-id="1d434-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d434-139">RELATED LINKS</span></span>

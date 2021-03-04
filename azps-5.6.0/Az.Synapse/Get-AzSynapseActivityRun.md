---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseactivityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
ms.openlocfilehash: c32b0714a64e0fa97b5376861360bc3645995418
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981857"
---
# <span data-ttu-id="729d8-101">Get-AzSynapseActivityRun</span><span class="sxs-lookup"><span data-stu-id="729d8-101">Get-AzSynapseActivityRun</span></span>

## <span data-ttu-id="729d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="729d8-102">SYNOPSIS</span></span>
<span data-ttu-id="729d8-103">Pobiera informacje o działaniach uruchamianych dla uruchomienia potoku.</span><span class="sxs-lookup"><span data-stu-id="729d8-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="729d8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="729d8-104">SYNTAX</span></span>

### <span data-ttu-id="729d8-105">GetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="729d8-105">GetByName (Default)</span></span>
```
Get-AzSynapseActivityRun -WorkspaceName <String> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="729d8-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="729d8-106">GetByObject</span></span>
```
Get-AzSynapseActivityRun -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="729d8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="729d8-107">DESCRIPTION</span></span>
<span data-ttu-id="729d8-108">Polecenie **cmdlet Get-AzSynapseActivityRun** pobiera informacje o uruchamianiu w obszarze roboczym dla określonego uruchomienia potoku, które nastąpiło w określonym przedziale czasu.</span><span class="sxs-lookup"><span data-stu-id="729d8-108">The **Get-AzSynapseActivityRun** cmdlet gets information about runs in workspace for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="729d8-109">Ponadto możesz określić filtry dla nazwy działania i stanu uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="729d8-109">Additionally, you can specify filters for activity name and the status of the run.</span></span>

## <span data-ttu-id="729d8-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="729d8-110">EXAMPLES</span></span>

### <span data-ttu-id="729d8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="729d8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseActivityRun -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="729d8-112">To polecenie pobiera szczegółowe informacje o wszystkich działaniach uruchamianych w potoku o nazwie ContosoPipeline i identyfikatorem "f288712d-fb08-4cb8-96ef-82d3b9b30621", który został wydarzył się między "2018-09-01T21:00" a "2018-09-30T21:00".</span><span class="sxs-lookup"><span data-stu-id="729d8-112">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00".</span></span>

### <span data-ttu-id="729d8-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="729d8-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseActivityRun -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="729d8-114">To polecenie pobiera szczegółowe informacje o wszystkich działaniach uruchamianych w potoku o nazwie ContosoPipeline i identyfikatorem "f288712d-fb08-4cb8-96ef-82d3b9b30621", który wydarzył się między 2018-09-01T21:00" a 2018-09-30T21:00" w potoku.</span><span class="sxs-lookup"><span data-stu-id="729d8-114">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00" through pipeline.</span></span>

## <span data-ttu-id="729d8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="729d8-115">PARAMETERS</span></span>

### <span data-ttu-id="729d8-116">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="729d8-116">-ActivityName</span></span>
<span data-ttu-id="729d8-117">Nazwa działania.</span><span class="sxs-lookup"><span data-stu-id="729d8-117">The name of the activity.</span></span>

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

### <span data-ttu-id="729d8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="729d8-118">-DefaultProfile</span></span>
<span data-ttu-id="729d8-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="729d8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="729d8-120">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="729d8-120">-PipelineName</span></span>
<span data-ttu-id="729d8-121">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="729d8-121">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729d8-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="729d8-122">-PipelineRunId</span></span>
<span data-ttu-id="729d8-123">Identyfikator uruchomienia potoku.</span><span class="sxs-lookup"><span data-stu-id="729d8-123">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729d8-124">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="729d8-124">-RunStartedAfter</span></span>
<span data-ttu-id="729d8-125">Godzina lub godzina, po której zdarzenie uruchomienia zostało zaktualizowane w formacie "ISO 8601".</span><span class="sxs-lookup"><span data-stu-id="729d8-125">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729d8-126">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="729d8-126">-RunStartedBefore</span></span>
<span data-ttu-id="729d8-127">Godzina lub wcześniejsza aktualizacja zdarzenia uruchomienia w formacie "ISO 8601".</span><span class="sxs-lookup"><span data-stu-id="729d8-127">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729d8-128">— Status</span><span class="sxs-lookup"><span data-stu-id="729d8-128">-Status</span></span>
<span data-ttu-id="729d8-129">Stan uruchomienia potoku.</span><span class="sxs-lookup"><span data-stu-id="729d8-129">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="729d8-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="729d8-130">-WorkspaceName</span></span>
<span data-ttu-id="729d8-131">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="729d8-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729d8-132">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="729d8-132">-WorkspaceObject</span></span>
<span data-ttu-id="729d8-133">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="729d8-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="729d8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="729d8-134">CommonParameters</span></span>
<span data-ttu-id="729d8-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="729d8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="729d8-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="729d8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="729d8-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="729d8-137">INPUTS</span></span>

### <span data-ttu-id="729d8-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="729d8-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="729d8-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="729d8-139">OUTPUTS</span></span>

### <span data-ttu-id="729d8-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span><span class="sxs-lookup"><span data-stu-id="729d8-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span></span>

## <span data-ttu-id="729d8-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="729d8-141">NOTES</span></span>

## <span data-ttu-id="729d8-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="729d8-142">RELATED LINKS</span></span>

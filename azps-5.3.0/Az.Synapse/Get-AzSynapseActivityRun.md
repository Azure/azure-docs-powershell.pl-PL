---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseactivityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
ms.openlocfilehash: fd300a54b3f35aa69a94bfee69cfcf7ca60f95a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491117"
---
# <span data-ttu-id="1280a-101">Get-AzSynapseActivityRun</span><span class="sxs-lookup"><span data-stu-id="1280a-101">Get-AzSynapseActivityRun</span></span>

## <span data-ttu-id="1280a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1280a-102">SYNOPSIS</span></span>
<span data-ttu-id="1280a-103">Pobiera informacje o działaniach dotyczących uruchamiania rurociągu.</span><span class="sxs-lookup"><span data-stu-id="1280a-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="1280a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1280a-104">SYNTAX</span></span>

### <span data-ttu-id="1280a-105">GetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1280a-105">GetByName (Default)</span></span>
```
Get-AzSynapseActivityRun -WorkspaceName <String> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1280a-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="1280a-106">GetByObject</span></span>
```
Get-AzSynapseActivityRun -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1280a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1280a-107">DESCRIPTION</span></span>
<span data-ttu-id="1280a-108">Polecenie cmdlet **Get-AzSynapseActivityRun** pobiera informacje o działaniu w obszarze roboczym dla określonego przebiegu procesu, który wystąpił w danym przedziale czasu.</span><span class="sxs-lookup"><span data-stu-id="1280a-108">The **Get-AzSynapseActivityRun** cmdlet gets information about runs in workspace for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="1280a-109">Ponadto możesz określić filtry dla nazwy działania i stanu uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="1280a-109">Additionally, you can specify filters for activity name and the status of the run.</span></span>

## <span data-ttu-id="1280a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1280a-110">EXAMPLES</span></span>

### <span data-ttu-id="1280a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1280a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseActivityRun -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="1280a-112">To polecenie pobiera szczegóły dotyczące wszystkich działań uruchomionych w potoku o nazwie ContosoPipeline Uruchom z IDENTYFIKATORem "f288712d-FB08-4cb8-96ef-82d3b9b30621", który wystąpił między "2018-09-01T21:00" i "2018-09-30T21:00".</span><span class="sxs-lookup"><span data-stu-id="1280a-112">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00".</span></span>

### <span data-ttu-id="1280a-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1280a-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseActivityRun -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="1280a-114">To polecenie pobiera szczegóły dotyczące wszystkich działań wykonywanych w potoku o nazwie ContosoPipeline Uruchom z IDENTYFIKATORem "f288712d-FB08-4cb8-96ef-82d3b9b30621", który wystąpił między "2018-09-01T21:00" i "2018-09-30T21:00" do rurociągu.</span><span class="sxs-lookup"><span data-stu-id="1280a-114">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00" through pipeline.</span></span>

## <span data-ttu-id="1280a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1280a-115">PARAMETERS</span></span>

### <span data-ttu-id="1280a-116">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="1280a-116">-ActivityName</span></span>
<span data-ttu-id="1280a-117">Nazwa działania.</span><span class="sxs-lookup"><span data-stu-id="1280a-117">The name of the activity.</span></span>

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

### <span data-ttu-id="1280a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1280a-118">-DefaultProfile</span></span>
<span data-ttu-id="1280a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1280a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1280a-120">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="1280a-120">-PipelineName</span></span>
<span data-ttu-id="1280a-121">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="1280a-121">The pipeline name.</span></span>

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

### <span data-ttu-id="1280a-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="1280a-122">-PipelineRunId</span></span>
<span data-ttu-id="1280a-123">Identyfikator uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="1280a-123">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="1280a-124">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="1280a-124">-RunStartedAfter</span></span>
<span data-ttu-id="1280a-125">Czas, po którym zdarzenie uruchomienia zostało zaktualizowane w formacie ISO 8601 '.</span><span class="sxs-lookup"><span data-stu-id="1280a-125">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="1280a-126">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="1280a-126">-RunStartedBefore</span></span>
<span data-ttu-id="1280a-127">Czas, w którym lub przed upływem którego zdarzenie Uruchom zostanie zaktualizowane w formacie "ISO 8601".</span><span class="sxs-lookup"><span data-stu-id="1280a-127">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="1280a-128">-Status</span><span class="sxs-lookup"><span data-stu-id="1280a-128">-Status</span></span>
<span data-ttu-id="1280a-129">Stan uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="1280a-129">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="1280a-130">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="1280a-130">-WorkspaceName</span></span>
<span data-ttu-id="1280a-131">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="1280a-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1280a-132">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="1280a-132">-WorkspaceObject</span></span>
<span data-ttu-id="1280a-133">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="1280a-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1280a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1280a-134">CommonParameters</span></span>
<span data-ttu-id="1280a-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1280a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1280a-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1280a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1280a-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1280a-137">INPUTS</span></span>

### <span data-ttu-id="1280a-138">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1280a-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1280a-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1280a-139">OUTPUTS</span></span>

### <span data-ttu-id="1280a-140">Microsoft. Azure. Commands. Synapse. models. PSActivityRunsQueryResponse</span><span class="sxs-lookup"><span data-stu-id="1280a-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span></span>

## <span data-ttu-id="1280a-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1280a-141">NOTES</span></span>

## <span data-ttu-id="1280a-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1280a-142">RELATED LINKS</span></span>

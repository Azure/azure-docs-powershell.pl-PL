---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
ms.openlocfilehash: 365311b156b8bd6f2c61da760c6b82a3b2d5dfb4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491090"
---
# <span data-ttu-id="e1b81-101">Get-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="e1b81-101">Get-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="e1b81-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1b81-102">SYNOPSIS</span></span>
<span data-ttu-id="e1b81-103">Pobiera informacje o przebiegach potokowych.</span><span class="sxs-lookup"><span data-stu-id="e1b81-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="e1b81-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1b81-104">SYNTAX</span></span>

### <span data-ttu-id="e1b81-105">GetByNameAndId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e1b81-105">GetByNameAndId (Default)</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1b81-106">GetByNameAndTime</span><span class="sxs-lookup"><span data-stu-id="e1b81-106">GetByNameAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1b81-107">GetByObjectAndId</span><span class="sxs-lookup"><span data-stu-id="e1b81-107">GetByObjectAndId</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1b81-108">GetByObjectAndTime</span><span class="sxs-lookup"><span data-stu-id="e1b81-108">GetByObjectAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1b81-109">Opis</span><span class="sxs-lookup"><span data-stu-id="e1b81-109">DESCRIPTION</span></span>
<span data-ttu-id="e1b81-110">Polecenie **Get-AzSynapsePipelineRun** zwraca informacje dotyczące uruchamiania określonego potoku.</span><span class="sxs-lookup"><span data-stu-id="e1b81-110">The **Get-AzSynapsePipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="e1b81-111">Jeśli PipelineRunId jest określony, wyświetlane są szczegóły dotyczące uruchamiania z tym IDENTYFIKATORem.</span><span class="sxs-lookup"><span data-stu-id="e1b81-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="e1b81-112">Jeśli nie podano PipelineRunId, wyświetlane są informacje o wszystkich przebiegach dla rurociągów, które wystąpiły między wartościami RunStartedAfter i RunStartedBefore.</span><span class="sxs-lookup"><span data-stu-id="e1b81-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of RunStartedAfter and RunStartedBefore.</span></span>

## <span data-ttu-id="e1b81-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1b81-113">EXAMPLES</span></span>

### <span data-ttu-id="e1b81-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e1b81-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"
```

<span data-ttu-id="e1b81-115">To polecenie pobiera szczegóły dotyczące procesu o IDENTYFIKATORze "61eb095a-FE23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="e1b81-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="e1b81-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1b81-116">PARAMETERS</span></span>

### <span data-ttu-id="e1b81-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1b81-117">-DefaultProfile</span></span>
<span data-ttu-id="e1b81-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1b81-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1b81-119">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="e1b81-119">-PipelineName</span></span>
<span data-ttu-id="e1b81-120">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="e1b81-120">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b81-121">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="e1b81-121">-PipelineRunId</span></span>
<span data-ttu-id="e1b81-122">Identyfikator uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="e1b81-122">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByObjectAndId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b81-123">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="e1b81-123">-RunStartedAfter</span></span>
<span data-ttu-id="e1b81-124">Czas, po którym zdarzenie uruchomienia zostało zaktualizowane w formacie ISO 8601 '.</span><span class="sxs-lookup"><span data-stu-id="e1b81-124">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b81-125">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="e1b81-125">-RunStartedBefore</span></span>
<span data-ttu-id="e1b81-126">Czas, w którym lub przed upływem którego zdarzenie Uruchom zostanie zaktualizowane w formacie "ISO 8601".</span><span class="sxs-lookup"><span data-stu-id="e1b81-126">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b81-127">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="e1b81-127">-WorkspaceName</span></span>
<span data-ttu-id="e1b81-128">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="e1b81-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByNameAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b81-129">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="e1b81-129">-WorkspaceObject</span></span>
<span data-ttu-id="e1b81-130">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="e1b81-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObjectAndId, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1b81-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1b81-131">CommonParameters</span></span>
<span data-ttu-id="e1b81-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1b81-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1b81-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1b81-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1b81-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1b81-134">INPUTS</span></span>

### <span data-ttu-id="e1b81-135">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e1b81-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e1b81-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1b81-136">OUTPUTS</span></span>

### <span data-ttu-id="e1b81-137">Microsoft. Azure. Commands. Synapse. models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="e1b81-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="e1b81-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1b81-138">NOTES</span></span>

## <span data-ttu-id="e1b81-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1b81-139">RELATED LINKS</span></span>

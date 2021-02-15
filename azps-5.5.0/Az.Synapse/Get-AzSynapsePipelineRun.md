---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
ms.openlocfilehash: 365311b156b8bd6f2c61da760c6b82a3b2d5dfb4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197378"
---
# <span data-ttu-id="68d39-101">Get-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="68d39-101">Get-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="68d39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68d39-102">SYNOPSIS</span></span>
<span data-ttu-id="68d39-103">Pobiera informacje o uruchamianych potokach.</span><span class="sxs-lookup"><span data-stu-id="68d39-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="68d39-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="68d39-104">SYNTAX</span></span>

### <span data-ttu-id="68d39-105">GetByNameAndId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="68d39-105">GetByNameAndId (Default)</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68d39-106">GetByNameAndTime</span><span class="sxs-lookup"><span data-stu-id="68d39-106">GetByNameAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="68d39-107">GetByObjectAndId</span><span class="sxs-lookup"><span data-stu-id="68d39-107">GetByObjectAndId</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68d39-108">GetByObjectAndTime</span><span class="sxs-lookup"><span data-stu-id="68d39-108">GetByObjectAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68d39-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="68d39-109">DESCRIPTION</span></span>
<span data-ttu-id="68d39-110">Polecenie **Get-AzSynapsePipelineRun zwraca** informacje o uruchomieniach dla określonego potoku.</span><span class="sxs-lookup"><span data-stu-id="68d39-110">The **Get-AzSynapsePipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="68d39-111">Jeśli określono wartość PipelineRunId, są w nim podane szczegóły dotyczące uruchomienia z tym identyfikatorem.</span><span class="sxs-lookup"><span data-stu-id="68d39-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="68d39-112">Jeśli wartość PipelineRunId nie jest określona, wyświetla informacje o wszystkich uruchomieniach dla potoków, które się wydarzyły między wartościami RunStartedAfter i RunStartedBefore.</span><span class="sxs-lookup"><span data-stu-id="68d39-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of RunStartedAfter and RunStartedBefore.</span></span>

## <span data-ttu-id="68d39-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="68d39-113">EXAMPLES</span></span>

### <span data-ttu-id="68d39-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="68d39-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"
```

<span data-ttu-id="68d39-115">To polecenie pobiera szczegółowe informacje o uruchomieniu potoku o identyfikatorze "61eb095a-fe23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="68d39-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="68d39-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68d39-116">PARAMETERS</span></span>

### <span data-ttu-id="68d39-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68d39-117">-DefaultProfile</span></span>
<span data-ttu-id="68d39-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="68d39-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68d39-119">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="68d39-119">-PipelineName</span></span>
<span data-ttu-id="68d39-120">Nazwa potoku.</span><span class="sxs-lookup"><span data-stu-id="68d39-120">The pipeline name.</span></span>

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

### <span data-ttu-id="68d39-121">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="68d39-121">-PipelineRunId</span></span>
<span data-ttu-id="68d39-122">Identyfikator uruchomienia potoku.</span><span class="sxs-lookup"><span data-stu-id="68d39-122">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="68d39-123">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="68d39-123">-RunStartedAfter</span></span>
<span data-ttu-id="68d39-124">Godzina lub godzina, po której zdarzenie uruchomienia zostało zaktualizowane w formacie "ISO 8601".</span><span class="sxs-lookup"><span data-stu-id="68d39-124">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="68d39-125">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="68d39-125">-RunStartedBefore</span></span>
<span data-ttu-id="68d39-126">Godzina lub wcześniejsza aktualizacja zdarzenia uruchomienia w formacie "ISO 8601".</span><span class="sxs-lookup"><span data-stu-id="68d39-126">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="68d39-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="68d39-127">-WorkspaceName</span></span>
<span data-ttu-id="68d39-128">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="68d39-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="68d39-129">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="68d39-129">-WorkspaceObject</span></span>
<span data-ttu-id="68d39-130">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="68d39-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="68d39-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68d39-131">CommonParameters</span></span>
<span data-ttu-id="68d39-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68d39-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68d39-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68d39-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68d39-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68d39-134">INPUTS</span></span>

### <span data-ttu-id="68d39-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="68d39-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="68d39-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68d39-136">OUTPUTS</span></span>

### <span data-ttu-id="68d39-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="68d39-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="68d39-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="68d39-138">NOTES</span></span>

## <span data-ttu-id="68d39-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68d39-139">RELATED LINKS</span></span>

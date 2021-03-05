---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsetriggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
ms.openlocfilehash: 284974cc2d4cb98519b82c5c5a50e40d323dc354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977946"
---
# <span data-ttu-id="3fdf1-101">Get-AzSynapseTriggerRun</span><span class="sxs-lookup"><span data-stu-id="3fdf1-101">Get-AzSynapseTriggerRun</span></span>

## <span data-ttu-id="3fdf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fdf1-102">SYNOPSIS</span></span>
<span data-ttu-id="3fdf1-103">Zwraca informacje o uruchomieniach wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="3fdf1-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="3fdf1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3fdf1-104">SYNTAX</span></span>

### <span data-ttu-id="3fdf1-105">GetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="3fdf1-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceName <String> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fdf1-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="3fdf1-106">GetByObject</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceObject <PSSynapseWorkspace> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fdf1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3fdf1-107">DESCRIPTION</span></span>
<span data-ttu-id="3fdf1-108">Polecenie **Get-AzSynapseTriggerRun** zwraca szczegółowe informacje o wyzwalaczu uruchamianym dla określonego wyzwalacza w danym przedziale czasu.</span><span class="sxs-lookup"><span data-stu-id="3fdf1-108">The **Get-AzSynapseTriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="3fdf1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3fdf1-109">EXAMPLES</span></span>

### <span data-ttu-id="3fdf1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3fdf1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerRun -WorkspaceName ContosoWorkspace -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="3fdf1-111">To polecenie zawiera informacje o uruchamianiu programu ContosoTrigger w obszarze roboczym ContosoWorkspace, które rozpoczęło się między godziną "2018-09-01T21:00" i "2019-09-01T21:00".</span><span class="sxs-lookup"><span data-stu-id="3fdf1-111">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00".</span></span>

### <span data-ttu-id="3fdf1-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3fdf1-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerRun -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="3fdf1-113">To polecenie zawiera informacje o uruchomieniach dla programu ContosoTrigger w obszarze roboczym ContosoWorkspace, który rozpoczynał się między godziną "2018-09-01T21:00" i "2019-09-01T21:00" w ramach potoku.</span><span class="sxs-lookup"><span data-stu-id="3fdf1-113">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00" through pipeline.</span></span>

## <span data-ttu-id="3fdf1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fdf1-114">PARAMETERS</span></span>

### <span data-ttu-id="3fdf1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fdf1-115">-DefaultProfile</span></span>
<span data-ttu-id="3fdf1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3fdf1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fdf1-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3fdf1-117">-Name</span></span>
<span data-ttu-id="3fdf1-118">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="3fdf1-118">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fdf1-119">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="3fdf1-119">-RunStartedAfter</span></span>
<span data-ttu-id="3fdf1-120">Godzina lub godzina, po której zdarzenie uruchomienia zostało zaktualizowane w formacie "ISO 8601".</span><span class="sxs-lookup"><span data-stu-id="3fdf1-120">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="3fdf1-121">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="3fdf1-121">-RunStartedBefore</span></span>
<span data-ttu-id="3fdf1-122">Godzina lub wcześniejsza aktualizacja zdarzenia uruchomienia w formacie "ISO 8601".</span><span class="sxs-lookup"><span data-stu-id="3fdf1-122">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="3fdf1-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3fdf1-123">-WorkspaceName</span></span>
<span data-ttu-id="3fdf1-124">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="3fdf1-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3fdf1-125">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3fdf1-125">-WorkspaceObject</span></span>
<span data-ttu-id="3fdf1-126">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="3fdf1-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3fdf1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fdf1-127">CommonParameters</span></span>
<span data-ttu-id="3fdf1-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fdf1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fdf1-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3fdf1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fdf1-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fdf1-130">INPUTS</span></span>

### <span data-ttu-id="3fdf1-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3fdf1-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3fdf1-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fdf1-132">OUTPUTS</span></span>

### <span data-ttu-id="3fdf1-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="3fdf1-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span></span>

## <span data-ttu-id="3fdf1-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3fdf1-134">NOTES</span></span>

## <span data-ttu-id="3fdf1-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3fdf1-135">RELATED LINKS</span></span>

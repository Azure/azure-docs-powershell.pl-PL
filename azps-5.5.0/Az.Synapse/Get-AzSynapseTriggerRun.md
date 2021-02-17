---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
ms.openlocfilehash: 0d6d3bb99062177e1d75c4ab496562782cf142c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190611"
---
# <span data-ttu-id="d71ea-101">Get-AzSynapseTriggerRun</span><span class="sxs-lookup"><span data-stu-id="d71ea-101">Get-AzSynapseTriggerRun</span></span>

## <span data-ttu-id="d71ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d71ea-102">SYNOPSIS</span></span>
<span data-ttu-id="d71ea-103">Zwraca informacje o uruchomieniach wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="d71ea-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="d71ea-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d71ea-104">SYNTAX</span></span>

### <span data-ttu-id="d71ea-105">GetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="d71ea-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceName <String> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d71ea-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="d71ea-106">GetByObject</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceObject <PSSynapseWorkspace> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d71ea-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d71ea-107">DESCRIPTION</span></span>
<span data-ttu-id="d71ea-108">Polecenie **Get-AzSynapseTriggerRun** zwraca szczegółowe informacje o wyzwalaczu uruchamianym dla określonego wyzwalacza w danym przedziale czasu.</span><span class="sxs-lookup"><span data-stu-id="d71ea-108">The **Get-AzSynapseTriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="d71ea-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d71ea-109">EXAMPLES</span></span>

### <span data-ttu-id="d71ea-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d71ea-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerRun -WorkspaceName ContosoWorkspace -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="d71ea-111">To polecenie zawiera informacje o uruchamianiu programu ContosoTrigger w obszarze roboczym ContosoWorkspace, które rozpoczęło się między godziną "2018-09-01T21:00" i "2019-09-01T21:00".</span><span class="sxs-lookup"><span data-stu-id="d71ea-111">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00".</span></span>

### <span data-ttu-id="d71ea-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d71ea-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerRun -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="d71ea-113">To polecenie zawiera informacje o uruchomieniach dla programu ContosoTrigger w obszarze roboczym ContosoWorkspace, które rozpoczęło się między godziną "2018-09-01T21:00" i "2019-09-01T21:00" za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="d71ea-113">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00" through pipeline.</span></span>

## <span data-ttu-id="d71ea-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d71ea-114">PARAMETERS</span></span>

### <span data-ttu-id="d71ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d71ea-115">-DefaultProfile</span></span>
<span data-ttu-id="d71ea-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d71ea-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d71ea-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d71ea-117">-Name</span></span>
<span data-ttu-id="d71ea-118">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="d71ea-118">The trigger name.</span></span>

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

### <span data-ttu-id="d71ea-119">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="d71ea-119">-RunStartedAfter</span></span>
<span data-ttu-id="d71ea-120">Godzina lub godzina, po której zdarzenie uruchomienia zostało zaktualizowane w formacie "ISO 8601".</span><span class="sxs-lookup"><span data-stu-id="d71ea-120">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="d71ea-121">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="d71ea-121">-RunStartedBefore</span></span>
<span data-ttu-id="d71ea-122">Godzina lub wcześniejsza aktualizacja zdarzenia uruchomienia w formacie "ISO 8601".</span><span class="sxs-lookup"><span data-stu-id="d71ea-122">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="d71ea-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d71ea-123">-WorkspaceName</span></span>
<span data-ttu-id="d71ea-124">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="d71ea-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d71ea-125">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d71ea-125">-WorkspaceObject</span></span>
<span data-ttu-id="d71ea-126">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="d71ea-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d71ea-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d71ea-127">CommonParameters</span></span>
<span data-ttu-id="d71ea-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d71ea-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d71ea-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d71ea-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d71ea-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d71ea-130">INPUTS</span></span>

### <span data-ttu-id="d71ea-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d71ea-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d71ea-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d71ea-132">OUTPUTS</span></span>

### <span data-ttu-id="d71ea-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="d71ea-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span></span>

## <span data-ttu-id="d71ea-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d71ea-134">NOTES</span></span>

## <span data-ttu-id="d71ea-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d71ea-135">RELATED LINKS</span></span>

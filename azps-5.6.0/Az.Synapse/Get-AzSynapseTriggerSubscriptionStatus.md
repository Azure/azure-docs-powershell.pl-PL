---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: c0c1b83f177b568e7058b973b788a633cfefe48c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970129"
---
# <span data-ttu-id="33a1a-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="33a1a-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="33a1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="33a1a-103">Uzyskiwanie stanu subskrypcji wyzwalacza zdarzenia dla określonych zdarzeń usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="33a1a-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="33a1a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="33a1a-104">SYNTAX</span></span>

### <span data-ttu-id="33a1a-105">GetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="33a1a-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33a1a-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="33a1a-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33a1a-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="33a1a-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33a1a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="33a1a-108">DESCRIPTION</span></span>
<span data-ttu-id="33a1a-109">Polecenie **cmdlet Get-AzSynapseTriggerSubscriptionStatus** pobiera stan subskrypcji wyzwalacza zdarzenia do określonych zdarzeń usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="33a1a-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="33a1a-110">Wyzwalacza nie można uruchomić, dopóki nie zostanie zwrócony stan "Włączony".</span><span class="sxs-lookup"><span data-stu-id="33a1a-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="33a1a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="33a1a-111">EXAMPLES</span></span>

### <span data-ttu-id="33a1a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="33a1a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="33a1a-113">To polecenie pobierze stan subscribtion wyzwalacza o nazwie ContosoTrigger do zdarzeń usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="33a1a-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="33a1a-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="33a1a-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="33a1a-115">To polecenie pobierze stan subscribtion wyzwalacza o nazwie ContosoTrigger do zdarzeń usługi zewnętrznej za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="33a1a-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="33a1a-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="33a1a-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="33a1a-117">To polecenie pobierze stan subscribtion wyzwalacza o nazwie ContosoTrigger do zdarzeń usługi zewnętrznej za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="33a1a-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="33a1a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33a1a-118">PARAMETERS</span></span>

### <span data-ttu-id="33a1a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33a1a-119">-DefaultProfile</span></span>
<span data-ttu-id="33a1a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="33a1a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33a1a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33a1a-121">-InputObject</span></span>
<span data-ttu-id="33a1a-122">Obiekt wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="33a1a-122">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33a1a-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="33a1a-123">-Name</span></span>
<span data-ttu-id="33a1a-124">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="33a1a-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, GetByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33a1a-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="33a1a-125">-WorkspaceName</span></span>
<span data-ttu-id="33a1a-126">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="33a1a-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="33a1a-127">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="33a1a-127">-WorkspaceObject</span></span>
<span data-ttu-id="33a1a-128">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="33a1a-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="33a1a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33a1a-129">CommonParameters</span></span>
<span data-ttu-id="33a1a-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33a1a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33a1a-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33a1a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33a1a-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33a1a-132">INPUTS</span></span>

### <span data-ttu-id="33a1a-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="33a1a-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="33a1a-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="33a1a-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="33a1a-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33a1a-135">OUTPUTS</span></span>

### <span data-ttu-id="33a1a-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span><span class="sxs-lookup"><span data-stu-id="33a1a-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="33a1a-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="33a1a-137">NOTES</span></span>

## <span data-ttu-id="33a1a-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33a1a-138">RELATED LINKS</span></span>

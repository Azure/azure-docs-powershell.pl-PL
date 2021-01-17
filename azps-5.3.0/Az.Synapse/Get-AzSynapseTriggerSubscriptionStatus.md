---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: b18a308b94bdb486945186c67c3a905bcb0408d3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383714"
---
# <span data-ttu-id="d0c6f-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="d0c6f-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="d0c6f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0c6f-102">SYNOPSIS</span></span>
<span data-ttu-id="d0c6f-103">Uzyskaj stan subskrypcji wyzwalacza zdarzeń na określone zdarzenia usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="d0c6f-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="d0c6f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0c6f-104">SYNTAX</span></span>

### <span data-ttu-id="d0c6f-105">GetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d0c6f-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0c6f-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="d0c6f-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0c6f-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="d0c6f-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0c6f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d0c6f-108">DESCRIPTION</span></span>
<span data-ttu-id="d0c6f-109">Polecenie cmdlet **Get-AzSynapseTriggerSubscriptionStatus** Pobiera stan subskrypcji wyzwalacza zdarzeń do określonych zdarzeń usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="d0c6f-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="d0c6f-110">Nie można uruchomić wyzwalacza, dopóki nie zostanie zwrócony stan "włączony".</span><span class="sxs-lookup"><span data-stu-id="d0c6f-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="d0c6f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0c6f-111">EXAMPLES</span></span>

### <span data-ttu-id="d0c6f-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d0c6f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="d0c6f-113">To polecenie uzyska stan subscribtion dla wyzwalacza o nazwie ContosoTrigger na zdarzenia usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="d0c6f-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="d0c6f-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d0c6f-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="d0c6f-115">To polecenie uzyska stan subscribtion dla wyzwalacza o nazwie ContosoTrigger do zdarzeń usługi zewnętrznej za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="d0c6f-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="d0c6f-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d0c6f-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="d0c6f-117">To polecenie uzyska stan subscribtion dla wyzwalacza o nazwie ContosoTrigger do zdarzeń usługi zewnętrznej za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="d0c6f-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="d0c6f-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0c6f-118">PARAMETERS</span></span>

### <span data-ttu-id="d0c6f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0c6f-119">-DefaultProfile</span></span>
<span data-ttu-id="d0c6f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0c6f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0c6f-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d0c6f-121">-InputObject</span></span>
<span data-ttu-id="d0c6f-122">Obiekt Trigger.</span><span class="sxs-lookup"><span data-stu-id="d0c6f-122">The trigger object.</span></span>

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

### <span data-ttu-id="d0c6f-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d0c6f-123">-Name</span></span>
<span data-ttu-id="d0c6f-124">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="d0c6f-124">The trigger name.</span></span>

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

### <span data-ttu-id="d0c6f-125">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="d0c6f-125">-WorkspaceName</span></span>
<span data-ttu-id="d0c6f-126">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="d0c6f-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d0c6f-127">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="d0c6f-127">-WorkspaceObject</span></span>
<span data-ttu-id="d0c6f-128">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="d0c6f-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d0c6f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0c6f-129">CommonParameters</span></span>
<span data-ttu-id="d0c6f-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0c6f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0c6f-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0c6f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0c6f-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0c6f-132">INPUTS</span></span>

### <span data-ttu-id="d0c6f-133">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d0c6f-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d0c6f-134">Microsoft. Azure. Commands. Synapse. models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="d0c6f-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="d0c6f-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0c6f-135">OUTPUTS</span></span>

### <span data-ttu-id="d0c6f-136">Microsoft. Azure. Commands. Synapse. models. PSTriggerSubscriptionOperationStatus</span><span class="sxs-lookup"><span data-stu-id="d0c6f-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="d0c6f-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0c6f-137">NOTES</span></span>

## <span data-ttu-id="d0c6f-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0c6f-138">RELATED LINKS</span></span>

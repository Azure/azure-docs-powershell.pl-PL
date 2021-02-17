---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: b18a308b94bdb486945186c67c3a905bcb0408d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190610"
---
# <span data-ttu-id="47e6f-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="47e6f-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="47e6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47e6f-102">SYNOPSIS</span></span>
<span data-ttu-id="47e6f-103">Uzyskiwanie stanu subskrypcji wyzwalacza zdarzenia dla określonych zdarzeń usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="47e6f-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="47e6f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="47e6f-104">SYNTAX</span></span>

### <span data-ttu-id="47e6f-105">GetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="47e6f-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47e6f-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="47e6f-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47e6f-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="47e6f-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47e6f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="47e6f-108">DESCRIPTION</span></span>
<span data-ttu-id="47e6f-109">Polecenie **cmdlet Get-AzSynapseTriggerSubscriptionStatus** pobiera stan subskrypcji wyzwalacza zdarzenia do określonych zdarzeń usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="47e6f-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="47e6f-110">Wyzwalacza nie można uruchomić, dopóki nie zostanie zwrócony stan "Włączony".</span><span class="sxs-lookup"><span data-stu-id="47e6f-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="47e6f-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="47e6f-111">EXAMPLES</span></span>

### <span data-ttu-id="47e6f-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="47e6f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="47e6f-113">To polecenie pobierze stan subscribtion wyzwalacza o nazwie ContosoTrigger do zdarzeń usługi zewnętrznej.</span><span class="sxs-lookup"><span data-stu-id="47e6f-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="47e6f-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="47e6f-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="47e6f-115">To polecenie pobierze stan subscribtion wyzwalacza o nazwie ContosoTrigger do zdarzeń usługi zewnętrznej za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="47e6f-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="47e6f-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="47e6f-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="47e6f-117">To polecenie pobierze stan subscribtion wyzwalacza o nazwie ContosoTrigger do zdarzeń usługi zewnętrznej za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="47e6f-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="47e6f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47e6f-118">PARAMETERS</span></span>

### <span data-ttu-id="47e6f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47e6f-119">-DefaultProfile</span></span>
<span data-ttu-id="47e6f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="47e6f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47e6f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47e6f-121">-InputObject</span></span>
<span data-ttu-id="47e6f-122">Obiekt wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="47e6f-122">The trigger object.</span></span>

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

### <span data-ttu-id="47e6f-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="47e6f-123">-Name</span></span>
<span data-ttu-id="47e6f-124">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="47e6f-124">The trigger name.</span></span>

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

### <span data-ttu-id="47e6f-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="47e6f-125">-WorkspaceName</span></span>
<span data-ttu-id="47e6f-126">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="47e6f-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="47e6f-127">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="47e6f-127">-WorkspaceObject</span></span>
<span data-ttu-id="47e6f-128">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="47e6f-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="47e6f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47e6f-129">CommonParameters</span></span>
<span data-ttu-id="47e6f-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47e6f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47e6f-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47e6f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47e6f-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47e6f-132">INPUTS</span></span>

### <span data-ttu-id="47e6f-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="47e6f-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="47e6f-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="47e6f-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="47e6f-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47e6f-135">OUTPUTS</span></span>

### <span data-ttu-id="47e6f-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span><span class="sxs-lookup"><span data-stu-id="47e6f-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="47e6f-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="47e6f-137">NOTES</span></span>

## <span data-ttu-id="47e6f-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47e6f-138">RELATED LINKS</span></span>

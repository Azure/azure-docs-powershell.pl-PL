---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
ms.openlocfilehash: 9e39d6458ca330909e500a45532d0a9d66f404af
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359340"
---
# <span data-ttu-id="3e854-101">Get-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="3e854-101">Get-AzSynapseTrigger</span></span>

## <span data-ttu-id="3e854-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e854-102">SYNOPSIS</span></span>
<span data-ttu-id="3e854-103">Pobiera informacje o wyzwalaczach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="3e854-103">Gets information about triggers in a workspace.</span></span>

## <span data-ttu-id="3e854-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e854-104">SYNTAX</span></span>

### <span data-ttu-id="3e854-105">GetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3e854-105">GetByName (Default)</span></span>
```
Get-AzSynapseTrigger -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e854-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="3e854-106">GetByObject</span></span>
```
Get-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e854-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3e854-107">DESCRIPTION</span></span>
<span data-ttu-id="3e854-108">Polecenie cmdlet **Get-AzSynapseTrigger** pobiera informacje o wyzwalaczach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="3e854-108">The **Get-AzSynapseTrigger** cmdlet gets information about triggers in a workspace.</span></span> <span data-ttu-id="3e854-109">Jeśli określisz nazwę wyzwalacza, polecenie cmdlet pobiera informacje o tym wyzwalaczu.</span><span class="sxs-lookup"><span data-stu-id="3e854-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="3e854-110">Jeśli nie określisz nazwy, polecenie cmdlet pobiera informacje o wszystkich wyzwalaczach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="3e854-110">If you do not specify a name, the cmdlet gets information about all triggers in the workspace.</span></span>

## <span data-ttu-id="3e854-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e854-111">EXAMPLES</span></span>

### <span data-ttu-id="3e854-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3e854-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="3e854-113">Pobiera listę wszystkich wyzwalaczy utworzonych w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3e854-113">Gets a list of all triggers that have been created in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="3e854-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3e854-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="3e854-115">Pobiera jeden wyzwalacz o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3e854-115">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="3e854-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="3e854-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="3e854-117">Pobiera jeden wyzwalacz o nazwie ContosoTrigger w obszarze roboczym ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="3e854-117">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="3e854-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e854-118">PARAMETERS</span></span>

### <span data-ttu-id="3e854-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e854-119">-DefaultProfile</span></span>
<span data-ttu-id="3e854-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e854-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e854-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3e854-121">-Name</span></span>
<span data-ttu-id="3e854-122">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="3e854-122">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e854-123">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="3e854-123">-WorkspaceName</span></span>
<span data-ttu-id="3e854-124">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="3e854-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3e854-125">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="3e854-125">-WorkspaceObject</span></span>
<span data-ttu-id="3e854-126">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="3e854-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3e854-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e854-127">CommonParameters</span></span>
<span data-ttu-id="3e854-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e854-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e854-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e854-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e854-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e854-130">INPUTS</span></span>

### <span data-ttu-id="3e854-131">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3e854-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3e854-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e854-132">OUTPUTS</span></span>

### <span data-ttu-id="3e854-133">Microsoft. Azure. Commands. Synapse. models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="3e854-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="3e854-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e854-134">NOTES</span></span>

## <span data-ttu-id="3e854-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e854-135">RELATED LINKS</span></span>

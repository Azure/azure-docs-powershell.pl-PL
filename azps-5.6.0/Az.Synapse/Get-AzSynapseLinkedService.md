---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
ms.openlocfilehash: 61ddc7c6a71dcc5545b8bdc2751e619d7da8e3bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967217"
---
# <span data-ttu-id="3aeee-101">Get-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="3aeee-101">Get-AzSynapseLinkedService</span></span>

## <span data-ttu-id="3aeee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3aeee-102">SYNOPSIS</span></span>
<span data-ttu-id="3aeee-103">Pobiera informacje o usługach połączonych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="3aeee-103">Gets information about linked services in workspace.</span></span>

## <span data-ttu-id="3aeee-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3aeee-104">SYNTAX</span></span>

### <span data-ttu-id="3aeee-105">GetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="3aeee-105">GetByName (Default)</span></span>
```
Get-AzSynapseLinkedService -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3aeee-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="3aeee-106">GetByObject</span></span>
```
Get-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3aeee-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3aeee-107">DESCRIPTION</span></span>
<span data-ttu-id="3aeee-108">Polecenie **cmdlet Get-AzSynapseLinkedService** pobiera informacje o połączonych usługach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="3aeee-108">The **Get-AzSynapseLinkedService** cmdlet gets information about linked services in workspace.</span></span>
<span data-ttu-id="3aeee-109">Jeśli określisz nazwę usługi połączonej, to polecenie cmdlet pobiera informacje o tej połączonej usłudze.</span><span class="sxs-lookup"><span data-stu-id="3aeee-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="3aeee-110">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich połączonych usługach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="3aeee-110">If you do not specify a name, this cmdlet gets information about all the linked services in the workspace.</span></span>

## <span data-ttu-id="3aeee-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3aeee-111">EXAMPLES</span></span>

### <span data-ttu-id="3aeee-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3aeee-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="3aeee-113">To polecenie pobiera informacje o wszystkich połączonych usługach w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3aeee-113">This command gets information about all linked services in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="3aeee-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3aeee-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="3aeee-115">To polecenie pobiera informacje o połączonej usłudze o nazwie ContosoLinkedService w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3aeee-115">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="3aeee-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="3aeee-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="3aeee-117">To polecenie pobiera za pośrednictwem potoku informacje o połączonej usłudze ContosoLinkedService w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3aeee-117">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="3aeee-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3aeee-118">PARAMETERS</span></span>

### <span data-ttu-id="3aeee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aeee-119">-DefaultProfile</span></span>
<span data-ttu-id="3aeee-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3aeee-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3aeee-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3aeee-121">-Name</span></span>
<span data-ttu-id="3aeee-122">Nazwa połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="3aeee-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aeee-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3aeee-123">-WorkspaceName</span></span>
<span data-ttu-id="3aeee-124">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="3aeee-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3aeee-125">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3aeee-125">-WorkspaceObject</span></span>
<span data-ttu-id="3aeee-126">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="3aeee-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3aeee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aeee-127">CommonParameters</span></span>
<span data-ttu-id="3aeee-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aeee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aeee-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3aeee-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aeee-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3aeee-130">INPUTS</span></span>

### <span data-ttu-id="3aeee-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3aeee-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3aeee-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3aeee-132">OUTPUTS</span></span>

### <span data-ttu-id="3aeee-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="3aeee-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="3aeee-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3aeee-134">NOTES</span></span>

## <span data-ttu-id="3aeee-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3aeee-135">RELATED LINKS</span></span>

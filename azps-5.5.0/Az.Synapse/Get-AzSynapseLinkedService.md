---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
ms.openlocfilehash: d7f494b6ba943214106363a5b7dfe4dfb5cdd877
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197386"
---
# <span data-ttu-id="8b98d-101">Get-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="8b98d-101">Get-AzSynapseLinkedService</span></span>

## <span data-ttu-id="8b98d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b98d-102">SYNOPSIS</span></span>
<span data-ttu-id="8b98d-103">Pobiera informacje o usługach połączonych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="8b98d-103">Gets information about linked services in workspace.</span></span>

## <span data-ttu-id="8b98d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8b98d-104">SYNTAX</span></span>

### <span data-ttu-id="8b98d-105">GetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="8b98d-105">GetByName (Default)</span></span>
```
Get-AzSynapseLinkedService -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b98d-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="8b98d-106">GetByObject</span></span>
```
Get-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b98d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8b98d-107">DESCRIPTION</span></span>
<span data-ttu-id="8b98d-108">Polecenie **cmdlet Get-AzSynapseLinkedService** pobiera informacje o połączonych usługach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="8b98d-108">The **Get-AzSynapseLinkedService** cmdlet gets information about linked services in workspace.</span></span>
<span data-ttu-id="8b98d-109">Jeśli określisz nazwę usługi połączonej, to polecenie cmdlet pobiera informacje o tej połączonej usłudze.</span><span class="sxs-lookup"><span data-stu-id="8b98d-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="8b98d-110">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich połączonych usługach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="8b98d-110">If you do not specify a name, this cmdlet gets information about all the linked services in the workspace.</span></span>

## <span data-ttu-id="8b98d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8b98d-111">EXAMPLES</span></span>

### <span data-ttu-id="8b98d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8b98d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="8b98d-113">To polecenie pobiera informacje o wszystkich połączonych usługach w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="8b98d-113">This command gets information about all linked services in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="8b98d-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8b98d-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="8b98d-115">To polecenie pobiera informacje o połączonej usłudze o nazwie ContosoLinkedService w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="8b98d-115">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="8b98d-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="8b98d-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="8b98d-117">To polecenie pobiera informacje o połączonej usłudze o nazwie ContosoLinkedService w obszarze roboczym o nazwie ContosoWorkspace za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="8b98d-117">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="8b98d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b98d-118">PARAMETERS</span></span>

### <span data-ttu-id="8b98d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b98d-119">-DefaultProfile</span></span>
<span data-ttu-id="8b98d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b98d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b98d-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8b98d-121">-Name</span></span>
<span data-ttu-id="8b98d-122">Nazwa połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="8b98d-122">The linked service name.</span></span>

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

### <span data-ttu-id="8b98d-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8b98d-123">-WorkspaceName</span></span>
<span data-ttu-id="8b98d-124">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="8b98d-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8b98d-125">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8b98d-125">-WorkspaceObject</span></span>
<span data-ttu-id="8b98d-126">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="8b98d-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8b98d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b98d-127">CommonParameters</span></span>
<span data-ttu-id="8b98d-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b98d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b98d-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b98d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b98d-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b98d-130">INPUTS</span></span>

### <span data-ttu-id="8b98d-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8b98d-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8b98d-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b98d-132">OUTPUTS</span></span>

### <span data-ttu-id="8b98d-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="8b98d-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="8b98d-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8b98d-134">NOTES</span></span>

## <span data-ttu-id="8b98d-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b98d-135">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
ms.openlocfilehash: d7f494b6ba943214106363a5b7dfe4dfb5cdd877
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317526"
---
# <span data-ttu-id="5d6fd-101">Get-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="5d6fd-101">Get-AzSynapseLinkedService</span></span>

## <span data-ttu-id="5d6fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d6fd-102">SYNOPSIS</span></span>
<span data-ttu-id="5d6fd-103">Pobiera informacje o usługach połączonych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="5d6fd-103">Gets information about linked services in workspace.</span></span>

## <span data-ttu-id="5d6fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d6fd-104">SYNTAX</span></span>

### <span data-ttu-id="5d6fd-105">GetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5d6fd-105">GetByName (Default)</span></span>
```
Get-AzSynapseLinkedService -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d6fd-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="5d6fd-106">GetByObject</span></span>
```
Get-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d6fd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5d6fd-107">DESCRIPTION</span></span>
<span data-ttu-id="5d6fd-108">Polecenie cmdlet **Get-AzSynapseLinkedService** pobiera informacje o usługach połączonych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="5d6fd-108">The **Get-AzSynapseLinkedService** cmdlet gets information about linked services in workspace.</span></span>
<span data-ttu-id="5d6fd-109">Jeśli określisz nazwę połączonej usługi, to polecenie cmdlet będzie pobierać informacje dotyczące tej połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="5d6fd-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="5d6fd-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich usług połączonych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="5d6fd-110">If you do not specify a name, this cmdlet gets information about all the linked services in the workspace.</span></span>

## <span data-ttu-id="5d6fd-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d6fd-111">EXAMPLES</span></span>

### <span data-ttu-id="5d6fd-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5d6fd-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="5d6fd-113">To polecenie pobiera informacje dotyczące wszystkich usług połączonych w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="5d6fd-113">This command gets information about all linked services in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="5d6fd-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5d6fd-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="5d6fd-115">To polecenie pobiera informacje o połączonej usłudze o nazwie ContosoLinkedService w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="5d6fd-115">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="5d6fd-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="5d6fd-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="5d6fd-117">To polecenie pobiera informacje o połączonej usłudze o nazwie ContosoLinkedService w obszarze roboczym o nazwie ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="5d6fd-117">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="5d6fd-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d6fd-118">PARAMETERS</span></span>

### <span data-ttu-id="5d6fd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d6fd-119">-DefaultProfile</span></span>
<span data-ttu-id="5d6fd-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d6fd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d6fd-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5d6fd-121">-Name</span></span>
<span data-ttu-id="5d6fd-122">Nazwa połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="5d6fd-122">The linked service name.</span></span>

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

### <span data-ttu-id="5d6fd-123">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="5d6fd-123">-WorkspaceName</span></span>
<span data-ttu-id="5d6fd-124">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="5d6fd-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5d6fd-125">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="5d6fd-125">-WorkspaceObject</span></span>
<span data-ttu-id="5d6fd-126">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="5d6fd-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5d6fd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d6fd-127">CommonParameters</span></span>
<span data-ttu-id="5d6fd-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d6fd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d6fd-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d6fd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d6fd-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d6fd-130">INPUTS</span></span>

### <span data-ttu-id="5d6fd-131">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5d6fd-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5d6fd-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d6fd-132">OUTPUTS</span></span>

### <span data-ttu-id="5d6fd-133">Microsoft. Azure. Commands. Synapse. models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="5d6fd-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="5d6fd-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d6fd-134">NOTES</span></span>

## <span data-ttu-id="5d6fd-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d6fd-135">RELATED LINKS</span></span>

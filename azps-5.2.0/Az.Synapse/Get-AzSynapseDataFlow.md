---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 87627738967a5c3174020932e5c9e7b996980ee9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339274"
---
# <span data-ttu-id="87abb-101">Get-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="87abb-101">Get-AzSynapseDataFlow</span></span>

## <span data-ttu-id="87abb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87abb-102">SYNOPSIS</span></span>
<span data-ttu-id="87abb-103">Pobiera informacje o przepływach danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="87abb-103">Gets information about data flows in workspace.</span></span>

## <span data-ttu-id="87abb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87abb-104">SYNTAX</span></span>

### <span data-ttu-id="87abb-105">GetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="87abb-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87abb-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="87abb-106">GetByObject</span></span>
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87abb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="87abb-107">DESCRIPTION</span></span>
<span data-ttu-id="87abb-108">Polecenie cmdlet **Get-AzSynapseDataFlow** pobiera informacje o przepływach danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="87abb-108">The **Get-AzSynapseDataFlow** cmdlet gets information about data flows in workspace.</span></span>
<span data-ttu-id="87abb-109">Jeśli określisz nazwę przepływu danych, to polecenie cmdlet będzie pobierać informacje o przepływie danych.</span><span class="sxs-lookup"><span data-stu-id="87abb-109">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="87abb-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje o przepływach danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="87abb-110">If you do not specify a name, this cmdlet gets information about all the data flows in the workspace.</span></span>

## <span data-ttu-id="87abb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87abb-111">EXAMPLES</span></span>

### <span data-ttu-id="87abb-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="87abb-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="87abb-113">To polecenie pobiera informacje o przepływach danych w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="87abb-113">This command gets information about all data flows in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="87abb-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="87abb-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="87abb-115">To polecenie pobiera informacje o przepływie danych o nazwie ContosoDataFlow w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="87abb-115">This command gets information about the data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="87abb-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87abb-116">PARAMETERS</span></span>

### <span data-ttu-id="87abb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87abb-117">-DefaultProfile</span></span>
<span data-ttu-id="87abb-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="87abb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87abb-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="87abb-119">-Name</span></span>
<span data-ttu-id="87abb-120">Nazwa przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="87abb-120">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87abb-121">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="87abb-121">-WorkspaceName</span></span>
<span data-ttu-id="87abb-122">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="87abb-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="87abb-123">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="87abb-123">-WorkspaceObject</span></span>
<span data-ttu-id="87abb-124">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="87abb-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="87abb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87abb-125">CommonParameters</span></span>
<span data-ttu-id="87abb-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87abb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87abb-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87abb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87abb-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87abb-128">INPUTS</span></span>

### <span data-ttu-id="87abb-129">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="87abb-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="87abb-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87abb-130">OUTPUTS</span></span>

### <span data-ttu-id="87abb-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="87abb-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="87abb-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87abb-132">NOTES</span></span>

## <span data-ttu-id="87abb-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87abb-133">RELATED LINKS</span></span>

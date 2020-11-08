---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: 6304e730e6b3b0a4f8edc0f42fc024852acbfc12
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224114"
---
# <span data-ttu-id="78a25-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="78a25-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="78a25-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78a25-102">SYNOPSIS</span></span>
<span data-ttu-id="78a25-103">Sprawdza, czy istnieje Pula usługi Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="78a25-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="78a25-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78a25-104">SYNTAX</span></span>

### <span data-ttu-id="78a25-105">TestByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="78a25-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78a25-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78a25-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78a25-107">Opis</span><span class="sxs-lookup"><span data-stu-id="78a25-107">DESCRIPTION</span></span>
<span data-ttu-id="78a25-108">Polecenie cmdlet **test-AzSynapseSparkPool** sprawdza, czy istnieje Pula Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="78a25-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="78a25-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78a25-109">EXAMPLES</span></span>

### <span data-ttu-id="78a25-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="78a25-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="78a25-111">To polecenie sprawdza istnienie określonej puli platformy Spark.</span><span class="sxs-lookup"><span data-stu-id="78a25-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="78a25-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78a25-112">PARAMETERS</span></span>

### <span data-ttu-id="78a25-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78a25-113">-DefaultProfile</span></span>
<span data-ttu-id="78a25-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="78a25-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78a25-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="78a25-115">-Name</span></span>
<span data-ttu-id="78a25-116">Nazwa puli Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="78a25-116">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a25-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78a25-117">-ResourceGroupName</span></span>
<span data-ttu-id="78a25-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="78a25-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a25-119">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="78a25-119">-WorkspaceName</span></span>
<span data-ttu-id="78a25-120">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="78a25-120">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a25-121">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="78a25-121">-WorkspaceObject</span></span>
<span data-ttu-id="78a25-122">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="78a25-122">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78a25-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a25-123">CommonParameters</span></span>
<span data-ttu-id="78a25-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78a25-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a25-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78a25-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a25-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78a25-126">INPUTS</span></span>

### <span data-ttu-id="78a25-127">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="78a25-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="78a25-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78a25-128">OUTPUTS</span></span>

### <span data-ttu-id="78a25-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="78a25-129">System.Object</span></span>
## <span data-ttu-id="78a25-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78a25-130">NOTES</span></span>

## <span data-ttu-id="78a25-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78a25-131">RELATED LINKS</span></span>

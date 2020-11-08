---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: 6304e730e6b3b0a4f8edc0f42fc024852acbfc12
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94061934"
---
# <span data-ttu-id="911a6-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="911a6-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="911a6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="911a6-102">SYNOPSIS</span></span>
<span data-ttu-id="911a6-103">Sprawdza, czy istnieje Pula usługi Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="911a6-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="911a6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="911a6-104">SYNTAX</span></span>

### <span data-ttu-id="911a6-105">TestByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="911a6-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="911a6-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="911a6-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="911a6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="911a6-107">DESCRIPTION</span></span>
<span data-ttu-id="911a6-108">Polecenie cmdlet **test-AzSynapseSparkPool** sprawdza, czy istnieje Pula Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="911a6-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="911a6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="911a6-109">EXAMPLES</span></span>

### <span data-ttu-id="911a6-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="911a6-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="911a6-111">To polecenie sprawdza istnienie określonej puli platformy Spark.</span><span class="sxs-lookup"><span data-stu-id="911a6-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="911a6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="911a6-112">PARAMETERS</span></span>

### <span data-ttu-id="911a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="911a6-113">-DefaultProfile</span></span>
<span data-ttu-id="911a6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="911a6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="911a6-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="911a6-115">-Name</span></span>
<span data-ttu-id="911a6-116">Nazwa puli Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="911a6-116">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="911a6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="911a6-117">-ResourceGroupName</span></span>
<span data-ttu-id="911a6-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="911a6-118">Resource group name.</span></span>

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

### <span data-ttu-id="911a6-119">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="911a6-119">-WorkspaceName</span></span>
<span data-ttu-id="911a6-120">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="911a6-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="911a6-121">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="911a6-121">-WorkspaceObject</span></span>
<span data-ttu-id="911a6-122">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="911a6-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="911a6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="911a6-123">CommonParameters</span></span>
<span data-ttu-id="911a6-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="911a6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="911a6-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="911a6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="911a6-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="911a6-126">INPUTS</span></span>

### <span data-ttu-id="911a6-127">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="911a6-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="911a6-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="911a6-128">OUTPUTS</span></span>

### <span data-ttu-id="911a6-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="911a6-129">System.Object</span></span>
## <span data-ttu-id="911a6-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="911a6-130">NOTES</span></span>

## <span data-ttu-id="911a6-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="911a6-131">RELATED LINKS</span></span>

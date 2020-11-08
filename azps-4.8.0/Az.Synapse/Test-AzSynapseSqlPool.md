---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: d07ec757fd5ab589de6234caac23992d6ff320fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94061933"
---
# <span data-ttu-id="1535d-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1535d-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="1535d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1535d-102">SYNOPSIS</span></span>
<span data-ttu-id="1535d-103">Sprawdza, czy istnieje Pula SQL analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="1535d-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1535d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1535d-104">SYNTAX</span></span>

### <span data-ttu-id="1535d-105">TestByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1535d-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1535d-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1535d-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1535d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1535d-107">DESCRIPTION</span></span>
<span data-ttu-id="1535d-108">Polecenie cmdlet **test-AzSynapseSqlPool** sprawdza istnienie puli Synapse analiz SQL.</span><span class="sxs-lookup"><span data-stu-id="1535d-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1535d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1535d-109">EXAMPLES</span></span>

### <span data-ttu-id="1535d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1535d-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="1535d-111">To polecenie sprawdza, czy istnieje określona Pula SQL.</span><span class="sxs-lookup"><span data-stu-id="1535d-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="1535d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1535d-112">PARAMETERS</span></span>

### <span data-ttu-id="1535d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1535d-113">-DefaultProfile</span></span>
<span data-ttu-id="1535d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1535d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1535d-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1535d-115">-Name</span></span>
<span data-ttu-id="1535d-116">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="1535d-116">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="1535d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1535d-117">-ResourceGroupName</span></span>
<span data-ttu-id="1535d-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1535d-118">Resource group name.</span></span>

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

### <span data-ttu-id="1535d-119">-Version</span><span class="sxs-lookup"><span data-stu-id="1535d-119">-Version</span></span>
<span data-ttu-id="1535d-120">Wersja puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="1535d-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="1535d-121">Na przykład 2 lub 3.</span><span class="sxs-lookup"><span data-stu-id="1535d-121">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1535d-122">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="1535d-122">-WorkspaceName</span></span>
<span data-ttu-id="1535d-123">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="1535d-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1535d-124">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="1535d-124">-WorkspaceObject</span></span>
<span data-ttu-id="1535d-125">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="1535d-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1535d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1535d-126">CommonParameters</span></span>
<span data-ttu-id="1535d-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1535d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1535d-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1535d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1535d-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1535d-129">INPUTS</span></span>

### <span data-ttu-id="1535d-130">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1535d-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1535d-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1535d-131">OUTPUTS</span></span>

### <span data-ttu-id="1535d-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="1535d-132">System.Object</span></span>
## <span data-ttu-id="1535d-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1535d-133">NOTES</span></span>

## <span data-ttu-id="1535d-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1535d-134">RELATED LINKS</span></span>

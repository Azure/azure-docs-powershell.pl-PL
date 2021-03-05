---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: 8d0bd6f046bbff99d93b0ed5dc7385d8ec772811
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005425"
---
# <span data-ttu-id="6180b-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="6180b-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="6180b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6180b-102">SYNOPSIS</span></span>
<span data-ttu-id="6180b-103">Usuwanie pełnego typu węzła z klastra.</span><span class="sxs-lookup"><span data-stu-id="6180b-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="6180b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6180b-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6180b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6180b-105">DESCRIPTION</span></span>
<span data-ttu-id="6180b-106">Użyj właściwości **Remove-AzServiceFabricNodeType,** aby usunąć wszystkie węzły z określonego typu węzła i typu węzła z klastry.</span><span class="sxs-lookup"><span data-stu-id="6180b-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="6180b-107">Tego polecenia nie można użyć do usunięcia typu węzła podstawowego.</span><span class="sxs-lookup"><span data-stu-id="6180b-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="6180b-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6180b-108">EXAMPLES</span></span>

### <span data-ttu-id="6180b-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6180b-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="6180b-110">To polecenie spowoduje usunięcie typu NodeType 'nt1' z klastrowania.</span><span class="sxs-lookup"><span data-stu-id="6180b-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="6180b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6180b-111">PARAMETERS</span></span>

### <span data-ttu-id="6180b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6180b-112">-DefaultProfile</span></span>
<span data-ttu-id="6180b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6180b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6180b-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6180b-114">-Name</span></span>
<span data-ttu-id="6180b-115">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="6180b-115">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6180b-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="6180b-116">-NodeType</span></span>
<span data-ttu-id="6180b-117">Nazwa typu węzła</span><span class="sxs-lookup"><span data-stu-id="6180b-117">The node type name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6180b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6180b-118">-ResourceGroupName</span></span>
<span data-ttu-id="6180b-119">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6180b-119">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6180b-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6180b-120">-Confirm</span></span>
<span data-ttu-id="6180b-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6180b-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6180b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6180b-122">-WhatIf</span></span>
<span data-ttu-id="6180b-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6180b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6180b-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6180b-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6180b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6180b-125">CommonParameters</span></span>
<span data-ttu-id="6180b-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6180b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6180b-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6180b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6180b-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6180b-128">INPUTS</span></span>

### <span data-ttu-id="6180b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="6180b-129">System.String</span></span>

## <span data-ttu-id="6180b-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6180b-130">OUTPUTS</span></span>

### <span data-ttu-id="6180b-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="6180b-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="6180b-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6180b-132">NOTES</span></span>

## <span data-ttu-id="6180b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6180b-133">RELATED LINKS</span></span>

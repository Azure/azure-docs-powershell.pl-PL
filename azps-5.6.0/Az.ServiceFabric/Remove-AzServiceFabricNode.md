---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: ba5400a35939a221b19ba144b35b0f2a53f6dbe9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005434"
---
# <span data-ttu-id="afb11-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="afb11-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="afb11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afb11-102">SYNOPSIS</span></span>
<span data-ttu-id="afb11-103">Usuwanie węzłów z określonego typu węzła z klastrów.</span><span class="sxs-lookup"><span data-stu-id="afb11-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="afb11-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="afb11-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afb11-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="afb11-105">DESCRIPTION</span></span>
<span data-ttu-id="afb11-106">Użyj **funkcji Remove-AzServiceFabricNode,** aby usunąć węzły z określonego typu węzła z klastry.</span><span class="sxs-lookup"><span data-stu-id="afb11-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="afb11-107">Usuwanie będzie kontynuowane tylko wtedy, gdy spełnia ono metrykę kondycji klastrów.</span><span class="sxs-lookup"><span data-stu-id="afb11-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="afb11-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="afb11-108">EXAMPLES</span></span>

### <span data-ttu-id="afb11-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="afb11-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="afb11-110">To polecenie spowoduje usunięcie 2 węzłów z typu NodeType 'nt1'.</span><span class="sxs-lookup"><span data-stu-id="afb11-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="afb11-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afb11-111">PARAMETERS</span></span>

### <span data-ttu-id="afb11-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afb11-112">-DefaultProfile</span></span>
<span data-ttu-id="afb11-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="afb11-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afb11-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="afb11-114">-Name</span></span>
<span data-ttu-id="afb11-115">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="afb11-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="afb11-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="afb11-116">-NodeType</span></span>
<span data-ttu-id="afb11-117">Nazwa typu węzła</span><span class="sxs-lookup"><span data-stu-id="afb11-117">Node type name</span></span>

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

### <span data-ttu-id="afb11-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="afb11-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="afb11-119">Liczba węzłów do dodania</span><span class="sxs-lookup"><span data-stu-id="afb11-119">The number of nodes to add</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Number

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afb11-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afb11-120">-ResourceGroupName</span></span>
<span data-ttu-id="afb11-121">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="afb11-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="afb11-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="afb11-122">-Confirm</span></span>
<span data-ttu-id="afb11-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="afb11-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afb11-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afb11-124">-WhatIf</span></span>
<span data-ttu-id="afb11-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afb11-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afb11-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="afb11-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afb11-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb11-127">CommonParameters</span></span>
<span data-ttu-id="afb11-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afb11-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb11-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="afb11-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb11-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="afb11-130">INPUTS</span></span>

### <span data-ttu-id="afb11-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="afb11-131">System.Int32</span></span>

### <span data-ttu-id="afb11-132">System.String</span><span class="sxs-lookup"><span data-stu-id="afb11-132">System.String</span></span>

## <span data-ttu-id="afb11-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="afb11-133">OUTPUTS</span></span>

### <span data-ttu-id="afb11-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="afb11-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="afb11-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="afb11-135">NOTES</span></span>

## <span data-ttu-id="afb11-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="afb11-136">RELATED LINKS</span></span>

[<span data-ttu-id="afb11-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="afb11-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)

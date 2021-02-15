---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: 41c78b659a39d3df52185eeb2b67e4c921f22b45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242162"
---
# <span data-ttu-id="f066f-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="f066f-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="f066f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f066f-102">SYNOPSIS</span></span>
<span data-ttu-id="f066f-103">Dodaj węzły do określonego typu węzła w klastrze.</span><span class="sxs-lookup"><span data-stu-id="f066f-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="f066f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f066f-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f066f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f066f-105">DESCRIPTION</span></span>
<span data-ttu-id="f066f-106">Użyj **funkcji Add-AzServiceFabricNode,** aby dodać węzły do określonego typu węzła.</span><span class="sxs-lookup"><span data-stu-id="f066f-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="f066f-107">Wystarczy określić liczbę węzłów, które chcesz dodać do typu węzła.</span><span class="sxs-lookup"><span data-stu-id="f066f-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="f066f-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f066f-108">EXAMPLES</span></span>

### <span data-ttu-id="f066f-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f066f-109">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="f066f-110">To polecenie spowoduje dodanie 2 węzłów do typu węzła "n1".</span><span class="sxs-lookup"><span data-stu-id="f066f-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="f066f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f066f-111">PARAMETERS</span></span>

### <span data-ttu-id="f066f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f066f-112">-DefaultProfile</span></span>
<span data-ttu-id="f066f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f066f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f066f-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f066f-114">-Name</span></span>
<span data-ttu-id="f066f-115">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="f066f-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="f066f-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="f066f-116">-NodeType</span></span>
<span data-ttu-id="f066f-117">Nazwa typu węzła</span><span class="sxs-lookup"><span data-stu-id="f066f-117">Node type name</span></span>

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

### <span data-ttu-id="f066f-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="f066f-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="f066f-119">Liczba węzłów do dodania</span><span class="sxs-lookup"><span data-stu-id="f066f-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="f066f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f066f-120">-ResourceGroupName</span></span>
<span data-ttu-id="f066f-121">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f066f-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="f066f-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f066f-122">-Confirm</span></span>
<span data-ttu-id="f066f-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f066f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f066f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f066f-124">-WhatIf</span></span>
<span data-ttu-id="f066f-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f066f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f066f-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f066f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f066f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f066f-127">CommonParameters</span></span>
<span data-ttu-id="f066f-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f066f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f066f-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f066f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f066f-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f066f-130">INPUTS</span></span>

### <span data-ttu-id="f066f-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f066f-131">System.Int32</span></span>

### <span data-ttu-id="f066f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f066f-132">System.String</span></span>

## <span data-ttu-id="f066f-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f066f-133">OUTPUTS</span></span>

### <span data-ttu-id="f066f-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="f066f-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="f066f-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f066f-135">NOTES</span></span>

## <span data-ttu-id="f066f-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f066f-136">RELATED LINKS</span></span>

[<span data-ttu-id="f066f-137">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="f066f-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)

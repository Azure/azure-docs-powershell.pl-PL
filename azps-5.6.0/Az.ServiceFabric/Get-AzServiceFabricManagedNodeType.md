---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 15ba499908a4a631a22f9064b1938d3b32fdafd5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955626"
---
# <span data-ttu-id="0c3f6-101">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="0c3f6-101">Get-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="0c3f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c3f6-102">SYNOPSIS</span></span>
<span data-ttu-id="0c3f6-103">Pobierz szczegóły zasobu typu węzła zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="0c3f6-103">Get the managed node type resource details.</span></span>

## <span data-ttu-id="0c3f6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0c3f6-104">SYNTAX</span></span>

### <span data-ttu-id="0c3f6-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="0c3f6-105">ByName (Default)</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c3f6-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0c3f6-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c3f6-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0c3f6-107">DESCRIPTION</span></span>
<span data-ttu-id="0c3f6-108">Pobierz szczegóły zasobu typu węzła zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="0c3f6-108">Get the managed node type resource details.</span></span>

## <span data-ttu-id="0c3f6-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0c3f6-109">EXAMPLES</span></span>

### <span data-ttu-id="0c3f6-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0c3f6-110">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName
```

<span data-ttu-id="0c3f6-111">Pobierz szczegóły typu węzła.</span><span class="sxs-lookup"><span data-stu-id="0c3f6-111">Get node type details.</span></span>

### <span data-ttu-id="0c3f6-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0c3f6-112">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName
```

<span data-ttu-id="0c3f6-113">Pobierz listę typów węzłów w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="0c3f6-113">Get list of node types under the specified cluster.</span></span>

## <span data-ttu-id="0c3f6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c3f6-114">PARAMETERS</span></span>

### <span data-ttu-id="0c3f6-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0c3f6-115">-ClusterName</span></span>
<span data-ttu-id="0c3f6-116">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="0c3f6-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c3f6-117">-DefaultProfile</span></span>
<span data-ttu-id="0c3f6-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c3f6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c3f6-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0c3f6-119">-Name</span></span>
<span data-ttu-id="0c3f6-120">Określ nazwę typu węzła.</span><span class="sxs-lookup"><span data-stu-id="0c3f6-120">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3f6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c3f6-121">-ResourceGroupName</span></span>
<span data-ttu-id="0c3f6-122">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0c3f6-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0c3f6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c3f6-123">CommonParameters</span></span>
<span data-ttu-id="0c3f6-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c3f6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c3f6-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c3f6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c3f6-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c3f6-126">INPUTS</span></span>

### <span data-ttu-id="0c3f6-127">System.String</span><span class="sxs-lookup"><span data-stu-id="0c3f6-127">System.String</span></span>

## <span data-ttu-id="0c3f6-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c3f6-128">OUTPUTS</span></span>

### <span data-ttu-id="0c3f6-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="0c3f6-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="0c3f6-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0c3f6-130">NOTES</span></span>

## <span data-ttu-id="0c3f6-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c3f6-131">RELATED LINKS</span></span>

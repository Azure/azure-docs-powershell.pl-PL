---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 6cca65a061e54bbd08327fc054a0c6b55d8c98f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502821"
---
# <span data-ttu-id="78709-101">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="78709-101">Get-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="78709-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78709-102">SYNOPSIS</span></span>
<span data-ttu-id="78709-103">Pobierz szczegóły zasobu typu zarządzanego węzła.</span><span class="sxs-lookup"><span data-stu-id="78709-103">Get the managed node type resource details.</span></span>

## <span data-ttu-id="78709-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78709-104">SYNTAX</span></span>

### <span data-ttu-id="78709-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="78709-105">ByName (Default)</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78709-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="78709-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78709-107">Opis</span><span class="sxs-lookup"><span data-stu-id="78709-107">DESCRIPTION</span></span>
<span data-ttu-id="78709-108">Pobierz szczegóły zasobu typu zarządzanego węzła.</span><span class="sxs-lookup"><span data-stu-id="78709-108">Get the managed node type resource details.</span></span>

## <span data-ttu-id="78709-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78709-109">EXAMPLES</span></span>

### <span data-ttu-id="78709-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="78709-110">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName
```

<span data-ttu-id="78709-111">Pobierz szczegóły typu węzła.</span><span class="sxs-lookup"><span data-stu-id="78709-111">Get node type details.</span></span>

### <span data-ttu-id="78709-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="78709-112">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName
```

<span data-ttu-id="78709-113">Pobieranie listy typów węzłów w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="78709-113">Get list of node types under the specified cluster.</span></span>

## <span data-ttu-id="78709-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78709-114">PARAMETERS</span></span>

### <span data-ttu-id="78709-115">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="78709-115">-ClusterName</span></span>
<span data-ttu-id="78709-116">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="78709-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="78709-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78709-117">-DefaultProfile</span></span>
<span data-ttu-id="78709-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="78709-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78709-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="78709-119">-Name</span></span>
<span data-ttu-id="78709-120">Określ nazwę typu węzła.</span><span class="sxs-lookup"><span data-stu-id="78709-120">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="78709-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78709-121">-ResourceGroupName</span></span>
<span data-ttu-id="78709-122">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="78709-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="78709-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78709-123">CommonParameters</span></span>
<span data-ttu-id="78709-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78709-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78709-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78709-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78709-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78709-126">INPUTS</span></span>

### <span data-ttu-id="78709-127">System. String</span><span class="sxs-lookup"><span data-stu-id="78709-127">System.String</span></span>

## <span data-ttu-id="78709-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78709-128">OUTPUTS</span></span>

### <span data-ttu-id="78709-129">Microsoft. Azure. Commands. servicefabric. MODELES. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="78709-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="78709-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78709-130">NOTES</span></span>

## <span data-ttu-id="78709-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78709-131">RELATED LINKS</span></span>

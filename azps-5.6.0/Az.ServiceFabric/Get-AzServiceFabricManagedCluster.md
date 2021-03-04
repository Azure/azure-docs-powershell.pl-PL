---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 5a67faaf48d96a93fe1bc3e6380abb4fe6d03d98
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955633"
---
# <span data-ttu-id="301b0-101">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="301b0-101">Get-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="301b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="301b0-102">SYNOPSIS</span></span>
<span data-ttu-id="301b0-103">Uzyskaj szczegółowe informacje dotyczące zarządzanego zasobu klastrów.</span><span class="sxs-lookup"><span data-stu-id="301b0-103">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="301b0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="301b0-104">SYNTAX</span></span>

### <span data-ttu-id="301b0-105">BySubscription (Default)</span><span class="sxs-lookup"><span data-stu-id="301b0-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricManagedCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="301b0-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="301b0-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="301b0-107">ByName</span><span class="sxs-lookup"><span data-stu-id="301b0-107">ByName</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="301b0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="301b0-108">DESCRIPTION</span></span>
<span data-ttu-id="301b0-109">Uzyskaj szczegółowe informacje dotyczące zarządzanego zasobu klastrów.</span><span class="sxs-lookup"><span data-stu-id="301b0-109">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="301b0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="301b0-110">EXAMPLES</span></span>

### <span data-ttu-id="301b0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="301b0-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
```

<span data-ttu-id="301b0-112">Uzyskaj szczegółowe informacje o klastrze.</span><span class="sxs-lookup"><span data-stu-id="301b0-112">Get cluster details.</span></span>

### <span data-ttu-id="301b0-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="301b0-113">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName
```

<span data-ttu-id="301b0-114">Uzyskiwanie listy klastrów w ramach określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="301b0-114">Get list of clusters under the specified resource group.</span></span>

### <span data-ttu-id="301b0-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="301b0-115">Example 3</span></span>
```powershell
Get-AzServiceFabricManagedCluster
```

<span data-ttu-id="301b0-116">Uzyskaj listę klastrów w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="301b0-116">Get list of clusters under the current subscription.</span></span>

## <span data-ttu-id="301b0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="301b0-117">PARAMETERS</span></span>

### <span data-ttu-id="301b0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="301b0-118">-DefaultProfile</span></span>
<span data-ttu-id="301b0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="301b0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="301b0-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="301b0-120">-Name</span></span>
<span data-ttu-id="301b0-121">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="301b0-121">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="301b0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="301b0-122">-ResourceGroupName</span></span>
<span data-ttu-id="301b0-123">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="301b0-123">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="301b0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="301b0-124">CommonParameters</span></span>
<span data-ttu-id="301b0-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="301b0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="301b0-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="301b0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="301b0-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="301b0-127">INPUTS</span></span>

### <span data-ttu-id="301b0-128">System.String</span><span class="sxs-lookup"><span data-stu-id="301b0-128">System.String</span></span>

## <span data-ttu-id="301b0-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="301b0-129">OUTPUTS</span></span>

### <span data-ttu-id="301b0-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="301b0-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="301b0-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="301b0-131">NOTES</span></span>

## <span data-ttu-id="301b0-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="301b0-132">RELATED LINKS</span></span>

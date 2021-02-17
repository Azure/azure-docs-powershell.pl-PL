---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
ms.openlocfilehash: c81199bb78a64ac2ed32a21e0f3822093a2b2b14
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242114"
---
# <span data-ttu-id="203e1-101">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="203e1-101">Get-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="203e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="203e1-102">SYNOPSIS</span></span>
<span data-ttu-id="203e1-103">Uzyskaj szczegółowe informacje dotyczące zarządzanego zasobu klastrów.</span><span class="sxs-lookup"><span data-stu-id="203e1-103">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="203e1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="203e1-104">SYNTAX</span></span>

### <span data-ttu-id="203e1-105">BySubscription (Default)</span><span class="sxs-lookup"><span data-stu-id="203e1-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricManagedCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="203e1-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="203e1-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="203e1-107">ByName</span><span class="sxs-lookup"><span data-stu-id="203e1-107">ByName</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="203e1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="203e1-108">DESCRIPTION</span></span>
<span data-ttu-id="203e1-109">Uzyskaj szczegółowe informacje dotyczące zarządzanego zasobu klastrów.</span><span class="sxs-lookup"><span data-stu-id="203e1-109">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="203e1-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="203e1-110">EXAMPLES</span></span>

### <span data-ttu-id="203e1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="203e1-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
```

<span data-ttu-id="203e1-112">Uzyskaj szczegółowe informacje o klastrze.</span><span class="sxs-lookup"><span data-stu-id="203e1-112">Get cluster details.</span></span>

### <span data-ttu-id="203e1-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="203e1-113">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName
```

<span data-ttu-id="203e1-114">Uzyskiwanie listy klastrów w ramach określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="203e1-114">Get list of clusters under the specified resource group.</span></span>

### <span data-ttu-id="203e1-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="203e1-115">Example 3</span></span>
```powershell
Get-AzServiceFabricManagedCluster
```

<span data-ttu-id="203e1-116">Uzyskaj listę klastrów w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="203e1-116">Get list of clusters under the current subscription.</span></span>

## <span data-ttu-id="203e1-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="203e1-117">PARAMETERS</span></span>

### <span data-ttu-id="203e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="203e1-118">-DefaultProfile</span></span>
<span data-ttu-id="203e1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="203e1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="203e1-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="203e1-120">-Name</span></span>
<span data-ttu-id="203e1-121">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="203e1-121">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="203e1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="203e1-122">-ResourceGroupName</span></span>
<span data-ttu-id="203e1-123">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="203e1-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="203e1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="203e1-124">CommonParameters</span></span>
<span data-ttu-id="203e1-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="203e1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="203e1-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="203e1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="203e1-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="203e1-127">INPUTS</span></span>

### <span data-ttu-id="203e1-128">System.String</span><span class="sxs-lookup"><span data-stu-id="203e1-128">System.String</span></span>

## <span data-ttu-id="203e1-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="203e1-129">OUTPUTS</span></span>

### <span data-ttu-id="203e1-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="203e1-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="203e1-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="203e1-131">NOTES</span></span>

## <span data-ttu-id="203e1-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="203e1-132">RELATED LINKS</span></span>

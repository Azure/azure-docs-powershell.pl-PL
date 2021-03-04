---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: 4695502bddb11b1b033b75057ba5ff3d2bf96b74
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955642"
---
# <span data-ttu-id="45679-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="45679-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="45679-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45679-102">SYNOPSIS</span></span>
<span data-ttu-id="45679-103">Uzyskaj szczegółowe informacje o zasobach klastrów.</span><span class="sxs-lookup"><span data-stu-id="45679-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="45679-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="45679-104">SYNTAX</span></span>

### <span data-ttu-id="45679-105">BySubscription (Default)</span><span class="sxs-lookup"><span data-stu-id="45679-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45679-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="45679-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="45679-107">ByName</span><span class="sxs-lookup"><span data-stu-id="45679-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45679-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="45679-108">DESCRIPTION</span></span>
<span data-ttu-id="45679-109">Usługa **Get-AzServiceFabricCluster** otrzyma szczegółowe informacje o zasobach klastrów.</span><span class="sxs-lookup"><span data-stu-id="45679-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="45679-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="45679-110">EXAMPLES</span></span>

### <span data-ttu-id="45679-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="45679-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="45679-112">To polecenie spowoduje uzyskiwanie szczegółów zasobów klastrów dla grupowania "myCluster".</span><span class="sxs-lookup"><span data-stu-id="45679-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="45679-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45679-113">PARAMETERS</span></span>

### <span data-ttu-id="45679-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45679-114">-DefaultProfile</span></span>
<span data-ttu-id="45679-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="45679-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45679-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="45679-116">-Name</span></span>
<span data-ttu-id="45679-117">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="45679-117">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="45679-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45679-118">-ResourceGroupName</span></span>
<span data-ttu-id="45679-119">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="45679-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="45679-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45679-120">CommonParameters</span></span>
<span data-ttu-id="45679-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45679-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45679-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45679-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45679-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45679-123">INPUTS</span></span>

### <span data-ttu-id="45679-124">System.String</span><span class="sxs-lookup"><span data-stu-id="45679-124">System.String</span></span>

## <span data-ttu-id="45679-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45679-125">OUTPUTS</span></span>

### <span data-ttu-id="45679-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="45679-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="45679-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="45679-127">NOTES</span></span>

## <span data-ttu-id="45679-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45679-128">RELATED LINKS</span></span>

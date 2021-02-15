---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: 43e2ae9426d80b7762fb8afe7b9c57a53a232f8a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197843"
---
# <span data-ttu-id="4a686-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="4a686-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="4a686-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a686-102">SYNOPSIS</span></span>
<span data-ttu-id="4a686-103">Pobierz szczegóły zasobów klastrów.</span><span class="sxs-lookup"><span data-stu-id="4a686-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="4a686-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4a686-104">SYNTAX</span></span>

### <span data-ttu-id="4a686-105">BySubscription (Default)</span><span class="sxs-lookup"><span data-stu-id="4a686-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a686-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4a686-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a686-107">ByName</span><span class="sxs-lookup"><span data-stu-id="4a686-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a686-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4a686-108">DESCRIPTION</span></span>
<span data-ttu-id="4a686-109">Usługa **Get-AzServiceFabricCluster** otrzyma szczegółowe informacje o zasobach klastrów.</span><span class="sxs-lookup"><span data-stu-id="4a686-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="4a686-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4a686-110">EXAMPLES</span></span>

### <span data-ttu-id="4a686-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4a686-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="4a686-112">To polecenie spowoduje uzyskiwanie szczegółów zasobów klastrów dla grupowania "myCluster".</span><span class="sxs-lookup"><span data-stu-id="4a686-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="4a686-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a686-113">PARAMETERS</span></span>

### <span data-ttu-id="4a686-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a686-114">-DefaultProfile</span></span>
<span data-ttu-id="4a686-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a686-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a686-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4a686-116">-Name</span></span>
<span data-ttu-id="4a686-117">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="4a686-117">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="4a686-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a686-118">-ResourceGroupName</span></span>
<span data-ttu-id="4a686-119">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4a686-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="4a686-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a686-120">CommonParameters</span></span>
<span data-ttu-id="4a686-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a686-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a686-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a686-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a686-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a686-123">INPUTS</span></span>

### <span data-ttu-id="4a686-124">System.String</span><span class="sxs-lookup"><span data-stu-id="4a686-124">System.String</span></span>

## <span data-ttu-id="4a686-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4a686-125">OUTPUTS</span></span>

### <span data-ttu-id="4a686-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="4a686-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="4a686-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4a686-127">NOTES</span></span>

## <span data-ttu-id="4a686-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a686-128">RELATED LINKS</span></span>

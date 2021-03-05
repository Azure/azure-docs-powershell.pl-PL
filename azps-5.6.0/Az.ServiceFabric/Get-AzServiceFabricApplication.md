---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: 346664d4714836b9965088d946262257e76747e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963617"
---
# <span data-ttu-id="b2326-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b2326-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="b2326-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2326-102">SYNOPSIS</span></span>
<span data-ttu-id="b2326-103">Uzyskaj szczegóły aplikacji Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="b2326-103">Get Service Fabric application details.</span></span> <span data-ttu-id="b2326-104">Obsługuje tylko ARM wdrożonych aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b2326-104">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="b2326-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b2326-105">SYNTAX</span></span>

### <span data-ttu-id="b2326-106">ByResourceGroupAndCluster (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b2326-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2326-107">ByName</span><span class="sxs-lookup"><span data-stu-id="b2326-107">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2326-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b2326-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2326-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="b2326-109">DESCRIPTION</span></span>
<span data-ttu-id="b2326-110">To polecenie cmdlet pobiera szczegóły aplikacji w określonej grupie zasobów i klastrze.</span><span class="sxs-lookup"><span data-stu-id="b2326-110">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="b2326-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b2326-111">EXAMPLES</span></span>

### <span data-ttu-id="b2326-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b2326-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="b2326-113">W tym przykładzie są uzyskujene szczegóły zasobu aplikacji "testApp".</span><span class="sxs-lookup"><span data-stu-id="b2326-113">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="b2326-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b2326-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="b2326-115">W tym przykładzie zostanie wyświetlona lista aplikacji w obszarze "testCluster".</span><span class="sxs-lookup"><span data-stu-id="b2326-115">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="b2326-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2326-116">PARAMETERS</span></span>

### <span data-ttu-id="b2326-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b2326-117">-ClusterName</span></span>
<span data-ttu-id="b2326-118">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="b2326-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2326-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2326-119">-DefaultProfile</span></span>
<span data-ttu-id="b2326-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2326-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2326-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b2326-121">-Name</span></span>
<span data-ttu-id="b2326-122">Określ nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b2326-122">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2326-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2326-123">-ResourceGroupName</span></span>
<span data-ttu-id="b2326-124">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b2326-124">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2326-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2326-125">-ResourceId</span></span>
<span data-ttu-id="b2326-126">Arm ResourceId aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b2326-126">Arm ResourceId of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2326-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2326-127">CommonParameters</span></span>
<span data-ttu-id="b2326-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2326-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2326-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2326-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2326-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2326-130">INPUTS</span></span>

### <span data-ttu-id="b2326-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b2326-131">System.String</span></span>

## <span data-ttu-id="b2326-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2326-132">OUTPUTS</span></span>

### <span data-ttu-id="b2326-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="b2326-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="b2326-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b2326-134">NOTES</span></span>

## <span data-ttu-id="b2326-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2326-135">RELATED LINKS</span></span>

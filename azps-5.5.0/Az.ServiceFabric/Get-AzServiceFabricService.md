---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: d927ef9a8a1c3ef97976911b122f22e1948f2996
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197834"
---
# <span data-ttu-id="cdf0f-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="cdf0f-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="cdf0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdf0f-102">SYNOPSIS</span></span>
<span data-ttu-id="cdf0f-103">Uzyskaj szczegóły usługi Service Fabric w ramach określonej aplikacji i klastra.</span><span class="sxs-lookup"><span data-stu-id="cdf0f-103">Get Service Fabric service details under the specified application and cluster.</span></span> <span data-ttu-id="cdf0f-104">Obsługuje tylko ARM wdrożonych usług.</span><span class="sxs-lookup"><span data-stu-id="cdf0f-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="cdf0f-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cdf0f-105">SYNTAX</span></span>

### <span data-ttu-id="cdf0f-106">ByResourceGroupAndCluster (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="cdf0f-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdf0f-107">ByName</span><span class="sxs-lookup"><span data-stu-id="cdf0f-107">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdf0f-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cdf0f-108">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdf0f-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="cdf0f-109">DESCRIPTION</span></span>
<span data-ttu-id="cdf0f-110">To polecenie cmdlet pobierze szczegóły usługi w określonej aplikacji i klastrze.</span><span class="sxs-lookup"><span data-stu-id="cdf0f-110">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="cdf0f-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cdf0f-111">EXAMPLES</span></span>

### <span data-ttu-id="cdf0f-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cdf0f-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="cdf0f-113">W tym przykładzie są pozysłowe szczegóły zasobu usługi "testApp~testService".</span><span class="sxs-lookup"><span data-stu-id="cdf0f-113">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="cdf0f-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cdf0f-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="cdf0f-115">W tym przykładzie zostanie wyświetlona lista usług w obszarze aplikacji "testApp".</span><span class="sxs-lookup"><span data-stu-id="cdf0f-115">This example gets a list of the services under the application "testApp".</span></span>

## <span data-ttu-id="cdf0f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdf0f-116">PARAMETERS</span></span>

### <span data-ttu-id="cdf0f-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="cdf0f-117">-ApplicationName</span></span>
<span data-ttu-id="cdf0f-118">Określ nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cdf0f-118">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdf0f-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cdf0f-119">-ClusterName</span></span>
<span data-ttu-id="cdf0f-120">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="cdf0f-120">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="cdf0f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdf0f-121">-DefaultProfile</span></span>
<span data-ttu-id="cdf0f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cdf0f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdf0f-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cdf0f-123">-Name</span></span>
<span data-ttu-id="cdf0f-124">Określ nazwę usługi.</span><span class="sxs-lookup"><span data-stu-id="cdf0f-124">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdf0f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdf0f-125">-ResourceGroupName</span></span>
<span data-ttu-id="cdf0f-126">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cdf0f-126">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="cdf0f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cdf0f-127">-ResourceId</span></span>
<span data-ttu-id="cdf0f-128">Arm ResourceId usługi.</span><span class="sxs-lookup"><span data-stu-id="cdf0f-128">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="cdf0f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdf0f-129">CommonParameters</span></span>
<span data-ttu-id="cdf0f-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdf0f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdf0f-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cdf0f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdf0f-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdf0f-132">INPUTS</span></span>

### <span data-ttu-id="cdf0f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="cdf0f-133">System.String</span></span>

## <span data-ttu-id="cdf0f-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdf0f-134">OUTPUTS</span></span>

### <span data-ttu-id="cdf0f-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="cdf0f-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="cdf0f-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cdf0f-136">NOTES</span></span>

## <span data-ttu-id="cdf0f-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cdf0f-137">RELATED LINKS</span></span>

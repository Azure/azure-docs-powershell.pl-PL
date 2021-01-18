---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: d927ef9a8a1c3ef97976911b122f22e1948f2996
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502819"
---
# <span data-ttu-id="72f1b-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="72f1b-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="72f1b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72f1b-102">SYNOPSIS</span></span>
<span data-ttu-id="72f1b-103">Pobierz szczegóły usługi programu Service Fabric w określonej aplikacji i klastrze.</span><span class="sxs-lookup"><span data-stu-id="72f1b-103">Get Service Fabric service details under the specified application and cluster.</span></span> <span data-ttu-id="72f1b-104">Obsługuje tylko usługi wdrażania ARM.</span><span class="sxs-lookup"><span data-stu-id="72f1b-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="72f1b-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72f1b-105">SYNTAX</span></span>

### <span data-ttu-id="72f1b-106">ByResourceGroupAndCluster (domyślny)</span><span class="sxs-lookup"><span data-stu-id="72f1b-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72f1b-107">ByName</span><span class="sxs-lookup"><span data-stu-id="72f1b-107">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72f1b-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="72f1b-108">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72f1b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="72f1b-109">DESCRIPTION</span></span>
<span data-ttu-id="72f1b-110">To polecenie cmdlet spowoduje wyświetlenie szczegółowych informacji o usłudze w określonej aplikacji i klastrze.</span><span class="sxs-lookup"><span data-stu-id="72f1b-110">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="72f1b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72f1b-111">EXAMPLES</span></span>

### <span data-ttu-id="72f1b-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="72f1b-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="72f1b-113">W tym przykładzie są pobierane dane zasobu usługi dotyczące usługi "testApp ~ testService".</span><span class="sxs-lookup"><span data-stu-id="72f1b-113">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="72f1b-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="72f1b-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="72f1b-115">W tym przykładzie jest pobierana Lista usług w ramach aplikacji "testApp".</span><span class="sxs-lookup"><span data-stu-id="72f1b-115">This example gets a list of the services under the application "testApp".</span></span>

## <span data-ttu-id="72f1b-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72f1b-116">PARAMETERS</span></span>

### <span data-ttu-id="72f1b-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="72f1b-117">-ApplicationName</span></span>
<span data-ttu-id="72f1b-118">Określ nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="72f1b-118">Specify the name of the application.</span></span>

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

### <span data-ttu-id="72f1b-119">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="72f1b-119">-ClusterName</span></span>
<span data-ttu-id="72f1b-120">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="72f1b-120">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="72f1b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72f1b-121">-DefaultProfile</span></span>
<span data-ttu-id="72f1b-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="72f1b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72f1b-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="72f1b-123">-Name</span></span>
<span data-ttu-id="72f1b-124">Określ nazwę usługi.</span><span class="sxs-lookup"><span data-stu-id="72f1b-124">Specify the name of the service.</span></span>

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

### <span data-ttu-id="72f1b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72f1b-125">-ResourceGroupName</span></span>
<span data-ttu-id="72f1b-126">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="72f1b-126">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="72f1b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72f1b-127">-ResourceId</span></span>
<span data-ttu-id="72f1b-128">Identyfikator zasobu ARM usługi.</span><span class="sxs-lookup"><span data-stu-id="72f1b-128">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="72f1b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72f1b-129">CommonParameters</span></span>
<span data-ttu-id="72f1b-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72f1b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72f1b-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72f1b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72f1b-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72f1b-132">INPUTS</span></span>

### <span data-ttu-id="72f1b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="72f1b-133">System.String</span></span>

## <span data-ttu-id="72f1b-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72f1b-134">OUTPUTS</span></span>

### <span data-ttu-id="72f1b-135">Microsoft. Azure. Commands. servicefabric. MODELES. PSService</span><span class="sxs-lookup"><span data-stu-id="72f1b-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="72f1b-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72f1b-136">NOTES</span></span>

## <span data-ttu-id="72f1b-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72f1b-137">RELATED LINKS</span></span>

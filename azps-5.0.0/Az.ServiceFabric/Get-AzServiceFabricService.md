---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: 1dfd9e0aa2bc6b7c5d52ccfed756f2a96a3f307c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307879"
---
# <span data-ttu-id="1f0db-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="1f0db-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="1f0db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f0db-102">SYNOPSIS</span></span>
<span data-ttu-id="1f0db-103">Pobierz szczegóły usługi programu Service Fabric w określonej aplikacji i klastrze.</span><span class="sxs-lookup"><span data-stu-id="1f0db-103">Get Service Fabric service details under the specified application and cluster.</span></span>

## <span data-ttu-id="1f0db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f0db-104">SYNTAX</span></span>

### <span data-ttu-id="1f0db-105">ByResourceGroupAndCluster (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1f0db-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f0db-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1f0db-106">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f0db-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1f0db-107">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f0db-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1f0db-108">DESCRIPTION</span></span>
<span data-ttu-id="1f0db-109">To polecenie cmdlet spowoduje wyświetlenie szczegółowych informacji o usłudze w określonej aplikacji i klastrze.</span><span class="sxs-lookup"><span data-stu-id="1f0db-109">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="1f0db-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f0db-110">EXAMPLES</span></span>

### <span data-ttu-id="1f0db-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1f0db-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="1f0db-112">W tym przykładzie są pobierane dane zasobu usługi dotyczące usługi "testApp ~ testService".</span><span class="sxs-lookup"><span data-stu-id="1f0db-112">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="1f0db-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1f0db-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="1f0db-114">W tym przykładzie jest pobierana Lista usług w ramach aplikacji "testApp".</span><span class="sxs-lookup"><span data-stu-id="1f0db-114">This example gets a list of the services under the application "testApp".</span></span>

## <span data-ttu-id="1f0db-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f0db-115">PARAMETERS</span></span>

### <span data-ttu-id="1f0db-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="1f0db-116">-ApplicationName</span></span>
<span data-ttu-id="1f0db-117">Określ nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f0db-117">Specify the name of the application.</span></span>

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

### <span data-ttu-id="1f0db-118">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="1f0db-118">-ClusterName</span></span>
<span data-ttu-id="1f0db-119">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="1f0db-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="1f0db-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f0db-120">-DefaultProfile</span></span>
<span data-ttu-id="1f0db-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f0db-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f0db-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1f0db-122">-Name</span></span>
<span data-ttu-id="1f0db-123">Określ nazwę usługi.</span><span class="sxs-lookup"><span data-stu-id="1f0db-123">Specify the name of the service.</span></span>

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

### <span data-ttu-id="1f0db-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f0db-124">-ResourceGroupName</span></span>
<span data-ttu-id="1f0db-125">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1f0db-125">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1f0db-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f0db-126">-ResourceId</span></span>
<span data-ttu-id="1f0db-127">Identyfikator zasobu ARM usługi.</span><span class="sxs-lookup"><span data-stu-id="1f0db-127">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="1f0db-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f0db-128">CommonParameters</span></span>
<span data-ttu-id="1f0db-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f0db-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f0db-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f0db-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f0db-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f0db-131">INPUTS</span></span>

### <span data-ttu-id="1f0db-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1f0db-132">System.String</span></span>

## <span data-ttu-id="1f0db-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f0db-133">OUTPUTS</span></span>

### <span data-ttu-id="1f0db-134">Microsoft. Azure. Commands. servicefabric. MODELES. PSService</span><span class="sxs-lookup"><span data-stu-id="1f0db-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="1f0db-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f0db-135">NOTES</span></span>

## <span data-ttu-id="1f0db-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f0db-136">RELATED LINKS</span></span>

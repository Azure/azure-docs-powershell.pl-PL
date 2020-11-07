---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: 3076a405c47f165d2ace1e5251644cf4e4484a03
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871531"
---
# <span data-ttu-id="aaaaf-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="aaaaf-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="aaaaf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aaaaf-102">SYNOPSIS</span></span>
<span data-ttu-id="aaaaf-103">Pobierz szczegóły usługi programu Service Fabric w określonej aplikacji i klastrze.</span><span class="sxs-lookup"><span data-stu-id="aaaaf-103">Get Service Fabric service details under the specified application and cluster.</span></span>

## <span data-ttu-id="aaaaf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aaaaf-104">SYNTAX</span></span>

### <span data-ttu-id="aaaaf-105">ByResourceGroupAndCluster (domyślny)</span><span class="sxs-lookup"><span data-stu-id="aaaaf-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aaaaf-106">ByName</span><span class="sxs-lookup"><span data-stu-id="aaaaf-106">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aaaaf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="aaaaf-107">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aaaaf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="aaaaf-108">DESCRIPTION</span></span>
<span data-ttu-id="aaaaf-109">To polecenie cmdlet spowoduje wyświetlenie szczegółowych informacji o usłudze w określonej aplikacji i klastrze.</span><span class="sxs-lookup"><span data-stu-id="aaaaf-109">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="aaaaf-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aaaaf-110">EXAMPLES</span></span>

### <span data-ttu-id="aaaaf-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aaaaf-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="aaaaf-112">W tym przykładzie są pobierane dane zasobu usługi dotyczące usługi "testApp ~ testService".</span><span class="sxs-lookup"><span data-stu-id="aaaaf-112">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="aaaaf-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="aaaaf-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="aaaaf-114">W tym przykładzie jest pobierana Lista usług w obszarze aplication "testApp".</span><span class="sxs-lookup"><span data-stu-id="aaaaf-114">This example gets a list of the services under the aplication "testApp".</span></span>

## <span data-ttu-id="aaaaf-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aaaaf-115">PARAMETERS</span></span>

### <span data-ttu-id="aaaaf-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="aaaaf-116">-ApplicationName</span></span>
<span data-ttu-id="aaaaf-117">Określ nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="aaaaf-117">Specify the name of the application.</span></span>

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

### <span data-ttu-id="aaaaf-118">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="aaaaf-118">-ClusterName</span></span>
<span data-ttu-id="aaaaf-119">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="aaaaf-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="aaaaf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaaaf-120">-DefaultProfile</span></span>
<span data-ttu-id="aaaaf-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aaaaf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaaaf-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aaaaf-122">-Name</span></span>
<span data-ttu-id="aaaaf-123">Określ nazwę usługi.</span><span class="sxs-lookup"><span data-stu-id="aaaaf-123">Specify the name of the service.</span></span>

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

### <span data-ttu-id="aaaaf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaaaf-124">-ResourceGroupName</span></span>
<span data-ttu-id="aaaaf-125">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aaaaf-125">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="aaaaf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aaaaf-126">-ResourceId</span></span>
<span data-ttu-id="aaaaf-127">Identyfikator zasobu ARM usługi.</span><span class="sxs-lookup"><span data-stu-id="aaaaf-127">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="aaaaf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaaaf-128">CommonParameters</span></span>
<span data-ttu-id="aaaaf-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaaaf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaaaf-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaaaf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaaaf-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aaaaf-131">INPUTS</span></span>

### <span data-ttu-id="aaaaf-132">System. String</span><span class="sxs-lookup"><span data-stu-id="aaaaf-132">System.String</span></span>

## <span data-ttu-id="aaaaf-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aaaaf-133">OUTPUTS</span></span>

### <span data-ttu-id="aaaaf-134">Microsoft. Azure. Commands. servicefabric. MODELES. PSService</span><span class="sxs-lookup"><span data-stu-id="aaaaf-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="aaaaf-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aaaaf-135">NOTES</span></span>

## <span data-ttu-id="aaaaf-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aaaaf-136">RELATED LINKS</span></span>

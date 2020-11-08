---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: c282ea9e902f26d010c2421339de68bc670e2f35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219823"
---
# <span data-ttu-id="2569c-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2569c-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="2569c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2569c-102">SYNOPSIS</span></span>
<span data-ttu-id="2569c-103">Pobierz szczegóły aplikacji sieci szkieletowej usług.</span><span class="sxs-lookup"><span data-stu-id="2569c-103">Get Service Fabric application details.</span></span>

## <span data-ttu-id="2569c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2569c-104">SYNTAX</span></span>

### <span data-ttu-id="2569c-105">ByResourceGroupAndCluster (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2569c-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2569c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2569c-106">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2569c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2569c-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2569c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2569c-108">DESCRIPTION</span></span>
<span data-ttu-id="2569c-109">To polecenie cmdlet spowoduje wyświetlenie szczegółów aplikacji w określonej grupie zasobów i klastrze.</span><span class="sxs-lookup"><span data-stu-id="2569c-109">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="2569c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2569c-110">EXAMPLES</span></span>

### <span data-ttu-id="2569c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2569c-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="2569c-112">W tym przykładzie są pobierane szczegóły zasobu aplikacji dla aplikacji "testApp".</span><span class="sxs-lookup"><span data-stu-id="2569c-112">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="2569c-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2569c-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="2569c-114">W tym przykładzie jest pobierana lista aplikacji w ramach klastra "testCluster".</span><span class="sxs-lookup"><span data-stu-id="2569c-114">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="2569c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2569c-115">PARAMETERS</span></span>

### <span data-ttu-id="2569c-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="2569c-116">-ClusterName</span></span>
<span data-ttu-id="2569c-117">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="2569c-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2569c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2569c-118">-DefaultProfile</span></span>
<span data-ttu-id="2569c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2569c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2569c-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2569c-120">-Name</span></span>
<span data-ttu-id="2569c-121">Określ nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2569c-121">Specify the name of the application.</span></span>

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

### <span data-ttu-id="2569c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2569c-122">-ResourceGroupName</span></span>
<span data-ttu-id="2569c-123">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2569c-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="2569c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2569c-124">-ResourceId</span></span>
<span data-ttu-id="2569c-125">Identyfikator zasobu ARM aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2569c-125">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="2569c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2569c-126">CommonParameters</span></span>
<span data-ttu-id="2569c-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2569c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2569c-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2569c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2569c-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2569c-129">INPUTS</span></span>

### <span data-ttu-id="2569c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2569c-130">System.String</span></span>

## <span data-ttu-id="2569c-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2569c-131">OUTPUTS</span></span>

### <span data-ttu-id="2569c-132">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplication</span><span class="sxs-lookup"><span data-stu-id="2569c-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="2569c-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2569c-133">NOTES</span></span>

## <span data-ttu-id="2569c-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2569c-134">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: e78580f98ae0569a2104a4d39123070e7383fa6f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053257"
---
# <span data-ttu-id="64c24-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="64c24-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="64c24-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64c24-102">SYNOPSIS</span></span>
<span data-ttu-id="64c24-103">Pobierz szczegóły aplikacji sieci szkieletowej usług.</span><span class="sxs-lookup"><span data-stu-id="64c24-103">Get Service Fabric application details.</span></span>

## <span data-ttu-id="64c24-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64c24-104">SYNTAX</span></span>

### <span data-ttu-id="64c24-105">ByResourceGroupAndCluster (domyślny)</span><span class="sxs-lookup"><span data-stu-id="64c24-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64c24-106">ByName</span><span class="sxs-lookup"><span data-stu-id="64c24-106">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64c24-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="64c24-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64c24-108">Opis</span><span class="sxs-lookup"><span data-stu-id="64c24-108">DESCRIPTION</span></span>
<span data-ttu-id="64c24-109">To polecenie cmdlet spowoduje wyświetlenie szczegółów aplikacji w określonej grupie zasobów i klastrze.</span><span class="sxs-lookup"><span data-stu-id="64c24-109">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="64c24-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64c24-110">EXAMPLES</span></span>

### <span data-ttu-id="64c24-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="64c24-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="64c24-112">W tym przykładzie są pobierane szczegóły zasobu aplikacji dla aplikacji "testApp".</span><span class="sxs-lookup"><span data-stu-id="64c24-112">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="64c24-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="64c24-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="64c24-114">W tym przykładzie jest pobierana lista aplikacji w ramach klastra "testCluster".</span><span class="sxs-lookup"><span data-stu-id="64c24-114">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="64c24-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64c24-115">PARAMETERS</span></span>

### <span data-ttu-id="64c24-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="64c24-116">-ClusterName</span></span>
<span data-ttu-id="64c24-117">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="64c24-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="64c24-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64c24-118">-DefaultProfile</span></span>
<span data-ttu-id="64c24-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="64c24-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64c24-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="64c24-120">-Name</span></span>
<span data-ttu-id="64c24-121">Określ nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="64c24-121">Specify the name of the application.</span></span>

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

### <span data-ttu-id="64c24-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64c24-122">-ResourceGroupName</span></span>
<span data-ttu-id="64c24-123">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="64c24-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="64c24-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64c24-124">-ResourceId</span></span>
<span data-ttu-id="64c24-125">Identyfikator zasobu ARM aplikacji.</span><span class="sxs-lookup"><span data-stu-id="64c24-125">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="64c24-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64c24-126">CommonParameters</span></span>
<span data-ttu-id="64c24-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64c24-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64c24-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64c24-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64c24-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64c24-129">INPUTS</span></span>

### <span data-ttu-id="64c24-130">System. String</span><span class="sxs-lookup"><span data-stu-id="64c24-130">System.String</span></span>

## <span data-ttu-id="64c24-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64c24-131">OUTPUTS</span></span>

### <span data-ttu-id="64c24-132">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplication</span><span class="sxs-lookup"><span data-stu-id="64c24-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="64c24-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64c24-133">NOTES</span></span>

## <span data-ttu-id="64c24-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64c24-134">RELATED LINKS</span></span>

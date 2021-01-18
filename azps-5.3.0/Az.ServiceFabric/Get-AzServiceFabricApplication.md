---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: 5946be075e2b97283546614543d5a0d4544bfa0f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502832"
---
# <span data-ttu-id="97843-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="97843-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="97843-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="97843-102">SYNOPSIS</span></span>
<span data-ttu-id="97843-103">Pobierz szczegóły aplikacji sieci szkieletowej usług.</span><span class="sxs-lookup"><span data-stu-id="97843-103">Get Service Fabric application details.</span></span> <span data-ttu-id="97843-104">Obsługuje tylko aplikacje rozmieszczone w ARM.</span><span class="sxs-lookup"><span data-stu-id="97843-104">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="97843-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="97843-105">SYNTAX</span></span>

### <span data-ttu-id="97843-106">ByResourceGroupAndCluster (domyślny)</span><span class="sxs-lookup"><span data-stu-id="97843-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97843-107">ByName</span><span class="sxs-lookup"><span data-stu-id="97843-107">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97843-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="97843-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97843-109">Opis</span><span class="sxs-lookup"><span data-stu-id="97843-109">DESCRIPTION</span></span>
<span data-ttu-id="97843-110">To polecenie cmdlet spowoduje wyświetlenie szczegółów aplikacji w określonej grupie zasobów i klastrze.</span><span class="sxs-lookup"><span data-stu-id="97843-110">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="97843-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="97843-111">EXAMPLES</span></span>

### <span data-ttu-id="97843-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="97843-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="97843-113">W tym przykładzie są pobierane szczegóły zasobu aplikacji dla aplikacji "testApp".</span><span class="sxs-lookup"><span data-stu-id="97843-113">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="97843-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="97843-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="97843-115">W tym przykładzie jest pobierana lista aplikacji w ramach klastra "testCluster".</span><span class="sxs-lookup"><span data-stu-id="97843-115">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="97843-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="97843-116">PARAMETERS</span></span>

### <span data-ttu-id="97843-117">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="97843-117">-ClusterName</span></span>
<span data-ttu-id="97843-118">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="97843-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="97843-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97843-119">-DefaultProfile</span></span>
<span data-ttu-id="97843-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="97843-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97843-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="97843-121">-Name</span></span>
<span data-ttu-id="97843-122">Określ nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="97843-122">Specify the name of the application.</span></span>

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

### <span data-ttu-id="97843-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97843-123">-ResourceGroupName</span></span>
<span data-ttu-id="97843-124">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="97843-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="97843-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97843-125">-ResourceId</span></span>
<span data-ttu-id="97843-126">Identyfikator zasobu ARM aplikacji.</span><span class="sxs-lookup"><span data-stu-id="97843-126">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="97843-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97843-127">CommonParameters</span></span>
<span data-ttu-id="97843-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97843-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97843-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97843-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97843-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97843-130">INPUTS</span></span>

### <span data-ttu-id="97843-131">System. String</span><span class="sxs-lookup"><span data-stu-id="97843-131">System.String</span></span>

## <span data-ttu-id="97843-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="97843-132">OUTPUTS</span></span>

### <span data-ttu-id="97843-133">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplication</span><span class="sxs-lookup"><span data-stu-id="97843-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="97843-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="97843-134">NOTES</span></span>

## <span data-ttu-id="97843-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97843-135">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: a0625a974da7d6544345419573fa4e96f0bbcae1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224214"
---
# <span data-ttu-id="111fb-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="111fb-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="111fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="111fb-102">SYNOPSIS</span></span>
<span data-ttu-id="111fb-103">Pobieranie szczegółów typu aplikacji sieci szkieletowej usług.</span><span class="sxs-lookup"><span data-stu-id="111fb-103">Get Service Fabric application type details.</span></span>

## <span data-ttu-id="111fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="111fb-104">SYNTAX</span></span>

### <span data-ttu-id="111fb-105">ByResourceGroupAndCluster (domyślny)</span><span class="sxs-lookup"><span data-stu-id="111fb-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="111fb-106">ByName</span><span class="sxs-lookup"><span data-stu-id="111fb-106">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="111fb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="111fb-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="111fb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="111fb-108">DESCRIPTION</span></span>
<span data-ttu-id="111fb-109">Użyj tego polecenia cmdlet, aby uzyskać szczegółowe informacje o typie aplikacji w określonej grupie zasobów i klastrze.</span><span class="sxs-lookup"><span data-stu-id="111fb-109">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="111fb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="111fb-110">EXAMPLES</span></span>

### <span data-ttu-id="111fb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="111fb-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="111fb-112">W tym przykładzie zostaną podane szczegóły dotyczące typu aplikacji z określonymi parametrami, jeśli nie znajdzie zasobu, który wygeneruje wyjątek.</span><span class="sxs-lookup"><span data-stu-id="111fb-112">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="111fb-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="111fb-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="111fb-114">W tym przykładzie pojawi się lista typów aplikacji zdefiniowanych w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="111fb-114">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="111fb-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="111fb-115">PARAMETERS</span></span>

### <span data-ttu-id="111fb-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="111fb-116">-ClusterName</span></span>
<span data-ttu-id="111fb-117">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="111fb-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="111fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="111fb-118">-DefaultProfile</span></span>
<span data-ttu-id="111fb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="111fb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="111fb-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="111fb-120">-Name</span></span>
<span data-ttu-id="111fb-121">Określ nazwę typu aplikacji</span><span class="sxs-lookup"><span data-stu-id="111fb-121">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="111fb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="111fb-122">-ResourceGroupName</span></span>
<span data-ttu-id="111fb-123">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="111fb-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="111fb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="111fb-124">-ResourceId</span></span>
<span data-ttu-id="111fb-125">Identyfikator zasobu ARM dla typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="111fb-125">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="111fb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="111fb-126">CommonParameters</span></span>
<span data-ttu-id="111fb-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="111fb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="111fb-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="111fb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="111fb-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="111fb-129">INPUTS</span></span>

### <span data-ttu-id="111fb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="111fb-130">System.String</span></span>

## <span data-ttu-id="111fb-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="111fb-131">OUTPUTS</span></span>

### <span data-ttu-id="111fb-132">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="111fb-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="111fb-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="111fb-133">NOTES</span></span>

## <span data-ttu-id="111fb-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="111fb-134">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: ea86fb4a110d355a848b9fe58969d30ccb96e2da
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063208"
---
# <span data-ttu-id="958bc-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="958bc-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="958bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="958bc-102">SYNOPSIS</span></span>
<span data-ttu-id="958bc-103">Uzyskiwanie szczegółowych informacji o wersji typu aplikacji sieci szkieletowej usług.</span><span class="sxs-lookup"><span data-stu-id="958bc-103">Get Service Fabric application type version details.</span></span>

## <span data-ttu-id="958bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="958bc-104">SYNTAX</span></span>

### <span data-ttu-id="958bc-105">ByResourceGroupAndCluster (domyślny)</span><span class="sxs-lookup"><span data-stu-id="958bc-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="958bc-106">ByVersion</span><span class="sxs-lookup"><span data-stu-id="958bc-106">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="958bc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="958bc-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="958bc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="958bc-108">DESCRIPTION</span></span>
<span data-ttu-id="958bc-109">Użyj tego polecenia cmdlet, aby uzyskać szczegółowe informacje o wersji typu aplikacji w określonej grupie zasobów i klastrze.</span><span class="sxs-lookup"><span data-stu-id="958bc-109">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="958bc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="958bc-110">EXAMPLES</span></span>

### <span data-ttu-id="958bc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="958bc-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="958bc-112">W tym przykładzie jest pobierana aplikacja typu "testAppType" z wersją "v1", jeśli nie znajdzie zasobu, który wygeneruje wyjątek.</span><span class="sxs-lookup"><span data-stu-id="958bc-112">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="958bc-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="958bc-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="958bc-114">W tym przykładzie jest pobierana Lista wersji typów aplikacji zdefiniowanych w określonym klastrze i typ.</span><span class="sxs-lookup"><span data-stu-id="958bc-114">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="958bc-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="958bc-115">PARAMETERS</span></span>

### <span data-ttu-id="958bc-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="958bc-116">-ClusterName</span></span>
<span data-ttu-id="958bc-117">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="958bc-117">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="958bc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="958bc-118">-DefaultProfile</span></span>
<span data-ttu-id="958bc-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="958bc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="958bc-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="958bc-120">-Name</span></span>
<span data-ttu-id="958bc-121">Określ nazwę typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="958bc-121">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="958bc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="958bc-122">-ResourceGroupName</span></span>
<span data-ttu-id="958bc-123">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="958bc-123">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="958bc-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="958bc-124">-ResourceId</span></span>
<span data-ttu-id="958bc-125">Identyfikator zasobu ARM w wersji typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="958bc-125">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="958bc-126">-Version</span><span class="sxs-lookup"><span data-stu-id="958bc-126">-Version</span></span>
<span data-ttu-id="958bc-127">Określ wersję typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="958bc-127">Specify the version of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVersion
Aliases: ApplicationTypeVersion

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="958bc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="958bc-128">CommonParameters</span></span>
<span data-ttu-id="958bc-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="958bc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="958bc-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="958bc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="958bc-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="958bc-131">INPUTS</span></span>

### <span data-ttu-id="958bc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="958bc-132">System.String</span></span>

## <span data-ttu-id="958bc-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="958bc-133">OUTPUTS</span></span>

### <span data-ttu-id="958bc-134">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="958bc-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="958bc-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="958bc-135">NOTES</span></span>

## <span data-ttu-id="958bc-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="958bc-136">RELATED LINKS</span></span>

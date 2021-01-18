---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 7dc8ca2302b00b5eb200c30aed104f5fe5ff8642
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502827"
---
# <span data-ttu-id="587ef-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="587ef-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="587ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="587ef-102">SYNOPSIS</span></span>
<span data-ttu-id="587ef-103">Uzyskiwanie szczegółowych informacji o wersji typu aplikacji sieci szkieletowej usług.</span><span class="sxs-lookup"><span data-stu-id="587ef-103">Get Service Fabric application type version details.</span></span> <span data-ttu-id="587ef-104">Obsługuje tylko wersje typu aplikacja ARM wdrożone.</span><span class="sxs-lookup"><span data-stu-id="587ef-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="587ef-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="587ef-105">SYNTAX</span></span>

### <span data-ttu-id="587ef-106">ByResourceGroupAndCluster (domyślny)</span><span class="sxs-lookup"><span data-stu-id="587ef-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="587ef-107">ByVersion</span><span class="sxs-lookup"><span data-stu-id="587ef-107">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="587ef-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="587ef-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="587ef-109">Opis</span><span class="sxs-lookup"><span data-stu-id="587ef-109">DESCRIPTION</span></span>
<span data-ttu-id="587ef-110">Użyj tego polecenia cmdlet, aby uzyskać szczegółowe informacje o wersji typu aplikacji w określonej grupie zasobów i klastrze.</span><span class="sxs-lookup"><span data-stu-id="587ef-110">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="587ef-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="587ef-111">EXAMPLES</span></span>

### <span data-ttu-id="587ef-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="587ef-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="587ef-113">W tym przykładzie jest pobierana aplikacja typu "testAppType" z wersją "v1", jeśli nie znajdzie zasobu, który wygeneruje wyjątek.</span><span class="sxs-lookup"><span data-stu-id="587ef-113">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="587ef-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="587ef-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="587ef-115">W tym przykładzie jest pobierana Lista wersji typów aplikacji zdefiniowanych w określonym klastrze i typ.</span><span class="sxs-lookup"><span data-stu-id="587ef-115">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="587ef-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="587ef-116">PARAMETERS</span></span>

### <span data-ttu-id="587ef-117">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="587ef-117">-ClusterName</span></span>
<span data-ttu-id="587ef-118">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="587ef-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="587ef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="587ef-119">-DefaultProfile</span></span>
<span data-ttu-id="587ef-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="587ef-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="587ef-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="587ef-121">-Name</span></span>
<span data-ttu-id="587ef-122">Określ nazwę typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="587ef-122">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="587ef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="587ef-123">-ResourceGroupName</span></span>
<span data-ttu-id="587ef-124">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="587ef-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="587ef-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="587ef-125">-ResourceId</span></span>
<span data-ttu-id="587ef-126">Identyfikator zasobu ARM w wersji typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="587ef-126">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="587ef-127">-Version</span><span class="sxs-lookup"><span data-stu-id="587ef-127">-Version</span></span>
<span data-ttu-id="587ef-128">Określ wersję typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="587ef-128">Specify the version of the application type.</span></span>

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

### <span data-ttu-id="587ef-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="587ef-129">CommonParameters</span></span>
<span data-ttu-id="587ef-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="587ef-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="587ef-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="587ef-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="587ef-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="587ef-132">INPUTS</span></span>

### <span data-ttu-id="587ef-133">System. String</span><span class="sxs-lookup"><span data-stu-id="587ef-133">System.String</span></span>

## <span data-ttu-id="587ef-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="587ef-134">OUTPUTS</span></span>

### <span data-ttu-id="587ef-135">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="587ef-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="587ef-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="587ef-136">NOTES</span></span>

## <span data-ttu-id="587ef-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="587ef-137">RELATED LINKS</span></span>

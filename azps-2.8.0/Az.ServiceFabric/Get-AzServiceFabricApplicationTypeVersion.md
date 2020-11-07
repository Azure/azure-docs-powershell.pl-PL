---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 0af0b8ac4f632682ee60bd691c41fb4500c2c2a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871535"
---
# <span data-ttu-id="c97da-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c97da-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="c97da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c97da-102">SYNOPSIS</span></span>
<span data-ttu-id="c97da-103">Uzyskiwanie szczegółowych informacji o wersji typu aplikacji sieci szkieletowej usług.</span><span class="sxs-lookup"><span data-stu-id="c97da-103">Get Service Fabric application type version details.</span></span>

## <span data-ttu-id="c97da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c97da-104">SYNTAX</span></span>

### <span data-ttu-id="c97da-105">ByResourceGroupAndCluster (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c97da-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c97da-106">ByVersion</span><span class="sxs-lookup"><span data-stu-id="c97da-106">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c97da-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c97da-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c97da-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c97da-108">DESCRIPTION</span></span>
<span data-ttu-id="c97da-109">Użyj tego polecenia cmdlet, aby uzyskać szczegółowe informacje o wersji typu aplikacji w określonej grupie zasobów i klastrze.</span><span class="sxs-lookup"><span data-stu-id="c97da-109">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="c97da-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c97da-110">EXAMPLES</span></span>

### <span data-ttu-id="c97da-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c97da-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="c97da-112">W tym przykładzie jest pobierana aplikacja typu "testAppType" z wersją "v1", jeśli nie znajdzie zasobu, który wygeneruje wyjątek.</span><span class="sxs-lookup"><span data-stu-id="c97da-112">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="c97da-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c97da-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="c97da-114">W tym przykładzie jest pobierana Lista wersji typów aplikacji zdefiniowanych w określonym klastrze i typ.</span><span class="sxs-lookup"><span data-stu-id="c97da-114">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="c97da-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c97da-115">PARAMETERS</span></span>

### <span data-ttu-id="c97da-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="c97da-116">-ClusterName</span></span>
<span data-ttu-id="c97da-117">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="c97da-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c97da-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c97da-118">-DefaultProfile</span></span>
<span data-ttu-id="c97da-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c97da-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c97da-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c97da-120">-Name</span></span>
<span data-ttu-id="c97da-121">Określ nazwę typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c97da-121">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="c97da-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c97da-122">-ResourceGroupName</span></span>
<span data-ttu-id="c97da-123">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c97da-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c97da-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c97da-124">-ResourceId</span></span>
<span data-ttu-id="c97da-125">Identyfikator zasobu ARM w wersji typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c97da-125">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="c97da-126">-Version</span><span class="sxs-lookup"><span data-stu-id="c97da-126">-Version</span></span>
<span data-ttu-id="c97da-127">Określ wersję typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c97da-127">Specify the version of the application type.</span></span>

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

### <span data-ttu-id="c97da-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c97da-128">CommonParameters</span></span>
<span data-ttu-id="c97da-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c97da-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c97da-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c97da-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c97da-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c97da-131">INPUTS</span></span>

### <span data-ttu-id="c97da-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c97da-132">System.String</span></span>

## <span data-ttu-id="c97da-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c97da-133">OUTPUTS</span></span>

### <span data-ttu-id="c97da-134">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c97da-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="c97da-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c97da-135">NOTES</span></span>

## <span data-ttu-id="c97da-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c97da-136">RELATED LINKS</span></span>

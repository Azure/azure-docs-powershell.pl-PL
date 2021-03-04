---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 9c9f1b3c88e49eca3be8a923324d195d3a773c1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974314"
---
# <span data-ttu-id="907a1-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="907a1-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="907a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="907a1-102">SYNOPSIS</span></span>
<span data-ttu-id="907a1-103">Uzyskaj szczegółowe informacje o wersji typu materiału usługowego.</span><span class="sxs-lookup"><span data-stu-id="907a1-103">Get Service Fabric application type version details.</span></span> <span data-ttu-id="907a1-104">Obsługuje tylko ARM wersji typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="907a1-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="907a1-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="907a1-105">SYNTAX</span></span>

### <span data-ttu-id="907a1-106">ByResourceGroupAndCluster (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="907a1-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="907a1-107">ByVersion</span><span class="sxs-lookup"><span data-stu-id="907a1-107">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="907a1-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="907a1-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="907a1-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="907a1-109">DESCRIPTION</span></span>
<span data-ttu-id="907a1-110">To polecenie cmdlet umożliwia uzyskiwanie szczegółów wersji typu aplikacji w określonej grupie zasobów i klastrze.</span><span class="sxs-lookup"><span data-stu-id="907a1-110">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="907a1-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="907a1-111">EXAMPLES</span></span>

### <span data-ttu-id="907a1-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="907a1-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="907a1-113">W tym przykładzie typ aplikacji "testAppType" z wersją "v1", jeśli nie znajdzie zasobu, będzie zgłaszał wyjątek.</span><span class="sxs-lookup"><span data-stu-id="907a1-113">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="907a1-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="907a1-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="907a1-115">Ten przykład zawiera listę wersji typu aplikacji zdefiniowanych w określonym klastrze i typie.</span><span class="sxs-lookup"><span data-stu-id="907a1-115">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="907a1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="907a1-116">PARAMETERS</span></span>

### <span data-ttu-id="907a1-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="907a1-117">-ClusterName</span></span>
<span data-ttu-id="907a1-118">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="907a1-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="907a1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="907a1-119">-DefaultProfile</span></span>
<span data-ttu-id="907a1-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="907a1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="907a1-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="907a1-121">-Name</span></span>
<span data-ttu-id="907a1-122">Określ nazwę typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="907a1-122">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="907a1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="907a1-123">-ResourceGroupName</span></span>
<span data-ttu-id="907a1-124">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="907a1-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="907a1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="907a1-125">-ResourceId</span></span>
<span data-ttu-id="907a1-126">Arm ResourceId wersji typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="907a1-126">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="907a1-127">— Wersja</span><span class="sxs-lookup"><span data-stu-id="907a1-127">-Version</span></span>
<span data-ttu-id="907a1-128">Określ wersję typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="907a1-128">Specify the version of the application type.</span></span>

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

### <span data-ttu-id="907a1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="907a1-129">CommonParameters</span></span>
<span data-ttu-id="907a1-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="907a1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="907a1-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="907a1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="907a1-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="907a1-132">INPUTS</span></span>

### <span data-ttu-id="907a1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="907a1-133">System.String</span></span>

## <span data-ttu-id="907a1-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="907a1-134">OUTPUTS</span></span>

### <span data-ttu-id="907a1-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="907a1-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="907a1-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="907a1-136">NOTES</span></span>

## <span data-ttu-id="907a1-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="907a1-137">RELATED LINKS</span></span>

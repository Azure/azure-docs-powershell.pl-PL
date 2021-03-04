---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: 0082f5625351b8bb8e832ad60eb76837f09ccd47
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974321"
---
# <span data-ttu-id="c1136-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="c1136-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="c1136-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1136-102">SYNOPSIS</span></span>
<span data-ttu-id="c1136-103">Uzyskaj szczegółowe informacje o typie aplikacji Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="c1136-103">Get Service Fabric application type details.</span></span> <span data-ttu-id="c1136-104">Obsługuje tylko ARM typów aplikacji wdrożonych.</span><span class="sxs-lookup"><span data-stu-id="c1136-104">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="c1136-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c1136-105">SYNTAX</span></span>

### <span data-ttu-id="c1136-106">ByResourceGroupAndCluster (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c1136-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1136-107">ByName</span><span class="sxs-lookup"><span data-stu-id="c1136-107">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1136-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1136-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1136-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="c1136-109">DESCRIPTION</span></span>
<span data-ttu-id="c1136-110">To polecenie cmdlet umożliwia uzyskiwanie szczegółów typu aplikacji w określonej grupie zasobów i klastrze.</span><span class="sxs-lookup"><span data-stu-id="c1136-110">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="c1136-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c1136-111">EXAMPLES</span></span>

### <span data-ttu-id="c1136-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c1136-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="c1136-113">W tym przykładzie zostaną podane szczegóły typu aplikacji z określonymi parametrami, jeśli nie znajdzie zasobu, w przypadku gdyby zgłaszał wyjątek.</span><span class="sxs-lookup"><span data-stu-id="c1136-113">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="c1136-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c1136-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="c1136-115">W tym przykładzie zostanie wyświetlona lista typów aplikacji zdefiniowanych w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="c1136-115">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="c1136-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1136-116">PARAMETERS</span></span>

### <span data-ttu-id="c1136-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c1136-117">-ClusterName</span></span>
<span data-ttu-id="c1136-118">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="c1136-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c1136-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1136-119">-DefaultProfile</span></span>
<span data-ttu-id="c1136-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c1136-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1136-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c1136-121">-Name</span></span>
<span data-ttu-id="c1136-122">Określanie nazwy typu aplikacji</span><span class="sxs-lookup"><span data-stu-id="c1136-122">Specify the name of the application type</span></span>

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

### <span data-ttu-id="c1136-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1136-123">-ResourceGroupName</span></span>
<span data-ttu-id="c1136-124">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c1136-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c1136-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1136-125">-ResourceId</span></span>
<span data-ttu-id="c1136-126">Arm ResourceId typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c1136-126">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="c1136-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1136-127">CommonParameters</span></span>
<span data-ttu-id="c1136-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1136-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1136-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1136-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1136-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1136-130">INPUTS</span></span>

### <span data-ttu-id="c1136-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c1136-131">System.String</span></span>

## <span data-ttu-id="c1136-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1136-132">OUTPUTS</span></span>

### <span data-ttu-id="c1136-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="c1136-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="c1136-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c1136-134">NOTES</span></span>

## <span data-ttu-id="c1136-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1136-135">RELATED LINKS</span></span>

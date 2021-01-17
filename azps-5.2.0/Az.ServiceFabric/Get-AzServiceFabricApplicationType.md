---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: 73e89bcb6ffb6f8c09a0ec53f203b6ed251fd3e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347845"
---
# <span data-ttu-id="13f2e-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="13f2e-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="13f2e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13f2e-102">SYNOPSIS</span></span>
<span data-ttu-id="13f2e-103">Pobieranie szczegółów typu aplikacji sieci szkieletowej usług.</span><span class="sxs-lookup"><span data-stu-id="13f2e-103">Get Service Fabric application type details.</span></span> <span data-ttu-id="13f2e-104">Obsługuje tylko typy aplikacji rozmieszczone w ARM.</span><span class="sxs-lookup"><span data-stu-id="13f2e-104">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="13f2e-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13f2e-105">SYNTAX</span></span>

### <span data-ttu-id="13f2e-106">ByResourceGroupAndCluster (domyślny)</span><span class="sxs-lookup"><span data-stu-id="13f2e-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13f2e-107">ByName</span><span class="sxs-lookup"><span data-stu-id="13f2e-107">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13f2e-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="13f2e-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13f2e-109">Opis</span><span class="sxs-lookup"><span data-stu-id="13f2e-109">DESCRIPTION</span></span>
<span data-ttu-id="13f2e-110">Użyj tego polecenia cmdlet, aby uzyskać szczegółowe informacje o typie aplikacji w określonej grupie zasobów i klastrze.</span><span class="sxs-lookup"><span data-stu-id="13f2e-110">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="13f2e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13f2e-111">EXAMPLES</span></span>

### <span data-ttu-id="13f2e-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="13f2e-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="13f2e-113">W tym przykładzie zostaną podane szczegóły dotyczące typu aplikacji z określonymi parametrami, jeśli nie znajdzie zasobu, który wygeneruje wyjątek.</span><span class="sxs-lookup"><span data-stu-id="13f2e-113">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="13f2e-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="13f2e-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="13f2e-115">W tym przykładzie pojawi się lista typów aplikacji zdefiniowanych w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="13f2e-115">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="13f2e-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13f2e-116">PARAMETERS</span></span>

### <span data-ttu-id="13f2e-117">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="13f2e-117">-ClusterName</span></span>
<span data-ttu-id="13f2e-118">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="13f2e-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="13f2e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13f2e-119">-DefaultProfile</span></span>
<span data-ttu-id="13f2e-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13f2e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13f2e-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="13f2e-121">-Name</span></span>
<span data-ttu-id="13f2e-122">Określ nazwę typu aplikacji</span><span class="sxs-lookup"><span data-stu-id="13f2e-122">Specify the name of the application type</span></span>

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

### <span data-ttu-id="13f2e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13f2e-123">-ResourceGroupName</span></span>
<span data-ttu-id="13f2e-124">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="13f2e-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="13f2e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13f2e-125">-ResourceId</span></span>
<span data-ttu-id="13f2e-126">Identyfikator zasobu ARM dla typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="13f2e-126">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="13f2e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13f2e-127">CommonParameters</span></span>
<span data-ttu-id="13f2e-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13f2e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13f2e-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13f2e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13f2e-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13f2e-130">INPUTS</span></span>

### <span data-ttu-id="13f2e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="13f2e-131">System.String</span></span>

## <span data-ttu-id="13f2e-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13f2e-132">OUTPUTS</span></span>

### <span data-ttu-id="13f2e-133">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="13f2e-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="13f2e-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13f2e-134">NOTES</span></span>

## <span data-ttu-id="13f2e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13f2e-135">RELATED LINKS</span></span>

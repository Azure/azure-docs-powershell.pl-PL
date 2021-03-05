---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
ms.openlocfilehash: 624ca943d9adf7df105fae18a0a4a8ccad2b9b9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984058"
---
# <span data-ttu-id="fe3d3-101">Get-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="fe3d3-101">Get-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="fe3d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe3d3-102">SYNOPSIS</span></span>
<span data-ttu-id="fe3d3-103">Zwraca informacje o wirtualnym klastrze SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fe3d3-103">Returns information about Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="fe3d3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fe3d3-104">SYNTAX</span></span>

### <span data-ttu-id="fe3d3-105">GetVirtualClusterByResourceGroup (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="fe3d3-105">GetVirtualClusterByResourceGroup (Default)</span></span>
```
Get-AzSqlVirtualCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe3d3-106">GetVirtualClusterByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fe3d3-106">GetVirtualClusterByNameAndResourceGroup</span></span>
```
Get-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe3d3-107">GetVirtualClusterByResourceId</span><span class="sxs-lookup"><span data-stu-id="fe3d3-107">GetVirtualClusterByResourceId</span></span>
```
Get-AzSqlVirtualCluster [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe3d3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="fe3d3-108">DESCRIPTION</span></span>
<span data-ttu-id="fe3d3-109">Polecenie **cmdlet Get-AzSqlVirtualCluster** zwraca informacje dotyczące co najmniej jednego klastrów wirtualnych języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="fe3d3-109">The **Get-AzSqlVirtualCluster** cmdlet returns information about one or more Azure SQL Virtual Clusters.</span></span>
<span data-ttu-id="fe3d3-110">Określ nazwę klastra wirtualnego, aby wyświetlić informacje tylko dla tego klastra.</span><span class="sxs-lookup"><span data-stu-id="fe3d3-110">Specify the name of a virtual cluster to see information for only that cluster.</span></span>

## <span data-ttu-id="fe3d3-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fe3d3-111">EXAMPLES</span></span>

### <span data-ttu-id="fe3d3-112">Przykład 1. Uzyskiwanie wszystkich klastrów wirtualnych przypisanych do grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fe3d3-112">Example 1: Get all virtual clusters assigned to a resource group</span></span>
```powershell
PS C:> Get-AzSqlVirtualCluster -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster2
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster2
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name2

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster3
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster3
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name3
```

<span data-ttu-id="fe3d3-113">To polecenie pobiera informacje o wszystkich grupach wirtualnych przypisanych do grupy zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="fe3d3-113">This command gets information about all Virtual Clusters assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="fe3d3-114">Przykład 2. Uzyskiwanie informacji o określonym klastrze wirtualnym</span><span class="sxs-lookup"><span data-stu-id="fe3d3-114">Example 2: Get information about specific virtual cluster</span></span>
```
PS C:\>  Get-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1
```

<span data-ttu-id="fe3d3-115">To polecenie pobiera informacje o klastrze wirtualnym VirtualCluster1 w grupie zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="fe3d3-115">This command gets information about the virtual cluster VirtualCluster1 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="fe3d3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe3d3-116">PARAMETERS</span></span>

### <span data-ttu-id="fe3d3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe3d3-117">-DefaultProfile</span></span>
<span data-ttu-id="fe3d3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe3d3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe3d3-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fe3d3-119">-Name</span></span>
<span data-ttu-id="fe3d3-120">Nazwa klastru wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="fe3d3-120">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3d3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe3d3-121">-ResourceGroupName</span></span>
<span data-ttu-id="fe3d3-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fe3d3-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3d3-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe3d3-123">-ResourceId</span></span>
<span data-ttu-id="fe3d3-124">Identyfikator zasobu obiektu wystąpienia do uzyskania</span><span class="sxs-lookup"><span data-stu-id="fe3d3-124">The resource id of instance object to get</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe3d3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe3d3-125">CommonParameters</span></span>
<span data-ttu-id="fe3d3-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe3d3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe3d3-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe3d3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe3d3-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe3d3-128">INPUTS</span></span>

### <span data-ttu-id="fe3d3-129">Brak</span><span class="sxs-lookup"><span data-stu-id="fe3d3-129">None</span></span>

## <span data-ttu-id="fe3d3-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe3d3-130">OUTPUTS</span></span>

### <span data-ttu-id="fe3d3-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="fe3d3-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="fe3d3-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fe3d3-132">NOTES</span></span>

## <span data-ttu-id="fe3d3-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe3d3-133">RELATED LINKS</span></span>

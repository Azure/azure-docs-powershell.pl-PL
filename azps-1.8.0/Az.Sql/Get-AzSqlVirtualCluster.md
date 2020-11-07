---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
ms.openlocfilehash: f5e52938a6d0f618d53621a895aeb7037dc543ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707877"
---
# <span data-ttu-id="aafcd-101">Get-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="aafcd-101">Get-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="aafcd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aafcd-102">SYNOPSIS</span></span>
<span data-ttu-id="aafcd-103">Zwraca informacje o wirtualnym klastrze SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="aafcd-103">Returns information about Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="aafcd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aafcd-104">SYNTAX</span></span>

### <span data-ttu-id="aafcd-105">GetVirtualClusterByResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="aafcd-105">GetVirtualClusterByResourceGroup (Default)</span></span>
```
Get-AzSqlVirtualCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aafcd-106">GetVirtualClusterByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="aafcd-106">GetVirtualClusterByNameAndResourceGroup</span></span>
```
Get-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aafcd-107">GetVirtualClusterByResourceId</span><span class="sxs-lookup"><span data-stu-id="aafcd-107">GetVirtualClusterByResourceId</span></span>
```
Get-AzSqlVirtualCluster [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aafcd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="aafcd-108">DESCRIPTION</span></span>
<span data-ttu-id="aafcd-109">Polecenie cmdlet **Get-AzSqlVirtualCluster** zwraca informacje dotyczące co najmniej jednego wirtualnego klastra usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="aafcd-109">The **Get-AzSqlVirtualCluster** cmdlet returns information about one or more Azure SQL Virtual Clusters.</span></span>
<span data-ttu-id="aafcd-110">Określ nazwę klastra wirtualnego, aby wyświetlić informacje dotyczące tylko tego klastra.</span><span class="sxs-lookup"><span data-stu-id="aafcd-110">Specify the name of a virtual cluster to see information for only that cluster.</span></span>

## <span data-ttu-id="aafcd-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aafcd-111">EXAMPLES</span></span>

### <span data-ttu-id="aafcd-112">Przykład 1. pobieranie wszystkich wirtualnych klastrów przydzielonych do grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="aafcd-112">Example 1: Get all virtual clusters assigned to a resource group</span></span>
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

<span data-ttu-id="aafcd-113">To polecenie pobiera informacje o wszystkich klastrach wirtualnych przypisanych do grupy zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="aafcd-113">This command gets information about all Virtual Clusters assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="aafcd-114">Przykład 2: uzyskiwanie informacji o konkretnym klastrze wirtualnym</span><span class="sxs-lookup"><span data-stu-id="aafcd-114">Example 2: Get information about specific virtual cluster</span></span>
```
PS C:\>  Get-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1
```

<span data-ttu-id="aafcd-115">To polecenie pobiera informacje o VirtualCluster1 klastra wirtualnego w ResourceGroup01 grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aafcd-115">This command gets information about the virtual cluster VirtualCluster1 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="aafcd-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aafcd-116">PARAMETERS</span></span>

### <span data-ttu-id="aafcd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aafcd-117">-DefaultProfile</span></span>
<span data-ttu-id="aafcd-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aafcd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aafcd-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aafcd-119">-Name</span></span>
<span data-ttu-id="aafcd-120">Nazwa klastra wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="aafcd-120">The name of the virtual cluster.</span></span>

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

### <span data-ttu-id="aafcd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aafcd-121">-ResourceGroupName</span></span>
<span data-ttu-id="aafcd-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aafcd-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="aafcd-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aafcd-123">-ResourceId</span></span>
<span data-ttu-id="aafcd-124">Identyfikator zasobu wystąpienia, który ma zostać wyświetlony</span><span class="sxs-lookup"><span data-stu-id="aafcd-124">The resource id of instance object to get</span></span>

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

### <span data-ttu-id="aafcd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aafcd-125">CommonParameters</span></span>
<span data-ttu-id="aafcd-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aafcd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aafcd-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aafcd-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aafcd-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aafcd-128">INPUTS</span></span>

### <span data-ttu-id="aafcd-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="aafcd-129">None</span></span>

## <span data-ttu-id="aafcd-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aafcd-130">OUTPUTS</span></span>

### <span data-ttu-id="aafcd-131">Microsoft. Azure. Commands. SQL. VirtualCluster. model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="aafcd-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="aafcd-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aafcd-132">NOTES</span></span>

## <span data-ttu-id="aafcd-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aafcd-133">RELATED LINKS</span></span>
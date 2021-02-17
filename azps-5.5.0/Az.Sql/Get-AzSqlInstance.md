---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
ms.openlocfilehash: 8758cc8045856f66799144200c173ac766d8cbdb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191083"
---
# <span data-ttu-id="e4d84-101">Get-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e4d84-101">Get-AzSqlInstance</span></span>

## <span data-ttu-id="e4d84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4d84-102">SYNOPSIS</span></span>
<span data-ttu-id="e4d84-103">Zwraca informacje o wystąpieniu zarządzanej bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e4d84-103">Returns information about Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="e4d84-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e4d84-104">SYNTAX</span></span>

### <span data-ttu-id="e4d84-105">DefaultParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e4d84-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstance [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e4d84-106">ListByInstancePoolObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4d84-106">ListByInstancePoolObjectParameterSet</span></span>
```
Get-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e4d84-107">ListByInstancePoolResourceIdentiferParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4d84-107">ListByInstancePoolResourceIdentiferParameterSet</span></span>
```
Get-AzSqlInstance [-InstancePoolResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e4d84-108">GetByManagedInstanceResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4d84-108">GetByManagedInstanceResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstance [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4d84-109">ListByInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4d84-109">ListByInstancePoolParameterSet</span></span>
```
Get-AzSqlInstance [-InstancePoolName] <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4d84-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="e4d84-110">DESCRIPTION</span></span>
<span data-ttu-id="e4d84-111">Polecenie **cmdlet Get-AzSqlInstance** zwraca informacje dotyczące co najmniej jednego wystąpienia zarządzanego języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e4d84-111">The **Get-AzSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="e4d84-112">Określ nazwę wystąpienia, aby wyświetlić informacje tylko dla tego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="e4d84-112">Specify the name of an instance to see information for only that instance.</span></span>

## <span data-ttu-id="e4d84-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e4d84-113">EXAMPLES</span></span>

### <span data-ttu-id="e4d84-114">Przykład 1. Uzyskiwanie wszystkich wystąpień przypisanych do grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e4d84-114">Example 1: Get all instances assigned to a resource group</span></span>
```powershell
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
```

<span data-ttu-id="e4d84-115">To polecenie pobiera informacje o wszystkich wystąpieniach przypisanych do grupy zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="e4d84-115">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="e4d84-116">Przykład 2. Uzyskiwanie informacji o wystąpieniu</span><span class="sxs-lookup"><span data-stu-id="e4d84-116">Example 2: Get information about an  instance</span></span>
```powershell
PS C:\> Get-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
```

<span data-ttu-id="e4d84-117">To polecenie pobiera informacje o wystąpieniu o nazwie managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="e4d84-117">This command gets information about the instance named managedInstance1.</span></span>

### <span data-ttu-id="e4d84-118">Przykład 3. Uzyskiwanie wszystkich wystąpień przypisanych do grupy zasobów przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="e4d84-118">Example 3: Get all instances assigned to a resource group using filtering</span></span>
```powershell
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "managedInstance*"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
```

<span data-ttu-id="e4d84-119">To polecenie pobiera informacje o wszystkich wystąpieniach przypisanych do grupy zasobów ResourceGroup01, których wartości zaczynają się od "managedInstance".</span><span class="sxs-lookup"><span data-stu-id="e4d84-119">This command gets information about all instances assigned to the resource group ResourceGroup01 that start with "managedInstance".</span></span>

### <span data-ttu-id="e4d84-120">Przykład 4. Uzyskiwanie wszystkich wystąpień w puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="e4d84-120">Example 4: Get all instances within an instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstancePoolName "instancePool0"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="e4d84-121">To polecenie pobiera informacje o wszystkich wystąpieniach w puli wystąpień "instancePool0".</span><span class="sxs-lookup"><span data-stu-id="e4d84-121">This command gets information about all instances within the instance pool "instancePool0".</span></span>

### <span data-ttu-id="e4d84-122">Przykład 5. Uzyskiwanie wszystkich wystąpień w puli wystąpień przy użyciu obiektu pula wystąpień</span><span class="sxs-lookup"><span data-stu-id="e4d84-122">Example 5: Get all instances within an instance pool using instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName "ResourceGroup01" -Name "instancePool0"
PS C:\> Get-AzSqlInstance -InstancePool $instancePool
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="e4d84-123">To polecenie pobiera informacje o wszystkich wystąpieniach w puli wystąpień "instancePool0".</span><span class="sxs-lookup"><span data-stu-id="e4d84-123">This command gets information about all instances within the instance pool "instancePool0".</span></span>

### <span data-ttu-id="e4d84-124">Przykład 6. Uzyskiwanie wszystkich wystąpień w puli wystąpień przy użyciu identyfikatora zasobu puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="e4d84-124">Example 6: Get all instances within an instance pool using instance pool resource identifier</span></span>
```powershell
PS C:\> Get-AzSqlInstance -InstancePoolResourceIdentifier "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="e4d84-125">To polecenie pobiera informacje o wszystkich wystąpieniach w puli wystąpień "instancePool0".</span><span class="sxs-lookup"><span data-stu-id="e4d84-125">This command gets information about all instances within the instance pool "instancePool0".</span></span>

### <span data-ttu-id="e4d84-126">Przykład 7. Uzyskiwanie wystąpienia zarządzanego przy użyciu jego identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="e4d84-126">Example 7: Get a managed instance using its resource identifier</span></span>
```powershell
PS C:\> Get-AzSqlInstance -ResourceIdentifier "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="e4d84-127">To polecenie pobiera informacje o wystąpieniu o nazwie managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="e4d84-127">This command gets information about the instance named managedInstance1.</span></span>

## <span data-ttu-id="e4d84-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4d84-128">PARAMETERS</span></span>

### <span data-ttu-id="e4d84-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4d84-129">-DefaultProfile</span></span>
<span data-ttu-id="e4d84-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4d84-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4d84-131">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="e4d84-131">-InstancePool</span></span>
<span data-ttu-id="e4d84-132">Obiekt nadrzędny puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="e4d84-132">The instance pool parent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: ListByInstancePoolObjectParameterSet
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4d84-133">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="e4d84-133">-InstancePoolName</span></span>
<span data-ttu-id="e4d84-134">Nazwa puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="e4d84-134">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d84-135">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="e4d84-135">-InstancePoolResourceId</span></span>
<span data-ttu-id="e4d84-136">Identyfikator zasobu puli wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="e4d84-136">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolResourceIdentiferParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4d84-137">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e4d84-137">-Name</span></span>
<span data-ttu-id="e4d84-138">Nazwa wystąpienia języka SQL.</span><span class="sxs-lookup"><span data-stu-id="e4d84-138">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: InstanceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d84-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4d84-139">-ResourceGroupName</span></span>
<span data-ttu-id="e4d84-140">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e4d84-140">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d84-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4d84-141">-ResourceId</span></span>
<span data-ttu-id="e4d84-142">Identyfikator zasobu zarządzanego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="e4d84-142">The managed instance resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByManagedInstanceResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4d84-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4d84-143">CommonParameters</span></span>
<span data-ttu-id="e4d84-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4d84-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4d84-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4d84-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4d84-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4d84-146">INPUTS</span></span>

### <span data-ttu-id="e4d84-147">Brak</span><span class="sxs-lookup"><span data-stu-id="e4d84-147">None</span></span>

## <span data-ttu-id="e4d84-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e4d84-148">OUTPUTS</span></span>

### <span data-ttu-id="e4d84-149">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="e4d84-149">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="e4d84-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e4d84-150">NOTES</span></span>

## <span data-ttu-id="e4d84-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4d84-151">RELATED LINKS</span></span>

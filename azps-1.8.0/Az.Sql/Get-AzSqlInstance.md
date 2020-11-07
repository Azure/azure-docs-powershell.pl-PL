---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
ms.openlocfilehash: a21b2436f44cb2df5f9984e70ccecf6c1d9c306a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707945"
---
# <span data-ttu-id="e1bfa-101">Get-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e1bfa-101">Get-AzSqlInstance</span></span>

## <span data-ttu-id="e1bfa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="e1bfa-103">Zwraca informacje o wystąpieniu bazy danych zarządzanej przez usługę Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e1bfa-103">Returns information about Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="e1bfa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1bfa-104">SYNTAX</span></span>

```
Get-AzSqlInstance [[-Name] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1bfa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e1bfa-105">DESCRIPTION</span></span>
<span data-ttu-id="e1bfa-106">Polecenie cmdlet **Get-AzSqlInstance** zwraca informacje o co najmniej jednym wystąpieniu zarządzanym usługą Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e1bfa-106">The **Get-AzSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="e1bfa-107">Określ nazwę wystąpienia, aby wyświetlić informacje dotyczące tylko tego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="e1bfa-107">Specify the name of a instance to see information for only that instance.</span></span>

## <span data-ttu-id="e1bfa-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1bfa-108">EXAMPLES</span></span>

### <span data-ttu-id="e1bfa-109">Przykład 1: pobieranie wszystkich wystąpień przydzielonych do grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e1bfa-109">Example 1: Get all instances assigned to a resource group</span></span>
```
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
```

<span data-ttu-id="e1bfa-110">To polecenie pobiera informacje o wszystkich wystąpieniach przypisanych do grupy zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="e1bfa-110">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="e1bfa-111">Przykład 2: uzyskiwanie informacji o wystąpieniu</span><span class="sxs-lookup"><span data-stu-id="e1bfa-111">Example 2: Get information about an  instance</span></span>
```
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
```

<span data-ttu-id="e1bfa-112">To polecenie pobiera informacje o wystąpieniu o nazwie managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="e1bfa-112">This command gets information about the instance named managedInstance1.</span></span>

### <span data-ttu-id="e1bfa-113">Przykład 3: pobieranie wszystkich wystąpień przydzielonych do grupy zasobów przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="e1bfa-113">Example 3: Get all instances assigned to a resource group using filtering</span></span>
```
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
```

<span data-ttu-id="e1bfa-114">To polecenie pobiera informacje o wszystkich wystąpieniach przypisanych do grupy zasobów ResourceGroup01, których adres rozpoczyna się od "managedInstance".</span><span class="sxs-lookup"><span data-stu-id="e1bfa-114">This command gets information about all instances assigned to the resource group ResourceGroup01 that start with "managedInstance".</span></span>

## <span data-ttu-id="e1bfa-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1bfa-115">PARAMETERS</span></span>

### <span data-ttu-id="e1bfa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1bfa-116">-DefaultProfile</span></span>
<span data-ttu-id="e1bfa-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1bfa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1bfa-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e1bfa-118">-Name</span></span>
<span data-ttu-id="e1bfa-119">Nazwa wystąpienia SQL.</span><span class="sxs-lookup"><span data-stu-id="e1bfa-119">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="e1bfa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1bfa-120">-ResourceGroupName</span></span>
<span data-ttu-id="e1bfa-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e1bfa-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="e1bfa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1bfa-122">CommonParameters</span></span>
<span data-ttu-id="e1bfa-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1bfa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1bfa-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1bfa-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1bfa-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1bfa-125">INPUTS</span></span>

### <span data-ttu-id="e1bfa-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e1bfa-126">None</span></span>

## <span data-ttu-id="e1bfa-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1bfa-127">OUTPUTS</span></span>

### <span data-ttu-id="e1bfa-128">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="e1bfa-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="e1bfa-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1bfa-129">NOTES</span></span>

## <span data-ttu-id="e1bfa-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1bfa-130">RELATED LINKS</span></span>

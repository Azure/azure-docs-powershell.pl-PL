---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstance.md
ms.openlocfilehash: 72e3b740a84a46da094208b941e8b68173133e46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548515"
---
# <span data-ttu-id="c3e3e-101">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c3e3e-101">Get-AzureRmSqlInstance</span></span>

## <span data-ttu-id="c3e3e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3e3e-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e3e-103">Zwraca informacje o wystąpieniu bazy danych zarządzanej przez usługę Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c3e3e-103">Returns information about Azure SQL Managed Database Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3e3e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3e3e-104">SYNTAX</span></span>

### <span data-ttu-id="c3e3e-105">GetInstanceByResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c3e3e-105">GetInstanceByResourceGroup (Default)</span></span>
```
Get-AzureRmSqlInstance [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3e3e-106">GetInstanceByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c3e3e-106">GetInstanceByNameAndResourceGroup</span></span>
```
Get-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3e3e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c3e3e-107">DESCRIPTION</span></span>
<span data-ttu-id="c3e3e-108">Polecenie cmdlet **Get-AzureRmSqlInstance** zwraca informacje o co najmniej jednym wystąpieniu zarządzanym usługą Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c3e3e-108">The **Get-AzureRmSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="c3e3e-109">Określ nazwę wystąpienia, aby wyświetlić informacje dotyczące tylko tego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="c3e3e-109">Specify the name of a instance to see information for only that instance.</span></span>

## <span data-ttu-id="c3e3e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3e3e-110">EXAMPLES</span></span>

### <span data-ttu-id="c3e3e-111">Przykład 1: pobieranie wszystkich wystąpień przydzielonych do grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c3e3e-111">Example 1: Get all instances assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlInstance -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="c3e3e-112">To polecenie pobiera informacje o wszystkich wystąpieniach przypisanych do grupy zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="c3e3e-112">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="c3e3e-113">Przykład 2: uzyskiwanie informacji o wystąpieniu</span><span class="sxs-lookup"><span data-stu-id="c3e3e-113">Example 2: Get information about an  instance</span></span>
```
PS C:\>Get-AzureRmSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="c3e3e-114">To polecenie pobiera informacje o wystąpieniu o nazwie managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="c3e3e-114">This command gets information about the instance named managedInstance1.</span></span>

## <span data-ttu-id="c3e3e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3e3e-115">PARAMETERS</span></span>

### <span data-ttu-id="c3e3e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e3e-116">-DefaultProfile</span></span>
<span data-ttu-id="c3e3e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3e3e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e3e-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c3e3e-118">-Name</span></span>
<span data-ttu-id="c3e3e-119">Nazwa wystąpienia SQL.</span><span class="sxs-lookup"><span data-stu-id="c3e3e-119">SQL instance name.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceByNameAndResourceGroup
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e3e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3e3e-120">-ResourceGroupName</span></span>
<span data-ttu-id="c3e3e-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c3e3e-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetInstanceByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e3e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e3e-122">CommonParameters</span></span>
<span data-ttu-id="c3e3e-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e3e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e3e-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3e3e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e3e-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3e3e-125">INPUTS</span></span>

### <span data-ttu-id="c3e3e-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c3e3e-126">None</span></span>

## <span data-ttu-id="c3e3e-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3e3e-127">OUTPUTS</span></span>

### <span data-ttu-id="c3e3e-128">Microsoft. Azure. Commands. SQL. ManagedInstance. model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="c3e3e-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="c3e3e-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3e3e-129">NOTES</span></span>

## <span data-ttu-id="c3e3e-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3e3e-130">RELATED LINKS</span></span>

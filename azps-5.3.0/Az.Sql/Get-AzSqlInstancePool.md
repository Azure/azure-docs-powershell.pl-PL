---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
ms.openlocfilehash: afbd74953f876ede2a03e94c4db46937470a92dc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499825"
---
# <span data-ttu-id="e6ba8-101">Get-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="e6ba8-101">Get-AzSqlInstancePool</span></span>

## <span data-ttu-id="e6ba8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ba8-103">Zwraca informacje o puli wystąpień usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-103">Returns information about the Azure SQL Instance pool.</span></span>

## <span data-ttu-id="e6ba8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6ba8-104">SYNTAX</span></span>

### <span data-ttu-id="e6ba8-105">ListBySubOrResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e6ba8-105">ListBySubOrResourceGroupParameterSet (Default)</span></span>
```
Get-AzSqlInstancePool [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6ba8-106">ListByInstancePoolDefaultsParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6ba8-106">ListByInstancePoolDefaultsParameterSet</span></span>
```
Get-AzSqlInstancePool -ResourceGroupName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6ba8-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6ba8-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6ba8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e6ba8-108">DESCRIPTION</span></span>
<span data-ttu-id="e6ba8-109">Polecenie cmdlet **Get-AzSqlInstancePool** zwraca informacje o jednej lub większej liczbie puli wystąpień SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-109">The **Get-AzSqlInstancePool** cmdlet returns information about one or more Azure SQL Instance pool.</span></span>
<span data-ttu-id="e6ba8-110">Określ nazwę puli wystąpień, aby wyświetlić informacje dotyczące tylko tej puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-110">Specify the name of an instance pool to see information for only that instance pool.</span></span>

## <span data-ttu-id="e6ba8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6ba8-111">EXAMPLES</span></span>

### <span data-ttu-id="e6ba8-112">Przykład 1: pobieranie wszystkich pul wystąpień w ramach abonamentu klienta</span><span class="sxs-lookup"><span data-stu-id="e6ba8-112">Example 1: Get all instance pools across a customer subscription</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded

ResourceGroupName : resourcegroup02
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup02/providers/Microsoft.Sql/instancePools/ps-instancepool-1
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup02/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="e6ba8-113">To polecenie pobiera informacje o wszystkich pulach wystąpień w ramach abonamentu klienta.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-113">This command gets information about all instance pools within the customer subscription.</span></span>

### <span data-ttu-id="e6ba8-114">Przykład 2: pobieranie wszystkich pul wystąpień w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="e6ba8-114">Example 2: Get all instance pools across a resource group</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroupName resourcegroup01
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="e6ba8-115">To polecenie pobiera informacje o wszystkich pulach wystąpień w resourcegroup01 grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-115">This command gets information about all instance pools within the resource group resourcegroup01.</span></span>

### <span data-ttu-id="e6ba8-116">Przykład 3: uzyskiwanie informacji o puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="e6ba8-116">Example 3: Get information about an instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="e6ba8-117">To polecenie pobiera informacje o puli wystąpień instancePool0.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-117">This command gets information about the instance pool instancePool0.</span></span>

### <span data-ttu-id="e6ba8-118">Przykład 4: uzyskiwanie informacji o puli wystąpień przy użyciu identyfikatora zasobu puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="e6ba8-118">Example 4: Get information about an instance pool using instance pool resource id</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="e6ba8-119">To polecenie pobiera informacje o puli wystąpień z identyfikatorem zasobu.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-119">This command gets information about the instance pool with its resource identifier.</span></span>

## <span data-ttu-id="e6ba8-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6ba8-120">PARAMETERS</span></span>

### <span data-ttu-id="e6ba8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6ba8-121">-DefaultProfile</span></span>
<span data-ttu-id="e6ba8-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6ba8-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e6ba8-123">-Name</span></span>
<span data-ttu-id="e6ba8-124">Nazwa puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-124">The instance pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolDefaultsParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ba8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6ba8-125">-ResourceGroupName</span></span>
<span data-ttu-id="e6ba8-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListBySubOrResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolDefaultsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ba8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6ba8-127">-ResourceId</span></span>
<span data-ttu-id="e6ba8-128">Identyfikator zasobu puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-128">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstancePoolByInstancePoolResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ba8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ba8-129">CommonParameters</span></span>
<span data-ttu-id="e6ba8-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ba8-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6ba8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ba8-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6ba8-132">INPUTS</span></span>

### <span data-ttu-id="e6ba8-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e6ba8-133">None</span></span>

## <span data-ttu-id="e6ba8-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6ba8-134">OUTPUTS</span></span>

### <span data-ttu-id="e6ba8-135">Microsoft.Azure.Commands.Sql.Instance_Pools. model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="e6ba8-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

## <span data-ttu-id="e6ba8-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6ba8-136">NOTES</span></span>

## <span data-ttu-id="e6ba8-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6ba8-137">RELATED LINKS</span></span>

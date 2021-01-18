---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
ms.openlocfilehash: db7d9165b8aec6a69f31850f7a37eddb2450e53b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499425"
---
# <span data-ttu-id="7a84b-101">Set-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="7a84b-101">Set-AzSqlInstancePool</span></span>

## <span data-ttu-id="7a84b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a84b-102">SYNOPSIS</span></span>
<span data-ttu-id="7a84b-103">Ustawia właściwości puli wystąpień usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7a84b-103">Sets properties for an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="7a84b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a84b-104">SYNTAX</span></span>

### <span data-ttu-id="7a84b-105">DefaultSetInstancePoolParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7a84b-105">DefaultSetInstancePoolParameterSet (Default)</span></span>
```
Set-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a84b-106">InputObjectSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a84b-106">InputObjectSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a84b-107">ResourceIdSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a84b-107">ResourceIdSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-ResourceId] <String> [-LicenseType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a84b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7a84b-108">DESCRIPTION</span></span>
<span data-ttu-id="7a84b-109">Polecenie cmdlet **Set-AzSqlInstancePool** modyfikuje właściwości puli wystąpień usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7a84b-109">The **Set-AzSqlInstancePool** cmdlet modifies properties of an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="7a84b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a84b-110">EXAMPLES</span></span>

### <span data-ttu-id="7a84b-111">Przykład 1: Ustawianie typu licencji puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="7a84b-111">Example 1 : Set an instance pool license type</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0 -LicenseType LicenseIncluded
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

<span data-ttu-id="7a84b-112">To polecenie ustawia typ licencji i/lub znaczniki puli wystąpień o nazwie instancePool0.</span><span class="sxs-lookup"><span data-stu-id="7a84b-112">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

### <span data-ttu-id="7a84b-113">Przykład 2: Ustawianie typu licencji puli wystąpień przy użyciu obiektu puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="7a84b-113">Example 2 : Set an instance pool license type using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0
PS C:\> Set-AzSqlInstancePool -InputObject $instancePool -LicenseType LicenseIncluded
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

<span data-ttu-id="7a84b-114">To polecenie ustawia typ licencji i/lub znaczniki puli wystąpień przy użyciu obiektu puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="7a84b-114">This command sets the license type and/or tags for an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="7a84b-115">Przykład 3: Ustawianie typu licencji puli wystąpień przy użyciu identyfikatora zasobu puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="7a84b-115">Example 3 : Set an instance pool license type using an instance pool resource id</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0" -LicenseType LicenseIncluded
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

<span data-ttu-id="7a84b-116">To polecenie ustawia typ licencji i/lub znaczniki puli wystąpień o nazwie instancePool0.</span><span class="sxs-lookup"><span data-stu-id="7a84b-116">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

## <span data-ttu-id="7a84b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a84b-117">PARAMETERS</span></span>

### <span data-ttu-id="7a84b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a84b-118">-AsJob</span></span>
<span data-ttu-id="7a84b-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7a84b-119">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a84b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a84b-120">-DefaultProfile</span></span>
<span data-ttu-id="7a84b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a84b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a84b-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7a84b-122">-InputObject</span></span>
<span data-ttu-id="7a84b-123">Obiekt wejściowy puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="7a84b-123">The instance pool input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: InputObjectSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a84b-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7a84b-124">-LicenseType</span></span>
<span data-ttu-id="7a84b-125">Określa typ licencji, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="7a84b-125">Determines which License Type to use.</span></span>
<span data-ttu-id="7a84b-126">Możliwe wartości to BasePrice (z rabatem AHB) i LicenseIncluded (bez AHB rabatu).</span><span class="sxs-lookup"><span data-stu-id="7a84b-126">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a84b-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7a84b-127">-Name</span></span>
<span data-ttu-id="7a84b-128">Nazwa puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="7a84b-128">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a84b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a84b-129">-ResourceGroupName</span></span>
<span data-ttu-id="7a84b-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a84b-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a84b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a84b-131">-ResourceId</span></span>
<span data-ttu-id="7a84b-132">Identyfikator zasobu puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="7a84b-132">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a84b-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="7a84b-133">-Tag</span></span>
<span data-ttu-id="7a84b-134">Znaczniki, które mają zostać skojarzone z wystąpieniem</span><span class="sxs-lookup"><span data-stu-id="7a84b-134">The tags to associate with the instance</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a84b-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a84b-135">-Confirm</span></span>
<span data-ttu-id="7a84b-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a84b-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a84b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a84b-137">-WhatIf</span></span>
<span data-ttu-id="7a84b-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a84b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a84b-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7a84b-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a84b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a84b-140">CommonParameters</span></span>
<span data-ttu-id="7a84b-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a84b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a84b-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a84b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a84b-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a84b-143">INPUTS</span></span>

### <span data-ttu-id="7a84b-144">Microsoft.Azure.Commands.Sql.Instance_Pools. model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="7a84b-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="7a84b-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7a84b-145">System.String</span></span>

## <span data-ttu-id="7a84b-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a84b-146">OUTPUTS</span></span>

### <span data-ttu-id="7a84b-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="7a84b-147">System.Object</span></span>
## <span data-ttu-id="7a84b-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a84b-148">NOTES</span></span>

## <span data-ttu-id="7a84b-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a84b-149">RELATED LINKS</span></span>

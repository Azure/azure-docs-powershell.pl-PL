---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
ms.openlocfilehash: db7d9165b8aec6a69f31850f7a37eddb2450e53b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197627"
---
# <span data-ttu-id="d1d34-101">Set-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="d1d34-101">Set-AzSqlInstancePool</span></span>

## <span data-ttu-id="d1d34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1d34-102">SYNOPSIS</span></span>
<span data-ttu-id="d1d34-103">Ustawia właściwości puli wystąpień języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d1d34-103">Sets properties for an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="d1d34-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d1d34-104">SYNTAX</span></span>

### <span data-ttu-id="d1d34-105">DefaultSetInstancePoolParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d1d34-105">DefaultSetInstancePoolParameterSet (Default)</span></span>
```
Set-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1d34-106">InputObjectSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1d34-106">InputObjectSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1d34-107">ResourceIdSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1d34-107">ResourceIdSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-ResourceId] <String> [-LicenseType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1d34-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d1d34-108">DESCRIPTION</span></span>
<span data-ttu-id="d1d34-109">Polecenie **cmdlet Set-AzSqlInstancePool** modyfikuje właściwości puli wystąpień języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d1d34-109">The **Set-AzSqlInstancePool** cmdlet modifies properties of an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="d1d34-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d1d34-110">EXAMPLES</span></span>

### <span data-ttu-id="d1d34-111">Przykład 1. Ustawianie typu licencji puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="d1d34-111">Example 1 : Set an instance pool license type</span></span>
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

<span data-ttu-id="d1d34-112">To polecenie ustawia typ licencji i/lub tagi dla puli wystąpień o nazwie instancePool0.</span><span class="sxs-lookup"><span data-stu-id="d1d34-112">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

### <span data-ttu-id="d1d34-113">Przykład 2. Ustawianie typu licencji puli wystąpień przy użyciu obiektu puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="d1d34-113">Example 2 : Set an instance pool license type using an instance pool object</span></span>
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

<span data-ttu-id="d1d34-114">To polecenie ustawia typ licencji i/lub tagi puli wystąpień przy użyciu obiektu puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="d1d34-114">This command sets the license type and/or tags for an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="d1d34-115">Przykład 3. Ustawianie typu licencji puli wystąpień przy użyciu identyfikatora zasobu puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="d1d34-115">Example 3 : Set an instance pool license type using an instance pool resource id</span></span>
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

<span data-ttu-id="d1d34-116">To polecenie ustawia typ licencji i/lub tagi dla puli wystąpień o nazwie instancePool0.</span><span class="sxs-lookup"><span data-stu-id="d1d34-116">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

## <span data-ttu-id="d1d34-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1d34-117">PARAMETERS</span></span>

### <span data-ttu-id="d1d34-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d1d34-118">-AsJob</span></span>
<span data-ttu-id="d1d34-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d1d34-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1d34-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1d34-120">-DefaultProfile</span></span>
<span data-ttu-id="d1d34-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1d34-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1d34-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1d34-122">-InputObject</span></span>
<span data-ttu-id="d1d34-123">Obiekt wejściowy puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="d1d34-123">The instance pool input object.</span></span>

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

### <span data-ttu-id="d1d34-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d1d34-124">-LicenseType</span></span>
<span data-ttu-id="d1d34-125">Określa typ licencji, którego należy użyć.</span><span class="sxs-lookup"><span data-stu-id="d1d34-125">Determines which License Type to use.</span></span>
<span data-ttu-id="d1d34-126">Możliwe wartości to Cena Bazowa (z rabatem AHB) i LicenseIncluded (bez rabatu AHB).</span><span class="sxs-lookup"><span data-stu-id="d1d34-126">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="d1d34-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d1d34-127">-Name</span></span>
<span data-ttu-id="d1d34-128">Nazwa puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="d1d34-128">The name of the instance pool.</span></span>

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

### <span data-ttu-id="d1d34-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1d34-129">-ResourceGroupName</span></span>
<span data-ttu-id="d1d34-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d1d34-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="d1d34-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1d34-131">-ResourceId</span></span>
<span data-ttu-id="d1d34-132">Identyfikator zasobu puli wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="d1d34-132">The instance pool resource identifier.</span></span>

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

### <span data-ttu-id="d1d34-133">— Tag</span><span class="sxs-lookup"><span data-stu-id="d1d34-133">-Tag</span></span>
<span data-ttu-id="d1d34-134">Tagi do skojarzenia z wystąpieniem</span><span class="sxs-lookup"><span data-stu-id="d1d34-134">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="d1d34-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d1d34-135">-Confirm</span></span>
<span data-ttu-id="d1d34-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d1d34-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1d34-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1d34-137">-WhatIf</span></span>
<span data-ttu-id="d1d34-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1d34-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1d34-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d1d34-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1d34-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1d34-140">CommonParameters</span></span>
<span data-ttu-id="d1d34-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1d34-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1d34-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1d34-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1d34-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1d34-143">INPUTS</span></span>

### <span data-ttu-id="d1d34-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="d1d34-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="d1d34-145">System.String</span><span class="sxs-lookup"><span data-stu-id="d1d34-145">System.String</span></span>

## <span data-ttu-id="d1d34-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1d34-146">OUTPUTS</span></span>

### <span data-ttu-id="d1d34-147">System.Object</span><span class="sxs-lookup"><span data-stu-id="d1d34-147">System.Object</span></span>
## <span data-ttu-id="d1d34-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d1d34-148">NOTES</span></span>

## <span data-ttu-id="d1d34-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1d34-149">RELATED LINKS</span></span>

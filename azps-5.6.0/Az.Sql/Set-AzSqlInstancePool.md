---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
ms.openlocfilehash: 0d7efa268709d0691fe55bfaf322bd9accf79dab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997116"
---
# <span data-ttu-id="7ab88-101">Set-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="7ab88-101">Set-AzSqlInstancePool</span></span>

## <span data-ttu-id="7ab88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ab88-102">SYNOPSIS</span></span>
<span data-ttu-id="7ab88-103">Ustawia właściwości puli wystąpień języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7ab88-103">Sets properties for an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="7ab88-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7ab88-104">SYNTAX</span></span>

### <span data-ttu-id="7ab88-105">DefaultSetInstancePoolParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="7ab88-105">DefaultSetInstancePoolParameterSet (Default)</span></span>
```
Set-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ab88-106">InputObjectSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ab88-106">InputObjectSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ab88-107">ResourceIdSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ab88-107">ResourceIdSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-ResourceId] <String> [-LicenseType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ab88-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7ab88-108">DESCRIPTION</span></span>
<span data-ttu-id="7ab88-109">Polecenie **cmdlet Set-AzSqlInstancePool** modyfikuje właściwości puli wystąpień języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7ab88-109">The **Set-AzSqlInstancePool** cmdlet modifies properties of an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="7ab88-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7ab88-110">EXAMPLES</span></span>

### <span data-ttu-id="7ab88-111">Przykład 1. Ustawianie typu licencji puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="7ab88-111">Example 1 : Set an instance pool license type</span></span>
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

<span data-ttu-id="7ab88-112">To polecenie ustawia typ licencji i/lub tagi dla puli wystąpień o nazwie instancePool0.</span><span class="sxs-lookup"><span data-stu-id="7ab88-112">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

### <span data-ttu-id="7ab88-113">Przykład 2. Ustawianie typu licencji puli wystąpień przy użyciu obiektu puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="7ab88-113">Example 2 : Set an instance pool license type using an instance pool object</span></span>
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

<span data-ttu-id="7ab88-114">To polecenie ustawia typ licencji i/lub tagi puli wystąpień przy użyciu obiektu puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="7ab88-114">This command sets the license type and/or tags for an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="7ab88-115">Przykład 3. Ustawianie typu licencji puli wystąpień przy użyciu identyfikatora zasobu puli wystąpień</span><span class="sxs-lookup"><span data-stu-id="7ab88-115">Example 3 : Set an instance pool license type using an instance pool resource id</span></span>
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

<span data-ttu-id="7ab88-116">To polecenie ustawia typ licencji i/lub tagi dla puli wystąpień o nazwie instancePool0.</span><span class="sxs-lookup"><span data-stu-id="7ab88-116">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

## <span data-ttu-id="7ab88-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ab88-117">PARAMETERS</span></span>

### <span data-ttu-id="7ab88-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7ab88-118">-AsJob</span></span>
<span data-ttu-id="7ab88-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7ab88-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ab88-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ab88-120">-DefaultProfile</span></span>
<span data-ttu-id="7ab88-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ab88-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ab88-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ab88-122">-InputObject</span></span>
<span data-ttu-id="7ab88-123">Obiekt wejściowy puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="7ab88-123">The instance pool input object.</span></span>

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

### <span data-ttu-id="7ab88-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7ab88-124">-LicenseType</span></span>
<span data-ttu-id="7ab88-125">Określenie typu licencji, którego należy użyć.</span><span class="sxs-lookup"><span data-stu-id="7ab88-125">Determines which License Type to use.</span></span>
<span data-ttu-id="7ab88-126">Dopuszczalne wartości to Cena Bazowa (z rabatem AHB) i LicenseIncluded (bez rabatu AHB).</span><span class="sxs-lookup"><span data-stu-id="7ab88-126">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="7ab88-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7ab88-127">-Name</span></span>
<span data-ttu-id="7ab88-128">Nazwa puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="7ab88-128">The name of the instance pool.</span></span>

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

### <span data-ttu-id="7ab88-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ab88-129">-ResourceGroupName</span></span>
<span data-ttu-id="7ab88-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7ab88-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="7ab88-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ab88-131">-ResourceId</span></span>
<span data-ttu-id="7ab88-132">Identyfikator zasobu puli wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="7ab88-132">The instance pool resource identifier.</span></span>

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

### <span data-ttu-id="7ab88-133">— Tag</span><span class="sxs-lookup"><span data-stu-id="7ab88-133">-Tag</span></span>
<span data-ttu-id="7ab88-134">Tagi do skojarzenia z wystąpieniem</span><span class="sxs-lookup"><span data-stu-id="7ab88-134">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="7ab88-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ab88-135">-Confirm</span></span>
<span data-ttu-id="7ab88-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7ab88-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ab88-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ab88-137">-WhatIf</span></span>
<span data-ttu-id="7ab88-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ab88-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ab88-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7ab88-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ab88-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab88-140">CommonParameters</span></span>
<span data-ttu-id="7ab88-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ab88-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ab88-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ab88-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ab88-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ab88-143">INPUTS</span></span>

### <span data-ttu-id="7ab88-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="7ab88-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="7ab88-145">System.String</span><span class="sxs-lookup"><span data-stu-id="7ab88-145">System.String</span></span>

## <span data-ttu-id="7ab88-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ab88-146">OUTPUTS</span></span>

### <span data-ttu-id="7ab88-147">System.Object</span><span class="sxs-lookup"><span data-stu-id="7ab88-147">System.Object</span></span>
## <span data-ttu-id="7ab88-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7ab88-148">NOTES</span></span>

## <span data-ttu-id="7ab88-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ab88-149">RELATED LINKS</span></span>

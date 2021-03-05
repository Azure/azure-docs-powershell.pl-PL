---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 818e76c9ea46b2593b3bdd3871f417dbaca044a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977681"
---
# <span data-ttu-id="227ba-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="227ba-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="227ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="227ba-102">SYNOPSIS</span></span>
<span data-ttu-id="227ba-103">Tworzy pulę wystąpień języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="227ba-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="227ba-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="227ba-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="227ba-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="227ba-105">DESCRIPTION</span></span>
<span data-ttu-id="227ba-106">Polecenie **cmdlet New-AzSqlInstancePool** tworzy pulę wystąpień języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="227ba-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="227ba-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="227ba-107">EXAMPLES</span></span>

### <span data-ttu-id="227ba-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="227ba-108">Example 1</span></span>
```powershell
PS C:\> New-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0 -Location canadacentral -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -VCore 8 -Edition GeneralPurpose -ComputeGeneration Gen5 -LicenseType LicenseIncluded
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

<span data-ttu-id="227ba-109">To polecenie tworzy nową pulę wystąpień języka Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="227ba-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="227ba-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="227ba-110">PARAMETERS</span></span>

### <span data-ttu-id="227ba-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="227ba-111">-AsJob</span></span>
<span data-ttu-id="227ba-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="227ba-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="227ba-113">-Compute Zwyrodnienie</span><span class="sxs-lookup"><span data-stu-id="227ba-113">-ComputeGeneration</span></span>
<span data-ttu-id="227ba-114">Generowanie obliczeń dla puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="227ba-114">The compute generation for the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="227ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="227ba-115">-DefaultProfile</span></span>
<span data-ttu-id="227ba-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="227ba-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="227ba-117">— wersja</span><span class="sxs-lookup"><span data-stu-id="227ba-117">-Edition</span></span>
<span data-ttu-id="227ba-118">Wersja puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="227ba-118">The edition for the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="227ba-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="227ba-119">-LicenseType</span></span>
<span data-ttu-id="227ba-120">Określenie typu licencji, którego należy użyć.</span><span class="sxs-lookup"><span data-stu-id="227ba-120">Determines which License Type to use.</span></span>
<span data-ttu-id="227ba-121">Dopuszczalne wartości to Cena Bazowa (z rabatem AHB) i LicenseIncluded (bez rabatu AHB).</span><span class="sxs-lookup"><span data-stu-id="227ba-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="227ba-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="227ba-122">-Location</span></span>
<span data-ttu-id="227ba-123">Lokalizacja tworzenia puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="227ba-123">The location to create the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="227ba-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="227ba-124">-Name</span></span>
<span data-ttu-id="227ba-125">Nazwa puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="227ba-125">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="227ba-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="227ba-126">-ResourceGroupName</span></span>
<span data-ttu-id="227ba-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="227ba-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="227ba-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="227ba-128">-SubnetId</span></span>
<span data-ttu-id="227ba-129">Identyfikator podsieci do użycia na przykład podczas tworzenia puli.</span><span class="sxs-lookup"><span data-stu-id="227ba-129">The subnet id to use for instance pool creation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="227ba-130">— Tag</span><span class="sxs-lookup"><span data-stu-id="227ba-130">-Tag</span></span>
<span data-ttu-id="227ba-131">Tagi do skojarzenia z wystąpieniem</span><span class="sxs-lookup"><span data-stu-id="227ba-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="227ba-132">— VCore</span><span class="sxs-lookup"><span data-stu-id="227ba-132">-VCore</span></span>
<span data-ttu-id="227ba-133">Określa, ile vcore ma skojarzyć z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="227ba-133">Determines how much VCore to associate with instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: VCores

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="227ba-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="227ba-134">-Confirm</span></span>
<span data-ttu-id="227ba-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="227ba-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="227ba-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="227ba-136">-WhatIf</span></span>
<span data-ttu-id="227ba-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="227ba-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="227ba-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="227ba-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="227ba-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="227ba-139">CommonParameters</span></span>
<span data-ttu-id="227ba-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="227ba-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="227ba-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="227ba-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="227ba-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="227ba-142">INPUTS</span></span>

### <span data-ttu-id="227ba-143">Brak</span><span class="sxs-lookup"><span data-stu-id="227ba-143">None</span></span>

## <span data-ttu-id="227ba-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="227ba-144">OUTPUTS</span></span>

### <span data-ttu-id="227ba-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="227ba-145">System.Object</span></span>
## <span data-ttu-id="227ba-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="227ba-146">NOTES</span></span>

## <span data-ttu-id="227ba-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="227ba-147">RELATED LINKS</span></span>

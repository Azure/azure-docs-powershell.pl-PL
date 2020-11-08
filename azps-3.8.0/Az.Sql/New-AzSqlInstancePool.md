---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 1b4f405e9bf6377855439d1f6d3cad9f0538920f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051430"
---
# <span data-ttu-id="24f02-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="24f02-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="24f02-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24f02-102">SYNOPSIS</span></span>
<span data-ttu-id="24f02-103">Tworzy pulę wystąpień SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="24f02-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="24f02-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24f02-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24f02-105">Opis</span><span class="sxs-lookup"><span data-stu-id="24f02-105">DESCRIPTION</span></span>
<span data-ttu-id="24f02-106">Polecenie cmdlet **New-AzSqlInstancePool** tworzy pulę wystąpień SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="24f02-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="24f02-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24f02-107">EXAMPLES</span></span>

### <span data-ttu-id="24f02-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="24f02-108">Example 1</span></span>
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

<span data-ttu-id="24f02-109">To polecenie tworzy nową pulę wystąpień usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="24f02-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="24f02-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24f02-110">PARAMETERS</span></span>

### <span data-ttu-id="24f02-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24f02-111">-AsJob</span></span>
<span data-ttu-id="24f02-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="24f02-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24f02-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="24f02-113">-ComputeGeneration</span></span>
<span data-ttu-id="24f02-114">Generowanie obliczeń dla puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="24f02-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="24f02-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24f02-115">-DefaultProfile</span></span>
<span data-ttu-id="24f02-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="24f02-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24f02-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="24f02-117">-Edition</span></span>
<span data-ttu-id="24f02-118">Wersja puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="24f02-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="24f02-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="24f02-119">-LicenseType</span></span>
<span data-ttu-id="24f02-120">Określa typ licencji, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="24f02-120">Determines which License Type to use.</span></span>
<span data-ttu-id="24f02-121">Możliwe wartości to BasePrice (z rabatem AHB) i LicenseIncluded (bez AHB rabatu).</span><span class="sxs-lookup"><span data-stu-id="24f02-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="24f02-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="24f02-122">-Location</span></span>
<span data-ttu-id="24f02-123">Lokalizacja, w której ma zostać utworzona Pula wystąpień.</span><span class="sxs-lookup"><span data-stu-id="24f02-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="24f02-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="24f02-124">-Name</span></span>
<span data-ttu-id="24f02-125">Nazwa puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="24f02-125">The name of the instance pool.</span></span>

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

### <span data-ttu-id="24f02-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24f02-126">-ResourceGroupName</span></span>
<span data-ttu-id="24f02-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="24f02-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="24f02-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="24f02-128">-SubnetId</span></span>
<span data-ttu-id="24f02-129">Identyfikator podsieci, który ma być używany do tworzenia puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="24f02-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="24f02-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="24f02-130">-Tag</span></span>
<span data-ttu-id="24f02-131">Znaczniki, które mają zostać skojarzone z wystąpieniem</span><span class="sxs-lookup"><span data-stu-id="24f02-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="24f02-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="24f02-132">-VCore</span></span>
<span data-ttu-id="24f02-133">Określa, ile VCore ma być kojarzona z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="24f02-133">Determines how much VCore to associate with instance.</span></span>

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

### <span data-ttu-id="24f02-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24f02-134">-Confirm</span></span>
<span data-ttu-id="24f02-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24f02-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24f02-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24f02-136">-WhatIf</span></span>
<span data-ttu-id="24f02-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24f02-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24f02-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="24f02-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24f02-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24f02-139">CommonParameters</span></span>
<span data-ttu-id="24f02-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24f02-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24f02-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24f02-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24f02-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24f02-142">INPUTS</span></span>

### <span data-ttu-id="24f02-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="24f02-143">None</span></span>

## <span data-ttu-id="24f02-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24f02-144">OUTPUTS</span></span>

### <span data-ttu-id="24f02-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="24f02-145">System.Object</span></span>
## <span data-ttu-id="24f02-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24f02-146">NOTES</span></span>

## <span data-ttu-id="24f02-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24f02-147">RELATED LINKS</span></span>

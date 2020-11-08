---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 1b4f405e9bf6377855439d1f6d3cad9f0538920f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063112"
---
# <span data-ttu-id="0a311-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="0a311-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="0a311-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a311-102">SYNOPSIS</span></span>
<span data-ttu-id="0a311-103">Tworzy pulę wystąpień SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0a311-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="0a311-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a311-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a311-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0a311-105">DESCRIPTION</span></span>
<span data-ttu-id="0a311-106">Polecenie cmdlet **New-AzSqlInstancePool** tworzy pulę wystąpień SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0a311-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="0a311-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a311-107">EXAMPLES</span></span>

### <span data-ttu-id="0a311-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0a311-108">Example 1</span></span>
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

<span data-ttu-id="0a311-109">To polecenie tworzy nową pulę wystąpień usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0a311-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="0a311-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a311-110">PARAMETERS</span></span>

### <span data-ttu-id="0a311-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a311-111">-AsJob</span></span>
<span data-ttu-id="0a311-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0a311-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a311-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="0a311-113">-ComputeGeneration</span></span>
<span data-ttu-id="0a311-114">Generowanie obliczeń dla puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="0a311-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="0a311-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a311-115">-DefaultProfile</span></span>
<span data-ttu-id="0a311-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0a311-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a311-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="0a311-117">-Edition</span></span>
<span data-ttu-id="0a311-118">Wersja puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="0a311-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="0a311-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0a311-119">-LicenseType</span></span>
<span data-ttu-id="0a311-120">Określa typ licencji, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="0a311-120">Determines which License Type to use.</span></span>
<span data-ttu-id="0a311-121">Możliwe wartości to BasePrice (z rabatem AHB) i LicenseIncluded (bez AHB rabatu).</span><span class="sxs-lookup"><span data-stu-id="0a311-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="0a311-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0a311-122">-Location</span></span>
<span data-ttu-id="0a311-123">Lokalizacja, w której ma zostać utworzona Pula wystąpień.</span><span class="sxs-lookup"><span data-stu-id="0a311-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="0a311-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0a311-124">-Name</span></span>
<span data-ttu-id="0a311-125">Nazwa puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="0a311-125">The name of the instance pool.</span></span>

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

### <span data-ttu-id="0a311-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a311-126">-ResourceGroupName</span></span>
<span data-ttu-id="0a311-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0a311-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="0a311-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0a311-128">-SubnetId</span></span>
<span data-ttu-id="0a311-129">Identyfikator podsieci, który ma być używany do tworzenia puli wystąpień.</span><span class="sxs-lookup"><span data-stu-id="0a311-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="0a311-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="0a311-130">-Tag</span></span>
<span data-ttu-id="0a311-131">Znaczniki, które mają zostać skojarzone z wystąpieniem</span><span class="sxs-lookup"><span data-stu-id="0a311-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="0a311-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="0a311-132">-VCore</span></span>
<span data-ttu-id="0a311-133">Określa, ile VCore ma być kojarzona z wystąpieniem.</span><span class="sxs-lookup"><span data-stu-id="0a311-133">Determines how much VCore to associate with instance.</span></span>

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

### <span data-ttu-id="0a311-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0a311-134">-Confirm</span></span>
<span data-ttu-id="0a311-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a311-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a311-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a311-136">-WhatIf</span></span>
<span data-ttu-id="0a311-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a311-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a311-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0a311-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a311-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a311-139">CommonParameters</span></span>
<span data-ttu-id="0a311-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a311-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a311-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a311-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a311-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a311-142">INPUTS</span></span>

### <span data-ttu-id="0a311-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0a311-143">None</span></span>

## <span data-ttu-id="0a311-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a311-144">OUTPUTS</span></span>

### <span data-ttu-id="0a311-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="0a311-145">System.Object</span></span>
## <span data-ttu-id="0a311-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a311-146">NOTES</span></span>

## <span data-ttu-id="0a311-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a311-147">RELATED LINKS</span></span>

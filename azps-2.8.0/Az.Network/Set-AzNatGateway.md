---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: 40a1d9c77d870971f8aa432735f556e89ad55e0d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871064"
---
# <span data-ttu-id="cd7fb-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cd7fb-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="cd7fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd7fb-102">SYNOPSIS</span></span>
<span data-ttu-id="cd7fb-103">Zaktualizuj zasób bramy NAT za pomocą publicznego adresu IP, prefiksu publicznego adresu IP i IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="cd7fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd7fb-104">SYNTAX</span></span>

### <span data-ttu-id="cd7fb-105">SetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cd7fb-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd7fb-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd7fb-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd7fb-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd7fb-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd7fb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cd7fb-108">DESCRIPTION</span></span>
<span data-ttu-id="cd7fb-109">Zaktualizuj zasób bramy NAT za pomocą publicznego adresu IP, prefiksu publicznego adresu IP i IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="cd7fb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd7fb-110">EXAMPLES</span></span>

### <span data-ttu-id="cd7fb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cd7fb-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="cd7fb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd7fb-112">PARAMETERS</span></span>

### <span data-ttu-id="cd7fb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd7fb-113">-AsJob</span></span>
<span data-ttu-id="cd7fb-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cd7fb-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd7fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd7fb-115">-DefaultProfile</span></span>
<span data-ttu-id="cd7fb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd7fb-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="cd7fb-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="cd7fb-118">Limit czasu bezczynności bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-118">The idle timeout of the nat gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd7fb-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cd7fb-119">-InputObject</span></span>
<span data-ttu-id="cd7fb-120">Określa zasób bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-120">Specifies Nat Gateway Resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd7fb-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cd7fb-121">-Name</span></span>
<span data-ttu-id="cd7fb-122">Nazwa zasobu bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-122">Name of the Nat Gateway Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd7fb-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cd7fb-123">-PublicIpAddress</span></span>
<span data-ttu-id="cd7fb-124">Tablica publicznych adresów IP skojarzonych z zasobem bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd7fb-125">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cd7fb-125">-PublicIpPrefix</span></span>
<span data-ttu-id="cd7fb-126">Tablica prefiksów publicznych adresów IP skojarzonych z zasobem bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd7fb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd7fb-127">-ResourceGroupName</span></span>
<span data-ttu-id="cd7fb-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-128">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd7fb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd7fb-129">-ResourceId</span></span>
<span data-ttu-id="cd7fb-130">Określa identyfikator zasobu bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-130">Specifies the Id of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd7fb-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd7fb-131">-Confirm</span></span>
<span data-ttu-id="cd7fb-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd7fb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd7fb-133">-WhatIf</span></span>
<span data-ttu-id="cd7fb-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd7fb-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd7fb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd7fb-136">CommonParameters</span></span>
<span data-ttu-id="cd7fb-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd7fb-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd7fb-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd7fb-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd7fb-139">INPUTS</span></span>

### <span data-ttu-id="cd7fb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="cd7fb-140">System.String</span></span>

### <span data-ttu-id="cd7fb-141">Microsoft. Azure. Commands. Network. models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="cd7fb-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="cd7fb-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd7fb-142">OUTPUTS</span></span>

### <span data-ttu-id="cd7fb-143">Microsoft. Azure. Commands. Network. models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="cd7fb-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="cd7fb-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd7fb-144">NOTES</span></span>

## <span data-ttu-id="cd7fb-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd7fb-145">RELATED LINKS</span></span>

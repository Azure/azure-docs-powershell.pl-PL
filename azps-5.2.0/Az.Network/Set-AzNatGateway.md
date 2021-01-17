---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: fe19aba38402519a77185062ac6192d6ff9915eb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345862"
---
# <span data-ttu-id="6fda2-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6fda2-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="6fda2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6fda2-102">SYNOPSIS</span></span>
<span data-ttu-id="6fda2-103">Zaktualizuj zasób bramy NAT za pomocą publicznego adresu IP, prefiksu publicznego adresu IP i IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="6fda2-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="6fda2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6fda2-104">SYNTAX</span></span>

### <span data-ttu-id="6fda2-105">SetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6fda2-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fda2-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fda2-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6fda2-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fda2-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fda2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6fda2-108">DESCRIPTION</span></span>
<span data-ttu-id="6fda2-109">Zaktualizuj zasób bramy NAT za pomocą publicznego adresu IP, prefiksu publicznego adresu IP i IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="6fda2-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="6fda2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6fda2-110">EXAMPLES</span></span>

### <span data-ttu-id="6fda2-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6fda2-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="6fda2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6fda2-112">PARAMETERS</span></span>

### <span data-ttu-id="6fda2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6fda2-113">-AsJob</span></span>
<span data-ttu-id="6fda2-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6fda2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6fda2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fda2-115">-DefaultProfile</span></span>
<span data-ttu-id="6fda2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fda2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fda2-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="6fda2-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="6fda2-118">Limit czasu bezczynności bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="6fda2-118">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="6fda2-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6fda2-119">-InputObject</span></span>
<span data-ttu-id="6fda2-120">Określa zasób bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="6fda2-120">Specifies Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="6fda2-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6fda2-121">-Name</span></span>
<span data-ttu-id="6fda2-122">Nazwa zasobu bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="6fda2-122">Name of the Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="6fda2-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6fda2-123">-PublicIpAddress</span></span>
<span data-ttu-id="6fda2-124">Tablica publicznych adresów IP skojarzonych z zasobem bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="6fda2-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="6fda2-125">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6fda2-125">-PublicIpPrefix</span></span>
<span data-ttu-id="6fda2-126">Tablica prefiksów publicznych adresów IP skojarzonych z zasobem bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="6fda2-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="6fda2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fda2-127">-ResourceGroupName</span></span>
<span data-ttu-id="6fda2-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6fda2-128">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="6fda2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fda2-129">-ResourceId</span></span>
<span data-ttu-id="6fda2-130">Określa identyfikator zasobu bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="6fda2-130">Specifies the Id of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="6fda2-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6fda2-131">-Confirm</span></span>
<span data-ttu-id="6fda2-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fda2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fda2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fda2-133">-WhatIf</span></span>
<span data-ttu-id="6fda2-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fda2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fda2-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6fda2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fda2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fda2-136">CommonParameters</span></span>
<span data-ttu-id="6fda2-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fda2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fda2-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fda2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fda2-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fda2-139">INPUTS</span></span>

### <span data-ttu-id="6fda2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6fda2-140">System.String</span></span>

### <span data-ttu-id="6fda2-141">Microsoft. Azure. Commands. Network. models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="6fda2-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="6fda2-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6fda2-142">OUTPUTS</span></span>

### <span data-ttu-id="6fda2-143">Microsoft. Azure. Commands. Network. models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="6fda2-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="6fda2-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6fda2-144">NOTES</span></span>

## <span data-ttu-id="6fda2-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fda2-145">RELATED LINKS</span></span>

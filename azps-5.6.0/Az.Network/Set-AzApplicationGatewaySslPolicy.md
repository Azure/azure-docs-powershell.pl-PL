---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 689e678bf740590f3d5d749124b74a38742395b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986735"
---
# <span data-ttu-id="5c998-101">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5c998-101">Set-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="5c998-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c998-102">SYNOPSIS</span></span>
<span data-ttu-id="5c998-103">Modyfikuje zasady SSL bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5c998-103">Modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="5c998-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5c998-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-DisabledSslProtocols <String[]>]
 [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c998-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5c998-105">DESCRIPTION</span></span>
<span data-ttu-id="5c998-106">Polecenie **cmdlet Set-AzApplicationGatewaySslPolicy** modyfikuje zasady SSL bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5c998-106">The **Set-AzApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="5c998-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5c998-107">EXAMPLES</span></span>

### <span data-ttu-id="5c998-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5c998-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="5c998-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 i zapisuje ją w zmiennej $AppGw aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5c998-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5c998-110">To drugie polecenie modyfikuje zasady ssl na zasady o typie Wstępnie zdefiniowane i nazwa zasad AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="5c998-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="5c998-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c998-111">PARAMETERS</span></span>

### <span data-ttu-id="5c998-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c998-112">-ApplicationGateway</span></span>
<span data-ttu-id="5c998-113">Określa bramę aplikacji zasad SSL, które to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="5c998-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c998-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="5c998-114">-CipherSuite</span></span>
<span data-ttu-id="5c998-115">Pakiety szyfrowania ssl, które mają być włączone w określonej kolejności dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="5c998-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c998-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c998-116">-DefaultProfile</span></span>
<span data-ttu-id="5c998-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5c998-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c998-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="5c998-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="5c998-119">Określa, które protokoły są wyłączone.</span><span class="sxs-lookup"><span data-stu-id="5c998-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="5c998-120">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5c998-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5c998-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="5c998-121">TLSv1_0</span></span> 
- <span data-ttu-id="5c998-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="5c998-122">TLSv1_1</span></span> 
- <span data-ttu-id="5c998-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="5c998-123">TLSv1_2</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c998-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="5c998-124">-MinProtocolVersion</span></span>
<span data-ttu-id="5c998-125">Minimalna wersja protokołu Ssl, która ma być obsługiwana przez bramę aplikacji</span><span class="sxs-lookup"><span data-stu-id="5c998-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c998-126">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="5c998-126">-PolicyName</span></span>
<span data-ttu-id="5c998-127">Nazwa wstępnie zdefiniowanych zasad SSL</span><span class="sxs-lookup"><span data-stu-id="5c998-127">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="5c998-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="5c998-128">-PolicyType</span></span>
<span data-ttu-id="5c998-129">Typ zasad SSL</span><span class="sxs-lookup"><span data-stu-id="5c998-129">Type of Ssl Policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c998-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5c998-130">-Confirm</span></span>
<span data-ttu-id="5c998-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5c998-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c998-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c998-132">-WhatIf</span></span>
<span data-ttu-id="5c998-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c998-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c998-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5c998-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c998-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c998-135">CommonParameters</span></span>
<span data-ttu-id="5c998-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c998-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c998-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c998-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c998-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c998-138">INPUTS</span></span>

### <span data-ttu-id="5c998-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c998-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5c998-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c998-140">OUTPUTS</span></span>

### <span data-ttu-id="5c998-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c998-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5c998-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5c998-142">NOTES</span></span>
* <span data-ttu-id="5c998-143">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="5c998-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="5c998-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c998-144">RELATED LINKS</span></span>

[<span data-ttu-id="5c998-145">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5c998-145">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="5c998-146">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5c998-146">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)



---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 984556937e57d710b9f62d80f20f7f30955865ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543247"
---
# <span data-ttu-id="89d88-101">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="89d88-101">Set-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="89d88-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89d88-102">SYNOPSIS</span></span>
<span data-ttu-id="89d88-103">Modyfikuje zasady SSL bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="89d88-103">Modifies the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89d88-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89d88-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89d88-105">Opis</span><span class="sxs-lookup"><span data-stu-id="89d88-105">DESCRIPTION</span></span>
<span data-ttu-id="89d88-106">Polecenie cmdlet **Set-AzureRmApplicationGatewaySslPolicy** modyfikuje zasady SSL bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="89d88-106">The **Set-AzureRmApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="89d88-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89d88-107">EXAMPLES</span></span>

### <span data-ttu-id="89d88-108">1:1</span><span class="sxs-lookup"><span data-stu-id="89d88-108">1:</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="89d88-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="89d88-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="89d88-110">To drugie polecenie modyfikuje zasady SSL do wstępnie zdefiniowanego typu zasad i nazwy zasad AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="89d88-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="89d88-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89d88-111">PARAMETERS</span></span>

### <span data-ttu-id="89d88-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89d88-112">-ApplicationGateway</span></span>
<span data-ttu-id="89d88-113">Określa bramę aplikacji dla zasad SSL, która jest modyfikowana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89d88-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="89d88-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="89d88-114">-CipherSuite</span></span>
<span data-ttu-id="89d88-115">Mechanizmy szyfrowania SSL są włączone w określonej kolejności dla bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="89d88-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d88-116">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="89d88-116">-DisabledSslProtocols</span></span>
<span data-ttu-id="89d88-117">Określa, które protokoły są wyłączone.</span><span class="sxs-lookup"><span data-stu-id="89d88-117">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="89d88-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="89d88-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="89d88-119">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="89d88-119">TLSv1_0</span></span> 
- <span data-ttu-id="89d88-120">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="89d88-120">TLSv1_1</span></span> 
- <span data-ttu-id="89d88-121">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="89d88-121">TLSv1_2</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d88-122">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="89d88-122">-MinProtocolVersion</span></span>
<span data-ttu-id="89d88-123">Minimalna wersja protokołu SSL, która ma być obsługiwana w bramie aplikacji</span><span class="sxs-lookup"><span data-stu-id="89d88-123">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="89d88-124">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="89d88-124">-PolicyName</span></span>
<span data-ttu-id="89d88-125">Nazwa wstępnie zdefiniowanych zasad SSL</span><span class="sxs-lookup"><span data-stu-id="89d88-125">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="89d88-126">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="89d88-126">-PolicyType</span></span>
<span data-ttu-id="89d88-127">Typ zasad SSL</span><span class="sxs-lookup"><span data-stu-id="89d88-127">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="89d88-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="89d88-128">-Confirm</span></span>
<span data-ttu-id="89d88-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89d88-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89d88-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89d88-130">-WhatIf</span></span>
<span data-ttu-id="89d88-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89d88-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89d88-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="89d88-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89d88-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89d88-133">-DefaultProfile</span></span>
<span data-ttu-id="89d88-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="89d88-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d88-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89d88-135">CommonParameters</span></span>
<span data-ttu-id="89d88-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89d88-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89d88-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89d88-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89d88-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89d88-138">INPUTS</span></span>

### <span data-ttu-id="89d88-139">System. String</span><span class="sxs-lookup"><span data-stu-id="89d88-139">System.String</span></span>

## <span data-ttu-id="89d88-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89d88-140">OUTPUTS</span></span>

### <span data-ttu-id="89d88-141">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89d88-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="89d88-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89d88-142">NOTES</span></span>
* <span data-ttu-id="89d88-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="89d88-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="89d88-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89d88-144">RELATED LINKS</span></span>

[<span data-ttu-id="89d88-145">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="89d88-145">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="89d88-146">Nowe — AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="89d88-146">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 07958bcab5948280774ff3e056f7c34c9f6b0aac
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892817"
---
# <span data-ttu-id="81ab3-101">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="81ab3-101">Set-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="81ab3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="81ab3-103">Modyfikuje zasady SSL bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="81ab3-103">Modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="81ab3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81ab3-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81ab3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="81ab3-105">DESCRIPTION</span></span>
<span data-ttu-id="81ab3-106">Polecenie cmdlet **Set-AzApplicationGatewaySslPolicy** modyfikuje zasady SSL bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="81ab3-106">The **Set-AzApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="81ab3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81ab3-107">EXAMPLES</span></span>

### <span data-ttu-id="81ab3-108">1:1</span><span class="sxs-lookup"><span data-stu-id="81ab3-108">1:</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="81ab3-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="81ab3-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="81ab3-110">To drugie polecenie modyfikuje zasady SSL do wstępnie zdefiniowanego typu zasad i nazwy zasad AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="81ab3-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="81ab3-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81ab3-111">PARAMETERS</span></span>

### <span data-ttu-id="81ab3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81ab3-112">-ApplicationGateway</span></span>
<span data-ttu-id="81ab3-113">Określa bramę aplikacji dla zasad SSL, która jest modyfikowana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81ab3-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81ab3-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="81ab3-114">-CipherSuite</span></span>
<span data-ttu-id="81ab3-115">Mechanizmy szyfrowania SSL są włączone w określonej kolejności dla bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="81ab3-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="81ab3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81ab3-116">-DefaultProfile</span></span>
<span data-ttu-id="81ab3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="81ab3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81ab3-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="81ab3-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="81ab3-119">Określa, które protokoły są wyłączone.</span><span class="sxs-lookup"><span data-stu-id="81ab3-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="81ab3-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="81ab3-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="81ab3-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="81ab3-121">TLSv1_0</span></span> 
- <span data-ttu-id="81ab3-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="81ab3-122">TLSv1_1</span></span> 
- <span data-ttu-id="81ab3-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="81ab3-123">TLSv1_2</span></span>

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

### <span data-ttu-id="81ab3-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="81ab3-124">-MinProtocolVersion</span></span>
<span data-ttu-id="81ab3-125">Minimalna wersja protokołu SSL, która ma być obsługiwana w bramie aplikacji</span><span class="sxs-lookup"><span data-stu-id="81ab3-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81ab3-126">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="81ab3-126">-PolicyName</span></span>
<span data-ttu-id="81ab3-127">Nazwa wstępnie zdefiniowanych zasad SSL</span><span class="sxs-lookup"><span data-stu-id="81ab3-127">Name of Ssl predefined policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81ab3-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="81ab3-128">-PolicyType</span></span>
<span data-ttu-id="81ab3-129">Typ zasad SSL</span><span class="sxs-lookup"><span data-stu-id="81ab3-129">Type of Ssl Policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81ab3-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="81ab3-130">-Confirm</span></span>
<span data-ttu-id="81ab3-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81ab3-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81ab3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81ab3-132">-WhatIf</span></span>
<span data-ttu-id="81ab3-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81ab3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81ab3-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="81ab3-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81ab3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81ab3-135">CommonParameters</span></span>
<span data-ttu-id="81ab3-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81ab3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81ab3-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81ab3-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81ab3-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81ab3-138">INPUTS</span></span>

### <span data-ttu-id="81ab3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="81ab3-139">System.String</span></span>

## <span data-ttu-id="81ab3-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81ab3-140">OUTPUTS</span></span>

### <span data-ttu-id="81ab3-141">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81ab3-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="81ab3-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81ab3-142">NOTES</span></span>
* <span data-ttu-id="81ab3-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="81ab3-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="81ab3-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81ab3-144">RELATED LINKS</span></span>

[<span data-ttu-id="81ab3-145">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="81ab3-145">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="81ab3-146">Nowe — AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="81ab3-146">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)



---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslpolicy
schema: 2.0.0
ms.openlocfilehash: 6c28665f35a7422a731aefd4ccf1c4ecabc549d4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897582"
---
# <span data-ttu-id="ef04b-101">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="ef04b-101">New-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="ef04b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ef04b-102">SYNOPSIS</span></span>
<span data-ttu-id="ef04b-103">Tworzy zasady SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ef04b-103">Creates an SSL policy for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef04b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ef04b-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslPolicy
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef04b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ef04b-105">DESCRIPTION</span></span>
<span data-ttu-id="ef04b-106">Polecenie cmdlet **New-AzureRmApplicationGatewaySslPolicy** tworzy zasady SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ef04b-106">The **New-AzureRmApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="ef04b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ef04b-107">EXAMPLES</span></span>

### <span data-ttu-id="ef04b-108">1:1</span><span class="sxs-lookup"><span data-stu-id="ef04b-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzureRmApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="ef04b-109">To polecenie tworzy zasadę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="ef04b-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="ef04b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ef04b-110">PARAMETERS</span></span>

### <span data-ttu-id="ef04b-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="ef04b-111">-CipherSuite</span></span>
<span data-ttu-id="ef04b-112">Mechanizmy szyfrowania SSL są włączone w określonej kolejności dla bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ef04b-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="ef04b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef04b-113">-DefaultProfile</span></span>
<span data-ttu-id="ef04b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef04b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef04b-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="ef04b-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="ef04b-116">Określa, które protokoły są wyłączone.</span><span class="sxs-lookup"><span data-stu-id="ef04b-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="ef04b-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ef04b-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ef04b-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="ef04b-118">TLSv1_0</span></span> 
- <span data-ttu-id="ef04b-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="ef04b-119">TLSv1_1</span></span> 
- <span data-ttu-id="ef04b-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="ef04b-120">TLSv1_2</span></span>

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

### <span data-ttu-id="ef04b-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="ef04b-121">-MinProtocolVersion</span></span>
<span data-ttu-id="ef04b-122">Minimalna wersja protokołu SSL, która ma być obsługiwana w bramie aplikacji</span><span class="sxs-lookup"><span data-stu-id="ef04b-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="ef04b-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="ef04b-123">-PolicyName</span></span>
<span data-ttu-id="ef04b-124">Nazwa wstępnie zdefiniowanych zasad SSL</span><span class="sxs-lookup"><span data-stu-id="ef04b-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="ef04b-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="ef04b-125">-PolicyType</span></span>
<span data-ttu-id="ef04b-126">Typ zasad SSL</span><span class="sxs-lookup"><span data-stu-id="ef04b-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="ef04b-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ef04b-127">-Confirm</span></span>
<span data-ttu-id="ef04b-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef04b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef04b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef04b-129">-WhatIf</span></span>
<span data-ttu-id="ef04b-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef04b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef04b-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ef04b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef04b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef04b-132">CommonParameters</span></span>
<span data-ttu-id="ef04b-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef04b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef04b-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef04b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef04b-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef04b-135">INPUTS</span></span>

### <span data-ttu-id="ef04b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ef04b-136">System.String</span></span>

## <span data-ttu-id="ef04b-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ef04b-137">OUTPUTS</span></span>

### <span data-ttu-id="ef04b-138">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="ef04b-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="ef04b-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ef04b-139">NOTES</span></span>
* <span data-ttu-id="ef04b-140">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="ef04b-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ef04b-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef04b-141">RELATED LINKS</span></span>

[<span data-ttu-id="ef04b-142">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="ef04b-142">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="ef04b-143">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="ef04b-143">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)



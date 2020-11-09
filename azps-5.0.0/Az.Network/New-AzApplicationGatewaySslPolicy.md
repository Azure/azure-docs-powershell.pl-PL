---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: cf2f2ef91fa217b1710eeb100f4e3e6c2ce6fb9d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318006"
---
# <span data-ttu-id="97a7a-101">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="97a7a-101">New-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="97a7a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="97a7a-102">SYNOPSIS</span></span>
<span data-ttu-id="97a7a-103">Tworzy zasady SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="97a7a-103">Creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="97a7a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="97a7a-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslPolicy [-DisabledSslProtocols <String[]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97a7a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="97a7a-105">DESCRIPTION</span></span>
<span data-ttu-id="97a7a-106">Polecenie cmdlet **New-AzApplicationGatewaySslPolicy** tworzy zasady SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="97a7a-106">The **New-AzApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="97a7a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="97a7a-107">EXAMPLES</span></span>

### <span data-ttu-id="97a7a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="97a7a-108">Example 1</span></span>
```powershell
PS C:\>$sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="97a7a-109">To polecenie tworzy zasadę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="97a7a-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="97a7a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="97a7a-110">PARAMETERS</span></span>

### <span data-ttu-id="97a7a-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="97a7a-111">-CipherSuite</span></span>
<span data-ttu-id="97a7a-112">Mechanizmy szyfrowania SSL są włączone w określonej kolejności dla bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="97a7a-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="97a7a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a7a-113">-DefaultProfile</span></span>
<span data-ttu-id="97a7a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="97a7a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97a7a-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="97a7a-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="97a7a-116">Określa, które protokoły są wyłączone.</span><span class="sxs-lookup"><span data-stu-id="97a7a-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="97a7a-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="97a7a-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="97a7a-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="97a7a-118">TLSv1_0</span></span> 
- <span data-ttu-id="97a7a-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="97a7a-119">TLSv1_1</span></span> 
- <span data-ttu-id="97a7a-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="97a7a-120">TLSv1_2</span></span>

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

### <span data-ttu-id="97a7a-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="97a7a-121">-MinProtocolVersion</span></span>
<span data-ttu-id="97a7a-122">Minimalna wersja protokołu SSL, która ma być obsługiwana w bramie aplikacji</span><span class="sxs-lookup"><span data-stu-id="97a7a-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="97a7a-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="97a7a-123">-PolicyName</span></span>
<span data-ttu-id="97a7a-124">Nazwa wstępnie zdefiniowanych zasad SSL</span><span class="sxs-lookup"><span data-stu-id="97a7a-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="97a7a-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="97a7a-125">-PolicyType</span></span>
<span data-ttu-id="97a7a-126">Typ zasad SSL</span><span class="sxs-lookup"><span data-stu-id="97a7a-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="97a7a-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="97a7a-127">-Confirm</span></span>
<span data-ttu-id="97a7a-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97a7a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97a7a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97a7a-129">-WhatIf</span></span>
<span data-ttu-id="97a7a-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97a7a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97a7a-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="97a7a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97a7a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a7a-132">CommonParameters</span></span>
<span data-ttu-id="97a7a-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97a7a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a7a-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97a7a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a7a-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97a7a-135">INPUTS</span></span>

### <span data-ttu-id="97a7a-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="97a7a-136">None</span></span>

## <span data-ttu-id="97a7a-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="97a7a-137">OUTPUTS</span></span>

### <span data-ttu-id="97a7a-138">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="97a7a-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="97a7a-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="97a7a-139">NOTES</span></span>
* <span data-ttu-id="97a7a-140">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="97a7a-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="97a7a-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97a7a-141">RELATED LINKS</span></span>

[<span data-ttu-id="97a7a-142">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="97a7a-142">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="97a7a-143">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="97a7a-143">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bf11b2b3010a7f7683d670c3c5e95d4248b83cd6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890386"
---
# <span data-ttu-id="e94f3-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e94f3-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="e94f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e94f3-102">SYNOPSIS</span></span>
<span data-ttu-id="e94f3-103">Usuwa certyfikat uwierzytelniania z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e94f3-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="e94f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e94f3-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e94f3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e94f3-105">DESCRIPTION</span></span>
<span data-ttu-id="e94f3-106">Polecenie cmdlet **Remove-AzApplicationGatewayAuthenticationCertificate** usuwa certyfikat uwierzytelniania z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e94f3-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="e94f3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e94f3-107">EXAMPLES</span></span>

### <span data-ttu-id="e94f3-108">1:1</span><span class="sxs-lookup"><span data-stu-id="e94f3-108">1:</span></span>
```

```

## <span data-ttu-id="e94f3-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e94f3-109">PARAMETERS</span></span>

### <span data-ttu-id="e94f3-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e94f3-110">-ApplicationGateway</span></span>
<span data-ttu-id="e94f3-111">Określa nazwę bramy aplikacji, z której to polecenie cmdlet usuwa certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="e94f3-111">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="e94f3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e94f3-112">-DefaultProfile</span></span>
<span data-ttu-id="e94f3-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e94f3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e94f3-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e94f3-114">-Name</span></span>
<span data-ttu-id="e94f3-115">Określa nazwę certyfikatu uwierzytelniania, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e94f3-115">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94f3-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e94f3-116">-Confirm</span></span>
<span data-ttu-id="e94f3-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e94f3-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e94f3-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e94f3-118">-WhatIf</span></span>
<span data-ttu-id="e94f3-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e94f3-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e94f3-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e94f3-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e94f3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e94f3-121">CommonParameters</span></span>
<span data-ttu-id="e94f3-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e94f3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e94f3-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e94f3-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e94f3-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e94f3-124">INPUTS</span></span>

### <span data-ttu-id="e94f3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e94f3-125">System.String</span></span>

## <span data-ttu-id="e94f3-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e94f3-126">OUTPUTS</span></span>

### <span data-ttu-id="e94f3-127">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e94f3-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e94f3-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e94f3-128">NOTES</span></span>
* <span data-ttu-id="e94f3-129">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="e94f3-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e94f3-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e94f3-130">RELATED LINKS</span></span>

[<span data-ttu-id="e94f3-131">Dodaj-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e94f3-131">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="e94f3-132">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e94f3-132">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="e94f3-133">Nowe — AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e94f3-133">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="e94f3-134">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e94f3-134">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)



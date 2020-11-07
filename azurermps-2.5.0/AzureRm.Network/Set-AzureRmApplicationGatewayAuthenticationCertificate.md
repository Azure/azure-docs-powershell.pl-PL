---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 3c70fcd0e04b566ff1cd3297525d3ed2c9ed95ba
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899207"
---
# <span data-ttu-id="276b6-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="276b6-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="276b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="276b6-102">SYNOPSIS</span></span>
<span data-ttu-id="276b6-103">Aktualizuje certyfikat uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="276b6-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="276b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="276b6-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="276b6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="276b6-105">DESCRIPTION</span></span>
<span data-ttu-id="276b6-106">Polecenie cmdlet **Set-AzureRmApplicationGatewayAuthenticationCertificate** aktualizuje certyfikat uwierzytelniania dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="276b6-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="276b6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="276b6-107">EXAMPLES</span></span>

### <span data-ttu-id="276b6-108">1:1</span><span class="sxs-lookup"><span data-stu-id="276b6-108">1:</span></span>
```

```

## <span data-ttu-id="276b6-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="276b6-109">PARAMETERS</span></span>

### <span data-ttu-id="276b6-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="276b6-110">-ApplicationGateway</span></span>
<span data-ttu-id="276b6-111">Określa nazwę bramy aplikacji, dla której to polecenie cmdlet aktualizuje certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="276b6-111">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="276b6-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="276b6-112">-CertificateFile</span></span>
<span data-ttu-id="276b6-113">Określa ścieżkę pliku certyfikatu uwierzytelniania, z którym ten aplet polecenia aktualizuje certyfikat.</span><span class="sxs-lookup"><span data-stu-id="276b6-113">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="276b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="276b6-114">-DefaultProfile</span></span>
<span data-ttu-id="276b6-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="276b6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="276b6-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="276b6-116">-Name</span></span>
<span data-ttu-id="276b6-117">Określa nazwę certyfikatu uwierzytelniania, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="276b6-117">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="276b6-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="276b6-118">-Confirm</span></span>
<span data-ttu-id="276b6-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="276b6-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="276b6-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="276b6-120">-WhatIf</span></span>
<span data-ttu-id="276b6-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="276b6-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="276b6-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="276b6-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="276b6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="276b6-123">CommonParameters</span></span>
<span data-ttu-id="276b6-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="276b6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="276b6-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="276b6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="276b6-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="276b6-126">INPUTS</span></span>

### <span data-ttu-id="276b6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="276b6-127">System.String</span></span>

## <span data-ttu-id="276b6-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="276b6-128">OUTPUTS</span></span>

### <span data-ttu-id="276b6-129">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="276b6-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="276b6-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="276b6-130">NOTES</span></span>
* <span data-ttu-id="276b6-131">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="276b6-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="276b6-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="276b6-132">RELATED LINKS</span></span>

[<span data-ttu-id="276b6-133">Dodaj-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="276b6-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="276b6-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="276b6-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="276b6-135">Nowe — AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="276b6-135">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="276b6-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="276b6-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)



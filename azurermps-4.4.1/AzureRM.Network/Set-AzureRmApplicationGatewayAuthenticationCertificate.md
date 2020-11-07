---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: a71ba6f6d9b45e0016589d5629f029998f33963f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719616"
---
# <span data-ttu-id="0415d-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0415d-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="0415d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0415d-102">SYNOPSIS</span></span>
<span data-ttu-id="0415d-103">Aktualizuje certyfikat uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0415d-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0415d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0415d-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0415d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0415d-105">DESCRIPTION</span></span>
<span data-ttu-id="0415d-106">Polecenie cmdlet **Set-AzureRmApplicationGatewayAuthenticationCertificate** aktualizuje certyfikat uwierzytelniania dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0415d-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="0415d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0415d-107">EXAMPLES</span></span>

## <span data-ttu-id="0415d-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0415d-108">PARAMETERS</span></span>

### <span data-ttu-id="0415d-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0415d-109">-ApplicationGateway</span></span>
<span data-ttu-id="0415d-110">Określa nazwę bramy aplikacji, dla której to polecenie cmdlet aktualizuje certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="0415d-110">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="0415d-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="0415d-111">-CertificateFile</span></span>
<span data-ttu-id="0415d-112">Określa ścieżkę pliku certyfikatu uwierzytelniania, z którym ten aplet polecenia aktualizuje certyfikat.</span><span class="sxs-lookup"><span data-stu-id="0415d-112">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="0415d-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0415d-113">-Name</span></span>
<span data-ttu-id="0415d-114">Określa nazwę certyfikatu uwierzytelniania, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0415d-114">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="0415d-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0415d-115">-Confirm</span></span>
<span data-ttu-id="0415d-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0415d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0415d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0415d-117">-WhatIf</span></span>
<span data-ttu-id="0415d-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0415d-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0415d-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0415d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0415d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0415d-120">-DefaultProfile</span></span>
<span data-ttu-id="0415d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0415d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0415d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0415d-122">CommonParameters</span></span>
<span data-ttu-id="0415d-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0415d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0415d-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0415d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0415d-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0415d-125">INPUTS</span></span>

### <span data-ttu-id="0415d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0415d-126">System.String</span></span>

## <span data-ttu-id="0415d-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0415d-127">OUTPUTS</span></span>

### <span data-ttu-id="0415d-128">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0415d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0415d-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0415d-129">NOTES</span></span>
* <span data-ttu-id="0415d-130">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="0415d-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="0415d-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0415d-131">RELATED LINKS</span></span>

[<span data-ttu-id="0415d-132">Dodaj-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0415d-132">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="0415d-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0415d-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="0415d-134">Nowe — AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0415d-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="0415d-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0415d-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)



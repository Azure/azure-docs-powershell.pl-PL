---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 8b19edba06f41d4e1e7cf3c95dd1a52fa00f09e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551212"
---
# <span data-ttu-id="daf8f-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="daf8f-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="daf8f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="daf8f-102">SYNOPSIS</span></span>
<span data-ttu-id="daf8f-103">Dodaje certyfikat uwierzytelniania do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="daf8f-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="daf8f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="daf8f-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="daf8f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="daf8f-105">DESCRIPTION</span></span>
<span data-ttu-id="daf8f-106">Polecenie cmdlet **Add-AzureRmApplicationGatewayAuthenticationCertificate** dodaje certyfikat uwierzytelniania do bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="daf8f-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="daf8f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="daf8f-107">EXAMPLES</span></span>

## <span data-ttu-id="daf8f-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="daf8f-108">PARAMETERS</span></span>

### <span data-ttu-id="daf8f-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daf8f-109">-ApplicationGateway</span></span>
<span data-ttu-id="daf8f-110">Określa nazwę bramy aplikacji, dla której to polecenie cmdlet dodaje certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="daf8f-110">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="daf8f-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="daf8f-111">-CertificateFile</span></span>
<span data-ttu-id="daf8f-112">Określa ścieżkę certyfikatu uwierzytelniania, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daf8f-112">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="daf8f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daf8f-113">-DefaultProfile</span></span>
<span data-ttu-id="daf8f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="daf8f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="daf8f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="daf8f-115">-Name</span></span>
<span data-ttu-id="daf8f-116">Określa nazwę certyfikatu, który jest dodawany przez to polecenie cmdlet do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="daf8f-116">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="daf8f-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="daf8f-117">-Confirm</span></span>
<span data-ttu-id="daf8f-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daf8f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daf8f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daf8f-119">-WhatIf</span></span>
<span data-ttu-id="daf8f-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daf8f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daf8f-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="daf8f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daf8f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf8f-122">CommonParameters</span></span>
<span data-ttu-id="daf8f-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daf8f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf8f-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daf8f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf8f-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="daf8f-125">INPUTS</span></span>

### <span data-ttu-id="daf8f-126">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daf8f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="daf8f-127">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="daf8f-127">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="daf8f-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="daf8f-128">OUTPUTS</span></span>

### <span data-ttu-id="daf8f-129">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daf8f-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="daf8f-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="daf8f-130">NOTES</span></span>
* <span data-ttu-id="daf8f-131">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="daf8f-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="daf8f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="daf8f-132">RELATED LINKS</span></span>

[<span data-ttu-id="daf8f-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="daf8f-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="daf8f-134">Nowe — AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="daf8f-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="daf8f-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="daf8f-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="daf8f-136">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="daf8f-136">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)



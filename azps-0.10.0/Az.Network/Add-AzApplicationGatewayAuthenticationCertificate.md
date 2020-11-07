---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 6652da4491bc503ecc2d0c8ee016416cefbff172
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891045"
---
# <span data-ttu-id="7cf50-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7cf50-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="7cf50-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7cf50-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf50-103">Dodaje certyfikat uwierzytelniania do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7cf50-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="7cf50-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7cf50-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7cf50-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7cf50-105">DESCRIPTION</span></span>
<span data-ttu-id="7cf50-106">Polecenie cmdlet **Add-AzApplicationGatewayAuthenticationCertificate** dodaje certyfikat uwierzytelniania do bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf50-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="7cf50-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7cf50-107">EXAMPLES</span></span>

### <span data-ttu-id="7cf50-108">1:1</span><span class="sxs-lookup"><span data-stu-id="7cf50-108">1:</span></span>
```

```

## <span data-ttu-id="7cf50-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7cf50-109">PARAMETERS</span></span>

### <span data-ttu-id="7cf50-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7cf50-110">-ApplicationGateway</span></span>
<span data-ttu-id="7cf50-111">Określa nazwę bramy aplikacji, dla której to polecenie cmdlet dodaje certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="7cf50-111">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="7cf50-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="7cf50-112">-CertificateFile</span></span>
<span data-ttu-id="7cf50-113">Określa ścieżkę certyfikatu uwierzytelniania, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf50-113">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="7cf50-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf50-114">-DefaultProfile</span></span>
<span data-ttu-id="7cf50-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf50-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cf50-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7cf50-116">-Name</span></span>
<span data-ttu-id="7cf50-117">Określa nazwę certyfikatu, który jest dodawany przez to polecenie cmdlet do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7cf50-117">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="7cf50-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7cf50-118">-Confirm</span></span>
<span data-ttu-id="7cf50-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf50-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cf50-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf50-120">-WhatIf</span></span>
<span data-ttu-id="7cf50-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf50-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cf50-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7cf50-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cf50-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf50-123">CommonParameters</span></span>
<span data-ttu-id="7cf50-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf50-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf50-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cf50-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf50-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7cf50-126">INPUTS</span></span>

### <span data-ttu-id="7cf50-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7cf50-127">System.String</span></span>

## <span data-ttu-id="7cf50-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7cf50-128">OUTPUTS</span></span>

### <span data-ttu-id="7cf50-129">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7cf50-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7cf50-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7cf50-130">NOTES</span></span>
* <span data-ttu-id="7cf50-131">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="7cf50-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7cf50-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7cf50-132">RELATED LINKS</span></span>

[<span data-ttu-id="7cf50-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7cf50-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7cf50-134">Nowe — AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7cf50-134">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7cf50-135">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7cf50-135">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7cf50-136">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7cf50-136">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)



---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 4d664018592f05203c684a896f0a0701940301a6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898737"
---
# <span data-ttu-id="e5543-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e5543-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="e5543-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e5543-102">SYNOPSIS</span></span>
<span data-ttu-id="e5543-103">Dodaje certyfikat uwierzytelniania do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e5543-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5543-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e5543-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5543-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e5543-105">DESCRIPTION</span></span>
<span data-ttu-id="e5543-106">Polecenie cmdlet **Add-AzureRmApplicationGatewayAuthenticationCertificate** dodaje certyfikat uwierzytelniania do bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e5543-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="e5543-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e5543-107">EXAMPLES</span></span>

### <span data-ttu-id="e5543-108">1:1</span><span class="sxs-lookup"><span data-stu-id="e5543-108">1:</span></span>
```

```

## <span data-ttu-id="e5543-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e5543-109">PARAMETERS</span></span>

### <span data-ttu-id="e5543-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5543-110">-ApplicationGateway</span></span>
<span data-ttu-id="e5543-111">Określa nazwę bramy aplikacji, dla której to polecenie cmdlet dodaje certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="e5543-111">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="e5543-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="e5543-112">-CertificateFile</span></span>
<span data-ttu-id="e5543-113">Określa ścieżkę certyfikatu uwierzytelniania, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5543-113">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="e5543-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5543-114">-DefaultProfile</span></span>
<span data-ttu-id="e5543-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5543-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5543-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e5543-116">-Name</span></span>
<span data-ttu-id="e5543-117">Określa nazwę certyfikatu, który jest dodawany przez to polecenie cmdlet do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e5543-117">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="e5543-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e5543-118">-Confirm</span></span>
<span data-ttu-id="e5543-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5543-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5543-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5543-120">-WhatIf</span></span>
<span data-ttu-id="e5543-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5543-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5543-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e5543-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5543-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5543-123">CommonParameters</span></span>
<span data-ttu-id="e5543-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5543-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5543-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5543-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5543-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5543-126">INPUTS</span></span>

### <span data-ttu-id="e5543-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e5543-127">System.String</span></span>

## <span data-ttu-id="e5543-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e5543-128">OUTPUTS</span></span>

### <span data-ttu-id="e5543-129">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5543-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e5543-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e5543-130">NOTES</span></span>
* <span data-ttu-id="e5543-131">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="e5543-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e5543-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5543-132">RELATED LINKS</span></span>

[<span data-ttu-id="e5543-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e5543-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="e5543-134">Nowe — AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e5543-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="e5543-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e5543-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="e5543-136">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e5543-136">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)



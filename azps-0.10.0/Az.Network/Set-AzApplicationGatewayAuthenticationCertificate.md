---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 23b337779da46169be29e3dd6fef55fc70f4f035
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892874"
---
# <span data-ttu-id="7989e-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7989e-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="7989e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7989e-102">SYNOPSIS</span></span>
<span data-ttu-id="7989e-103">Aktualizuje certyfikat uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7989e-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="7989e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7989e-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7989e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7989e-105">DESCRIPTION</span></span>
<span data-ttu-id="7989e-106">Polecenie cmdlet **Set-AzApplicationGatewayAuthenticationCertificate** aktualizuje certyfikat uwierzytelniania dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7989e-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="7989e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7989e-107">EXAMPLES</span></span>

### <span data-ttu-id="7989e-108">1:1</span><span class="sxs-lookup"><span data-stu-id="7989e-108">1:</span></span>
```

```

## <span data-ttu-id="7989e-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7989e-109">PARAMETERS</span></span>

### <span data-ttu-id="7989e-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7989e-110">-ApplicationGateway</span></span>
<span data-ttu-id="7989e-111">Określa nazwę bramy aplikacji, dla której to polecenie cmdlet aktualizuje certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="7989e-111">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="7989e-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="7989e-112">-CertificateFile</span></span>
<span data-ttu-id="7989e-113">Określa ścieżkę pliku certyfikatu uwierzytelniania, z którym ten aplet polecenia aktualizuje certyfikat.</span><span class="sxs-lookup"><span data-stu-id="7989e-113">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="7989e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7989e-114">-DefaultProfile</span></span>
<span data-ttu-id="7989e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7989e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7989e-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7989e-116">-Name</span></span>
<span data-ttu-id="7989e-117">Określa nazwę certyfikatu uwierzytelniania, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7989e-117">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="7989e-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7989e-118">-Confirm</span></span>
<span data-ttu-id="7989e-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7989e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7989e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7989e-120">-WhatIf</span></span>
<span data-ttu-id="7989e-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7989e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7989e-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7989e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7989e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7989e-123">CommonParameters</span></span>
<span data-ttu-id="7989e-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7989e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7989e-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7989e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7989e-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7989e-126">INPUTS</span></span>

### <span data-ttu-id="7989e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7989e-127">System.String</span></span>

## <span data-ttu-id="7989e-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7989e-128">OUTPUTS</span></span>

### <span data-ttu-id="7989e-129">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7989e-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7989e-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7989e-130">NOTES</span></span>
* <span data-ttu-id="7989e-131">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="7989e-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7989e-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7989e-132">RELATED LINKS</span></span>

[<span data-ttu-id="7989e-133">Dodaj-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7989e-133">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7989e-134">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7989e-134">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7989e-135">Nowe — AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7989e-135">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7989e-136">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7989e-136">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)



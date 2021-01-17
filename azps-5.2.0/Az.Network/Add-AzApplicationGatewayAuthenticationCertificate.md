---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 687752d74e13030cd954736132dba845c2c55127
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335281"
---
# <span data-ttu-id="02415-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="02415-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="02415-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02415-102">SYNOPSIS</span></span>
<span data-ttu-id="02415-103">Dodaje certyfikat uwierzytelniania do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="02415-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="02415-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02415-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02415-105">Opis</span><span class="sxs-lookup"><span data-stu-id="02415-105">DESCRIPTION</span></span>
<span data-ttu-id="02415-106">Polecenie cmdlet **Add-AzApplicationGatewayAuthenticationCertificate** dodaje certyfikat uwierzytelniania do bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="02415-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="02415-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02415-107">EXAMPLES</span></span>

### <span data-ttu-id="02415-108">Przykład 1: Dodawanie certyfikatu uwierzytelniania do bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="02415-108">Example 1: Add authentication certificate to an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="02415-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie appGwName i zapisuje ją w zmiennej $appgw.</span><span class="sxs-lookup"><span data-stu-id="02415-109">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="02415-110">Drugie polecenie dodaje certyfikat uwierzytelniania o nazwie cert01 do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="02415-110">The second command adds authentication certificate named cert01 to the application gateway.</span></span>
<span data-ttu-id="02415-111">W trzecim poleceniu jest aktualizowana Brama Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="02415-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="02415-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02415-112">PARAMETERS</span></span>

### <span data-ttu-id="02415-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="02415-113">-ApplicationGateway</span></span>
<span data-ttu-id="02415-114">Określa nazwę bramy aplikacji, dla której to polecenie cmdlet dodaje certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="02415-114">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="02415-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="02415-115">-CertificateFile</span></span>
<span data-ttu-id="02415-116">Określa ścieżkę certyfikatu uwierzytelniania, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02415-116">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="02415-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02415-117">-DefaultProfile</span></span>
<span data-ttu-id="02415-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="02415-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02415-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="02415-119">-Name</span></span>
<span data-ttu-id="02415-120">Określa nazwę certyfikatu, który jest dodawany przez to polecenie cmdlet do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="02415-120">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="02415-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02415-121">-Confirm</span></span>
<span data-ttu-id="02415-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02415-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02415-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02415-123">-WhatIf</span></span>
<span data-ttu-id="02415-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02415-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02415-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="02415-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02415-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02415-126">CommonParameters</span></span>
<span data-ttu-id="02415-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02415-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02415-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02415-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02415-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02415-129">INPUTS</span></span>

### <span data-ttu-id="02415-130">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="02415-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="02415-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02415-131">OUTPUTS</span></span>

### <span data-ttu-id="02415-132">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="02415-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="02415-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02415-133">NOTES</span></span>
* <span data-ttu-id="02415-134">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="02415-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="02415-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02415-135">RELATED LINKS</span></span>

[<span data-ttu-id="02415-136">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="02415-136">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="02415-137">Nowe — AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="02415-137">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="02415-138">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="02415-138">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="02415-139">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="02415-139">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)



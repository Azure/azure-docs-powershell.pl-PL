---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 5af778b84981b5b15acaa688bd8ad1702e5ab7e3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319105"
---
# <span data-ttu-id="69276-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="69276-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="69276-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69276-102">SYNOPSIS</span></span>
<span data-ttu-id="69276-103">Aktualizuje certyfikat uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="69276-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="69276-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69276-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69276-105">Opis</span><span class="sxs-lookup"><span data-stu-id="69276-105">DESCRIPTION</span></span>
<span data-ttu-id="69276-106">Polecenie cmdlet **Set-AzApplicationGatewayAuthenticationCertificate** aktualizuje certyfikat uwierzytelniania dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="69276-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="69276-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69276-107">EXAMPLES</span></span>

### <span data-ttu-id="69276-108">Przykład 1: aktualizowanie certyfikatu uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="69276-108">Example 1: Update an authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert2.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="69276-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie appGwName i zapisuje wynik w zmiennej $appgw.</span><span class="sxs-lookup"><span data-stu-id="69276-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="69276-110">Drugie polecenie aktualizuje certyfikat uwierzytelniania o nazwie cert01 w bramie Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="69276-110">The second command updates the authentication certificate named cert01 in the application gateway.</span></span>
<span data-ttu-id="69276-111">W trzecim poleceniu jest aktualizowana Brama Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="69276-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="69276-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69276-112">PARAMETERS</span></span>

### <span data-ttu-id="69276-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="69276-113">-ApplicationGateway</span></span>
<span data-ttu-id="69276-114">Określa nazwę bramy aplikacji, dla której to polecenie cmdlet aktualizuje certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="69276-114">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="69276-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="69276-115">-CertificateFile</span></span>
<span data-ttu-id="69276-116">Określa ścieżkę pliku certyfikatu uwierzytelniania, z którym ten aplet polecenia aktualizuje certyfikat.</span><span class="sxs-lookup"><span data-stu-id="69276-116">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="69276-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69276-117">-DefaultProfile</span></span>
<span data-ttu-id="69276-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="69276-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69276-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="69276-119">-Name</span></span>
<span data-ttu-id="69276-120">Określa nazwę certyfikatu uwierzytelniania, który jest aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69276-120">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="69276-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69276-121">-Confirm</span></span>
<span data-ttu-id="69276-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69276-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69276-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69276-123">-WhatIf</span></span>
<span data-ttu-id="69276-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69276-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69276-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="69276-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69276-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69276-126">CommonParameters</span></span>
<span data-ttu-id="69276-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69276-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69276-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69276-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69276-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69276-129">INPUTS</span></span>

### <span data-ttu-id="69276-130">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="69276-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="69276-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69276-131">OUTPUTS</span></span>

### <span data-ttu-id="69276-132">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="69276-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="69276-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69276-133">NOTES</span></span>
* <span data-ttu-id="69276-134">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="69276-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="69276-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69276-135">RELATED LINKS</span></span>

[<span data-ttu-id="69276-136">Dodaj-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="69276-136">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="69276-137">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="69276-137">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="69276-138">Nowe — AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="69276-138">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="69276-139">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="69276-139">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)



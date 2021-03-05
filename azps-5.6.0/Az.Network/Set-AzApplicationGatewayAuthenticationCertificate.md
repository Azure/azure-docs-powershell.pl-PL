---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: a060ddde57fc3d0cfadde487a147b8743acd5fbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003505"
---
# <span data-ttu-id="aae04-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="aae04-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="aae04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aae04-102">SYNOPSIS</span></span>
<span data-ttu-id="aae04-103">Aktualizuje certyfikat uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="aae04-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="aae04-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="aae04-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aae04-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="aae04-105">DESCRIPTION</span></span>
<span data-ttu-id="aae04-106">Polecenie **cmdlet Set-AzApplicationGatewayAuthenticationCertificate** aktualizuje certyfikat uwierzytelniania dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="aae04-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="aae04-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="aae04-107">EXAMPLES</span></span>

### <span data-ttu-id="aae04-108">Przykład 1. Aktualizowanie certyfikatu uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="aae04-108">Example 1: Update an authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert2.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="aae04-109">Pierwsze polecenie pobiera nazwę bramy aplikacji appGwName i zapisuje wynik w $appgw zmienną.</span><span class="sxs-lookup"><span data-stu-id="aae04-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="aae04-110">Drugie polecenie aktualizuje certyfikat uwierzytelniania o nazwie cert01 w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="aae04-110">The second command updates the authentication certificate named cert01 in the application gateway.</span></span>
<span data-ttu-id="aae04-111">Trzecie polecenie aktualizuje bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="aae04-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="aae04-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aae04-112">PARAMETERS</span></span>

### <span data-ttu-id="aae04-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aae04-113">-ApplicationGateway</span></span>
<span data-ttu-id="aae04-114">Określa nazwę bramy aplikacji, dla której to polecenie cmdlet aktualizuje certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="aae04-114">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="aae04-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="aae04-115">-CertificateFile</span></span>
<span data-ttu-id="aae04-116">Określa ścieżkę pliku certyfikatu uwierzytelniania, za pomocą którego to polecenie cmdlet aktualizuje certyfikat.</span><span class="sxs-lookup"><span data-stu-id="aae04-116">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="aae04-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aae04-117">-DefaultProfile</span></span>
<span data-ttu-id="aae04-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="aae04-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aae04-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="aae04-119">-Name</span></span>
<span data-ttu-id="aae04-120">Określa nazwę certyfikatu uwierzytelniania, który będzie aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aae04-120">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="aae04-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aae04-121">-Confirm</span></span>
<span data-ttu-id="aae04-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="aae04-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aae04-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aae04-123">-WhatIf</span></span>
<span data-ttu-id="aae04-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aae04-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aae04-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="aae04-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aae04-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aae04-126">CommonParameters</span></span>
<span data-ttu-id="aae04-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aae04-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aae04-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aae04-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aae04-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aae04-129">INPUTS</span></span>

### <span data-ttu-id="aae04-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aae04-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="aae04-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aae04-131">OUTPUTS</span></span>

### <span data-ttu-id="aae04-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aae04-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="aae04-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="aae04-133">NOTES</span></span>
* <span data-ttu-id="aae04-134">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="aae04-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="aae04-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aae04-135">RELATED LINKS</span></span>

[<span data-ttu-id="aae04-136">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="aae04-136">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="aae04-137">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="aae04-137">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="aae04-138">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="aae04-138">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="aae04-139">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="aae04-139">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)



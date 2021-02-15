---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 687752d74e13030cd954736132dba845c2c55127
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203275"
---
# <span data-ttu-id="247b5-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="247b5-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="247b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="247b5-102">SYNOPSIS</span></span>
<span data-ttu-id="247b5-103">Dodaje certyfikat uwierzytelniania do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="247b5-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="247b5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="247b5-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="247b5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="247b5-105">DESCRIPTION</span></span>
<span data-ttu-id="247b5-106">Polecenie **cmdlet Add-AzApplicationGatewayAuthenticationCertificate** dodaje certyfikat uwierzytelniania do bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="247b5-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="247b5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="247b5-107">EXAMPLES</span></span>

### <span data-ttu-id="247b5-108">Przykład 1. Dodawanie certyfikatu uwierzytelniania do bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="247b5-108">Example 1: Add authentication certificate to an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="247b5-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie appGwName i przechowuje ją w $appgw zmienną.</span><span class="sxs-lookup"><span data-stu-id="247b5-109">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="247b5-110">Drugie polecenie dodaje certyfikat uwierzytelniania o nazwie cert01 do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="247b5-110">The second command adds authentication certificate named cert01 to the application gateway.</span></span>
<span data-ttu-id="247b5-111">Trzecie polecenie aktualizuje bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="247b5-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="247b5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="247b5-112">PARAMETERS</span></span>

### <span data-ttu-id="247b5-113">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="247b5-113">-ApplicationGateway</span></span>
<span data-ttu-id="247b5-114">Określa nazwę bramy aplikacji, dla której to polecenie cmdlet dodaje certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="247b5-114">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="247b5-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="247b5-115">-CertificateFile</span></span>
<span data-ttu-id="247b5-116">Określa ścieżkę certyfikatu uwierzytelniania, który dodaje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="247b5-116">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="247b5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="247b5-117">-DefaultProfile</span></span>
<span data-ttu-id="247b5-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="247b5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="247b5-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="247b5-119">-Name</span></span>
<span data-ttu-id="247b5-120">Określa nazwę certyfikatu, który to polecenie cmdlet dodaje do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="247b5-120">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="247b5-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="247b5-121">-Confirm</span></span>
<span data-ttu-id="247b5-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="247b5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="247b5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="247b5-123">-WhatIf</span></span>
<span data-ttu-id="247b5-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="247b5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="247b5-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="247b5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="247b5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="247b5-126">CommonParameters</span></span>
<span data-ttu-id="247b5-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="247b5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="247b5-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="247b5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="247b5-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="247b5-129">INPUTS</span></span>

### <span data-ttu-id="247b5-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="247b5-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="247b5-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="247b5-131">OUTPUTS</span></span>

### <span data-ttu-id="247b5-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="247b5-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="247b5-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="247b5-133">NOTES</span></span>
* <span data-ttu-id="247b5-134">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="247b5-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="247b5-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="247b5-135">RELATED LINKS</span></span>

[<span data-ttu-id="247b5-136">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="247b5-136">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="247b5-137">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="247b5-137">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="247b5-138">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="247b5-138">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="247b5-139">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="247b5-139">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)



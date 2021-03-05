---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: c4c2c2041c6bf21aa6bf8b13055d0dac5ffbc64a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010417"
---
# <span data-ttu-id="cd0fa-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="cd0fa-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="cd0fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd0fa-102">SYNOPSIS</span></span>
<span data-ttu-id="cd0fa-103">Tworzy certyfikat uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cd0fa-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="cd0fa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cd0fa-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd0fa-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cd0fa-105">DESCRIPTION</span></span>
<span data-ttu-id="cd0fa-106">Polecenie **cmdlet New-AzApplicationGatewayAuthenticationCertificate** tworzy certyfikat uwierzytelniania dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cd0fa-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="cd0fa-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cd0fa-107">EXAMPLES</span></span>

### <span data-ttu-id="cd0fa-108">Przykład 1. Tworzenie certyfikatu uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="cd0fa-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="cd0fa-109">Pierwsze polecenie tworzy certyfikat uwierzytelniania o nazwie cert01.</span><span class="sxs-lookup"><span data-stu-id="cd0fa-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="cd0fa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd0fa-110">PARAMETERS</span></span>

### <span data-ttu-id="cd0fa-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="cd0fa-111">-CertificateFile</span></span>
<span data-ttu-id="cd0fa-112">Określa ścieżkę certyfikatu uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="cd0fa-112">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="cd0fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd0fa-113">-DefaultProfile</span></span>
<span data-ttu-id="cd0fa-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd0fa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd0fa-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cd0fa-115">-Name</span></span>
<span data-ttu-id="cd0fa-116">Określa nazwę certyfikatu uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="cd0fa-116">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="cd0fa-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd0fa-117">-Confirm</span></span>
<span data-ttu-id="cd0fa-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cd0fa-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd0fa-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd0fa-119">-WhatIf</span></span>
<span data-ttu-id="cd0fa-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd0fa-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd0fa-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cd0fa-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd0fa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd0fa-122">CommonParameters</span></span>
<span data-ttu-id="cd0fa-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd0fa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd0fa-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd0fa-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd0fa-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd0fa-125">INPUTS</span></span>

### <span data-ttu-id="cd0fa-126">Brak</span><span class="sxs-lookup"><span data-stu-id="cd0fa-126">None</span></span>

## <span data-ttu-id="cd0fa-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd0fa-127">OUTPUTS</span></span>

### <span data-ttu-id="cd0fa-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="cd0fa-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="cd0fa-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cd0fa-129">NOTES</span></span>
* <span data-ttu-id="cd0fa-130">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="cd0fa-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="cd0fa-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd0fa-131">RELATED LINKS</span></span>

[<span data-ttu-id="cd0fa-132">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="cd0fa-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="cd0fa-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="cd0fa-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="cd0fa-134">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="cd0fa-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="cd0fa-135">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="cd0fa-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)



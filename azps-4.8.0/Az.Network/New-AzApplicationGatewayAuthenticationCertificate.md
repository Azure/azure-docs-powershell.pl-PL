---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: c43fe72f8f3669b7e6e123a7f1d606771b161084
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223847"
---
# <span data-ttu-id="d2cab-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d2cab-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="d2cab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2cab-102">SYNOPSIS</span></span>
<span data-ttu-id="d2cab-103">Tworzy certyfikat uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d2cab-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="d2cab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2cab-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2cab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d2cab-105">DESCRIPTION</span></span>
<span data-ttu-id="d2cab-106">Polecenie cmdlet **New-AzApplicationGatewayAuthenticationCertificate** tworzy certyfikat uwierzytelniania dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d2cab-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="d2cab-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2cab-107">EXAMPLES</span></span>

### <span data-ttu-id="d2cab-108">Przykład 1: Tworzenie certyfikatu uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="d2cab-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="d2cab-109">Pierwsze polecenie tworzy certyfikat uwierzytelniania o nazwie cert01.</span><span class="sxs-lookup"><span data-stu-id="d2cab-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="d2cab-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2cab-110">PARAMETERS</span></span>

### <span data-ttu-id="d2cab-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="d2cab-111">-CertificateFile</span></span>
<span data-ttu-id="d2cab-112">Określa ścieżkę certyfikatu uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="d2cab-112">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="d2cab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2cab-113">-DefaultProfile</span></span>
<span data-ttu-id="d2cab-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2cab-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2cab-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d2cab-115">-Name</span></span>
<span data-ttu-id="d2cab-116">Określa nazwę certyfikatu uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="d2cab-116">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="d2cab-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d2cab-117">-Confirm</span></span>
<span data-ttu-id="d2cab-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2cab-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2cab-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2cab-119">-WhatIf</span></span>
<span data-ttu-id="d2cab-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2cab-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2cab-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d2cab-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2cab-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2cab-122">CommonParameters</span></span>
<span data-ttu-id="d2cab-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2cab-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2cab-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2cab-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2cab-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2cab-125">INPUTS</span></span>

### <span data-ttu-id="d2cab-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d2cab-126">None</span></span>

## <span data-ttu-id="d2cab-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2cab-127">OUTPUTS</span></span>

### <span data-ttu-id="d2cab-128">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d2cab-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="d2cab-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2cab-129">NOTES</span></span>
* <span data-ttu-id="d2cab-130">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="d2cab-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d2cab-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2cab-131">RELATED LINKS</span></span>

[<span data-ttu-id="d2cab-132">Dodaj-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d2cab-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d2cab-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d2cab-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d2cab-134">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d2cab-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d2cab-135">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d2cab-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)



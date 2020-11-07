---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 8f3685fddf4796cd0ad500c261f157e8ac5b95f5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890601"
---
# <span data-ttu-id="47292-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="47292-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="47292-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47292-102">SYNOPSIS</span></span>
<span data-ttu-id="47292-103">Tworzy certyfikat uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="47292-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="47292-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47292-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47292-105">Opis</span><span class="sxs-lookup"><span data-stu-id="47292-105">DESCRIPTION</span></span>
<span data-ttu-id="47292-106">Polecenie cmdlet **New-AzApplicationGatewayAuthenticationCertificate** tworzy certyfikat uwierzytelniania dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="47292-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="47292-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47292-107">EXAMPLES</span></span>

### <span data-ttu-id="47292-108">1:1</span><span class="sxs-lookup"><span data-stu-id="47292-108">1:</span></span>
```

```

## <span data-ttu-id="47292-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47292-109">PARAMETERS</span></span>

### <span data-ttu-id="47292-110">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="47292-110">-CertificateFile</span></span>
<span data-ttu-id="47292-111">Określa ścieżkę certyfikatu uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="47292-111">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="47292-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47292-112">-DefaultProfile</span></span>
<span data-ttu-id="47292-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="47292-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47292-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="47292-114">-Name</span></span>
<span data-ttu-id="47292-115">Określa nazwę certyfikatu uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="47292-115">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="47292-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="47292-116">-Confirm</span></span>
<span data-ttu-id="47292-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47292-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47292-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47292-118">-WhatIf</span></span>
<span data-ttu-id="47292-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47292-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47292-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="47292-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47292-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47292-121">CommonParameters</span></span>
<span data-ttu-id="47292-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47292-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47292-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47292-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47292-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47292-124">INPUTS</span></span>

### <span data-ttu-id="47292-125">System. String</span><span class="sxs-lookup"><span data-stu-id="47292-125">System.String</span></span>

## <span data-ttu-id="47292-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47292-126">OUTPUTS</span></span>

### <span data-ttu-id="47292-127">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="47292-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="47292-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47292-128">NOTES</span></span>
* <span data-ttu-id="47292-129">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="47292-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="47292-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47292-130">RELATED LINKS</span></span>

[<span data-ttu-id="47292-131">Dodaj-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="47292-131">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="47292-132">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="47292-132">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="47292-133">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="47292-133">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="47292-134">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="47292-134">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)



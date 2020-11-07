---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 3847c1026f8cea6f3c33db45215a7a3253e4c680
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898322"
---
# <span data-ttu-id="33a03-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="33a03-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="33a03-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33a03-102">SYNOPSIS</span></span>
<span data-ttu-id="33a03-103">Tworzy certyfikat uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="33a03-103">Creates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33a03-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33a03-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33a03-105">Opis</span><span class="sxs-lookup"><span data-stu-id="33a03-105">DESCRIPTION</span></span>
<span data-ttu-id="33a03-106">Polecenie cmdlet **New-AzureRmApplicationGatewayAuthenticationCertificate** tworzy certyfikat uwierzytelniania dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="33a03-106">The **New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="33a03-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33a03-107">EXAMPLES</span></span>

### <span data-ttu-id="33a03-108">1:1</span><span class="sxs-lookup"><span data-stu-id="33a03-108">1:</span></span>
```

```

## <span data-ttu-id="33a03-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33a03-109">PARAMETERS</span></span>

### <span data-ttu-id="33a03-110">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="33a03-110">-CertificateFile</span></span>
<span data-ttu-id="33a03-111">Określa ścieżkę certyfikatu uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="33a03-111">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="33a03-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33a03-112">-DefaultProfile</span></span>
<span data-ttu-id="33a03-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="33a03-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33a03-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="33a03-114">-Name</span></span>
<span data-ttu-id="33a03-115">Określa nazwę certyfikatu uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="33a03-115">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="33a03-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="33a03-116">-Confirm</span></span>
<span data-ttu-id="33a03-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33a03-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33a03-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33a03-118">-WhatIf</span></span>
<span data-ttu-id="33a03-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33a03-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33a03-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="33a03-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33a03-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33a03-121">CommonParameters</span></span>
<span data-ttu-id="33a03-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33a03-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33a03-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33a03-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33a03-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33a03-124">INPUTS</span></span>

### <span data-ttu-id="33a03-125">System. String</span><span class="sxs-lookup"><span data-stu-id="33a03-125">System.String</span></span>

## <span data-ttu-id="33a03-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33a03-126">OUTPUTS</span></span>

### <span data-ttu-id="33a03-127">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="33a03-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="33a03-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33a03-128">NOTES</span></span>
* <span data-ttu-id="33a03-129">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="33a03-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="33a03-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33a03-130">RELATED LINKS</span></span>

[<span data-ttu-id="33a03-131">Dodaj-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="33a03-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="33a03-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="33a03-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="33a03-133">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="33a03-133">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="33a03-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="33a03-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)



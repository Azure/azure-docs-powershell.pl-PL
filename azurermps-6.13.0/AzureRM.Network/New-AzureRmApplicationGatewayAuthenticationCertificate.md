---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bdc2821c8499c5a95acd180c9bbfa28568cc5034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543700"
---
# <span data-ttu-id="0e2cc-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0e2cc-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="0e2cc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e2cc-102">SYNOPSIS</span></span>
<span data-ttu-id="0e2cc-103">Tworzy certyfikat uwierzytelniania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0e2cc-103">Creates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e2cc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e2cc-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e2cc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0e2cc-105">DESCRIPTION</span></span>
<span data-ttu-id="0e2cc-106">Polecenie cmdlet **New-AzureRmApplicationGatewayAuthenticationCertificate** tworzy certyfikat uwierzytelniania dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0e2cc-106">The **New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="0e2cc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e2cc-107">EXAMPLES</span></span>

## <span data-ttu-id="0e2cc-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e2cc-108">PARAMETERS</span></span>

### <span data-ttu-id="0e2cc-109">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="0e2cc-109">-CertificateFile</span></span>
<span data-ttu-id="0e2cc-110">Określa ścieżkę certyfikatu uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="0e2cc-110">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="0e2cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e2cc-111">-DefaultProfile</span></span>
<span data-ttu-id="0e2cc-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e2cc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e2cc-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0e2cc-113">-Name</span></span>
<span data-ttu-id="0e2cc-114">Określa nazwę certyfikatu uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="0e2cc-114">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="0e2cc-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0e2cc-115">-Confirm</span></span>
<span data-ttu-id="0e2cc-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e2cc-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e2cc-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e2cc-117">-WhatIf</span></span>
<span data-ttu-id="0e2cc-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e2cc-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e2cc-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0e2cc-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e2cc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e2cc-120">CommonParameters</span></span>
<span data-ttu-id="0e2cc-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e2cc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e2cc-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e2cc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e2cc-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e2cc-123">INPUTS</span></span>

### <span data-ttu-id="0e2cc-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0e2cc-124">None</span></span>

## <span data-ttu-id="0e2cc-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e2cc-125">OUTPUTS</span></span>

### <span data-ttu-id="0e2cc-126">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0e2cc-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="0e2cc-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e2cc-127">NOTES</span></span>
* <span data-ttu-id="0e2cc-128">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="0e2cc-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="0e2cc-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e2cc-129">RELATED LINKS</span></span>

[<span data-ttu-id="0e2cc-130">Dodaj-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0e2cc-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="0e2cc-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0e2cc-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="0e2cc-132">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0e2cc-132">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="0e2cc-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="0e2cc-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)



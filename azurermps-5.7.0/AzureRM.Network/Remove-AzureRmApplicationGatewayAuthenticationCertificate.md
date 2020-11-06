---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 013010e0b679c69a6fa5c6d8341879b95bd55692
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552868"
---
# <span data-ttu-id="f410e-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f410e-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="f410e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f410e-102">SYNOPSIS</span></span>
<span data-ttu-id="f410e-103">Usuwa certyfikat uwierzytelniania z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f410e-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f410e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f410e-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f410e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f410e-105">DESCRIPTION</span></span>
<span data-ttu-id="f410e-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayAuthenticationCertificate** usuwa certyfikat uwierzytelniania z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f410e-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="f410e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f410e-107">EXAMPLES</span></span>

## <span data-ttu-id="f410e-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f410e-108">PARAMETERS</span></span>

### <span data-ttu-id="f410e-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f410e-109">-ApplicationGateway</span></span>
<span data-ttu-id="f410e-110">Określa nazwę bramy aplikacji, z której to polecenie cmdlet usuwa certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="f410e-110">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="f410e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f410e-111">-DefaultProfile</span></span>
<span data-ttu-id="f410e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f410e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f410e-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f410e-113">-Name</span></span>
<span data-ttu-id="f410e-114">Określa nazwę certyfikatu uwierzytelniania, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f410e-114">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f410e-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f410e-115">-Confirm</span></span>
<span data-ttu-id="f410e-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f410e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f410e-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f410e-117">-WhatIf</span></span>
<span data-ttu-id="f410e-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f410e-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f410e-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f410e-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f410e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f410e-120">CommonParameters</span></span>
<span data-ttu-id="f410e-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f410e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f410e-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f410e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f410e-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f410e-123">INPUTS</span></span>

### <span data-ttu-id="f410e-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f410e-124">System.String</span></span>

## <span data-ttu-id="f410e-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f410e-125">OUTPUTS</span></span>

### <span data-ttu-id="f410e-126">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f410e-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f410e-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f410e-127">NOTES</span></span>
* <span data-ttu-id="f410e-128">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="f410e-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f410e-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f410e-129">RELATED LINKS</span></span>

[<span data-ttu-id="f410e-130">Dodaj-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f410e-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f410e-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f410e-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f410e-132">Nowe — AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f410e-132">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f410e-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f410e-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)



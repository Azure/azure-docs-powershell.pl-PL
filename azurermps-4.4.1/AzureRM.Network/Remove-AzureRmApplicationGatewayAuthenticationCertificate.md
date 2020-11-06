---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 3facee36f6862c02975566dee20d9e7fb8c8824f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527402"
---
# <span data-ttu-id="04efa-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="04efa-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="04efa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04efa-102">SYNOPSIS</span></span>
<span data-ttu-id="04efa-103">Usuwa certyfikat uwierzytelniania z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="04efa-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04efa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04efa-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="04efa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="04efa-105">DESCRIPTION</span></span>
<span data-ttu-id="04efa-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayAuthenticationCertificate** usuwa certyfikat uwierzytelniania z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="04efa-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="04efa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04efa-107">EXAMPLES</span></span>

## <span data-ttu-id="04efa-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04efa-108">PARAMETERS</span></span>

### <span data-ttu-id="04efa-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="04efa-109">-ApplicationGateway</span></span>
<span data-ttu-id="04efa-110">Określa nazwę bramy aplikacji, z której to polecenie cmdlet usuwa certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="04efa-110">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="04efa-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="04efa-111">-Name</span></span>
<span data-ttu-id="04efa-112">Określa nazwę certyfikatu uwierzytelniania, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04efa-112">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="04efa-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="04efa-113">-Confirm</span></span>
<span data-ttu-id="04efa-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04efa-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04efa-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04efa-115">-WhatIf</span></span>
<span data-ttu-id="04efa-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04efa-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04efa-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="04efa-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04efa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04efa-118">-DefaultProfile</span></span>
<span data-ttu-id="04efa-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="04efa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04efa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04efa-120">CommonParameters</span></span>
<span data-ttu-id="04efa-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04efa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04efa-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04efa-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04efa-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04efa-123">INPUTS</span></span>

### <span data-ttu-id="04efa-124">System. String</span><span class="sxs-lookup"><span data-stu-id="04efa-124">System.String</span></span>

## <span data-ttu-id="04efa-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04efa-125">OUTPUTS</span></span>

### <span data-ttu-id="04efa-126">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="04efa-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="04efa-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04efa-127">NOTES</span></span>
* <span data-ttu-id="04efa-128">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="04efa-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="04efa-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04efa-129">RELATED LINKS</span></span>

[<span data-ttu-id="04efa-130">Dodaj-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="04efa-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="04efa-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="04efa-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="04efa-132">Nowe — AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="04efa-132">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="04efa-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="04efa-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)



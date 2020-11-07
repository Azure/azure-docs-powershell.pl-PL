---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 00ad021e86617d08f0ca30f660cac28110348885
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897921"
---
# <span data-ttu-id="376d6-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="376d6-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="376d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="376d6-102">SYNOPSIS</span></span>
<span data-ttu-id="376d6-103">Usuwa certyfikat uwierzytelniania z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="376d6-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="376d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="376d6-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="376d6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="376d6-105">DESCRIPTION</span></span>
<span data-ttu-id="376d6-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayAuthenticationCertificate** usuwa certyfikat uwierzytelniania z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="376d6-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="376d6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="376d6-107">EXAMPLES</span></span>

### <span data-ttu-id="376d6-108">1:1</span><span class="sxs-lookup"><span data-stu-id="376d6-108">1:</span></span>
```

```

## <span data-ttu-id="376d6-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="376d6-109">PARAMETERS</span></span>

### <span data-ttu-id="376d6-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="376d6-110">-ApplicationGateway</span></span>
<span data-ttu-id="376d6-111">Określa nazwę bramy aplikacji, z której to polecenie cmdlet usuwa certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="376d6-111">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="376d6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="376d6-112">-DefaultProfile</span></span>
<span data-ttu-id="376d6-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="376d6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="376d6-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="376d6-114">-Name</span></span>
<span data-ttu-id="376d6-115">Określa nazwę certyfikatu uwierzytelniania, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="376d6-115">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="376d6-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="376d6-116">-Confirm</span></span>
<span data-ttu-id="376d6-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="376d6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="376d6-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="376d6-118">-WhatIf</span></span>
<span data-ttu-id="376d6-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="376d6-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="376d6-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="376d6-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="376d6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="376d6-121">CommonParameters</span></span>
<span data-ttu-id="376d6-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="376d6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="376d6-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="376d6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="376d6-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="376d6-124">INPUTS</span></span>

### <span data-ttu-id="376d6-125">System. String</span><span class="sxs-lookup"><span data-stu-id="376d6-125">System.String</span></span>

## <span data-ttu-id="376d6-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="376d6-126">OUTPUTS</span></span>

### <span data-ttu-id="376d6-127">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="376d6-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="376d6-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="376d6-128">NOTES</span></span>
* <span data-ttu-id="376d6-129">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="376d6-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="376d6-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="376d6-130">RELATED LINKS</span></span>

[<span data-ttu-id="376d6-131">Dodaj-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="376d6-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="376d6-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="376d6-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="376d6-133">Nowe — AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="376d6-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="376d6-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="376d6-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)



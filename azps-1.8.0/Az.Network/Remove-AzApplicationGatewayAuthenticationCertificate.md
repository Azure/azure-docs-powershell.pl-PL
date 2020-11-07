---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 4bed76f6fa80e5f901d5deeba45940d16332fa41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709198"
---
# <span data-ttu-id="78ff4-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="78ff4-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="78ff4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78ff4-102">SYNOPSIS</span></span>
<span data-ttu-id="78ff4-103">Usuwa certyfikat uwierzytelniania z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="78ff4-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="78ff4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78ff4-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78ff4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="78ff4-105">DESCRIPTION</span></span>
<span data-ttu-id="78ff4-106">Polecenie cmdlet **Remove-AzApplicationGatewayAuthenticationCertificate** usuwa certyfikat uwierzytelniania z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="78ff4-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="78ff4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78ff4-107">EXAMPLES</span></span>

### <span data-ttu-id="78ff4-108">Przykład 1: Usuwanie certyfikatu uwierzytelniania z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="78ff4-108">Example 1: Remove an authentication certificate from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="78ff4-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie appGwName i zapisuje wynik w zmiennej $appgw.</span><span class="sxs-lookup"><span data-stu-id="78ff4-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="78ff4-110">Drugie polecenie usuwa certyfikat uwierzytelniania o nazwie cert01 z bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="78ff4-110">The second command removes the authentication certificate named cert01 from the application gateway.</span></span>
<span data-ttu-id="78ff4-111">W trzecim poleceniu jest aktualizowana Brama Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="78ff4-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="78ff4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78ff4-112">PARAMETERS</span></span>

### <span data-ttu-id="78ff4-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="78ff4-113">-ApplicationGateway</span></span>
<span data-ttu-id="78ff4-114">Określa nazwę bramy aplikacji, z której to polecenie cmdlet usuwa certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="78ff4-114">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="78ff4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78ff4-115">-DefaultProfile</span></span>
<span data-ttu-id="78ff4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="78ff4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78ff4-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="78ff4-117">-Name</span></span>
<span data-ttu-id="78ff4-118">Określa nazwę certyfikatu uwierzytelniania, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78ff4-118">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="78ff4-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="78ff4-119">-Confirm</span></span>
<span data-ttu-id="78ff4-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78ff4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78ff4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78ff4-121">-WhatIf</span></span>
<span data-ttu-id="78ff4-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78ff4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78ff4-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="78ff4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78ff4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78ff4-124">CommonParameters</span></span>
<span data-ttu-id="78ff4-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78ff4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78ff4-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78ff4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78ff4-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78ff4-127">INPUTS</span></span>

### <span data-ttu-id="78ff4-128">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="78ff4-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="78ff4-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78ff4-129">OUTPUTS</span></span>

### <span data-ttu-id="78ff4-130">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="78ff4-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="78ff4-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78ff4-131">NOTES</span></span>
* <span data-ttu-id="78ff4-132">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="78ff4-132">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="78ff4-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78ff4-133">RELATED LINKS</span></span>

[<span data-ttu-id="78ff4-134">Dodaj-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="78ff4-134">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="78ff4-135">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="78ff4-135">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="78ff4-136">Nowe — AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="78ff4-136">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="78ff4-137">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="78ff4-137">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


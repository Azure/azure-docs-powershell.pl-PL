---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 02416fdb18f01c9a2af6c091b0be109b479ce45d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184346"
---
# <span data-ttu-id="305a0-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="305a0-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="305a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="305a0-102">SYNOPSIS</span></span>
<span data-ttu-id="305a0-103">Usuwa certyfikat uwierzytelniania z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="305a0-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="305a0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="305a0-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="305a0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="305a0-105">DESCRIPTION</span></span>
<span data-ttu-id="305a0-106">Polecenie **cmdlet Remove-AzApplicationGatewayAuthenticationCertificate** usuwa certyfikat uwierzytelniania z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="305a0-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="305a0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="305a0-107">EXAMPLES</span></span>

### <span data-ttu-id="305a0-108">Przykład 1. Usuwanie certyfikatu uwierzytelniania z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="305a0-108">Example 1: Remove an authentication certificate from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="305a0-109">Pierwsze polecenie pobiera nazwę bramy aplikacji appGwName i zapisuje wynik w $appgw zmienną.</span><span class="sxs-lookup"><span data-stu-id="305a0-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="305a0-110">Drugie polecenie usuwa certyfikat uwierzytelniania o nazwie cert01 z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="305a0-110">The second command removes the authentication certificate named cert01 from the application gateway.</span></span>
<span data-ttu-id="305a0-111">Trzecie polecenie aktualizuje bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="305a0-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="305a0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="305a0-112">PARAMETERS</span></span>

### <span data-ttu-id="305a0-113">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="305a0-113">-ApplicationGateway</span></span>
<span data-ttu-id="305a0-114">Określa nazwę bramy aplikacji, z której to polecenie cmdlet usuwa certyfikat uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="305a0-114">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="305a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="305a0-115">-DefaultProfile</span></span>
<span data-ttu-id="305a0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="305a0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="305a0-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="305a0-117">-Name</span></span>
<span data-ttu-id="305a0-118">Określa nazwę certyfikatu uwierzytelniania, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="305a0-118">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="305a0-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="305a0-119">-Confirm</span></span>
<span data-ttu-id="305a0-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="305a0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="305a0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="305a0-121">-WhatIf</span></span>
<span data-ttu-id="305a0-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="305a0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="305a0-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="305a0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="305a0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="305a0-124">CommonParameters</span></span>
<span data-ttu-id="305a0-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="305a0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="305a0-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="305a0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="305a0-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="305a0-127">INPUTS</span></span>

### <span data-ttu-id="305a0-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="305a0-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="305a0-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="305a0-129">OUTPUTS</span></span>

### <span data-ttu-id="305a0-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="305a0-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="305a0-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="305a0-131">NOTES</span></span>
* <span data-ttu-id="305a0-132">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="305a0-132">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="305a0-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="305a0-133">RELATED LINKS</span></span>

[<span data-ttu-id="305a0-134">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="305a0-134">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="305a0-135">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="305a0-135">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="305a0-136">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="305a0-136">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="305a0-137">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="305a0-137">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)



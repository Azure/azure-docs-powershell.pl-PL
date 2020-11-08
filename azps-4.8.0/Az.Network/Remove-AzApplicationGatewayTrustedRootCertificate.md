---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 3e8c4f6bc25ea5ff9b8efcee989937fb688fea57
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223761"
---
# <span data-ttu-id="1b083-101">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1b083-101">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="1b083-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b083-102">SYNOPSIS</span></span>
<span data-ttu-id="1b083-103">Usuwa zaufany certyfikat główny z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1b083-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

## <span data-ttu-id="1b083-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b083-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedRootCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b083-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1b083-105">DESCRIPTION</span></span>
<span data-ttu-id="1b083-106">Polecenie cmdlet **Remove-AzApplicationGatewayTrustedRootCertificate** usuwa zaufany certyfikat główny z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1b083-106">The **Remove-AzApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="1b083-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b083-107">EXAMPLES</span></span>

### <span data-ttu-id="1b083-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1b083-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="1b083-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $gw.</span><span class="sxs-lookup"><span data-stu-id="1b083-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="1b083-110">Drugie polecenie usuwa zaufany certyfikat główny o nazwie myRootCA od bramy aplikacji przechowywanej w $gw.</span><span class="sxs-lookup"><span data-stu-id="1b083-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="1b083-111">W trzecim poleceniu jest aktualizowana Brama Application Gateway na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="1b083-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="1b083-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b083-112">PARAMETERS</span></span>

### <span data-ttu-id="1b083-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b083-113">-ApplicationGateway</span></span>
<span data-ttu-id="1b083-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b083-114">The applicationGateway</span></span>

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

### <span data-ttu-id="1b083-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b083-115">-DefaultProfile</span></span>
<span data-ttu-id="1b083-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b083-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b083-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1b083-117">-Name</span></span>
<span data-ttu-id="1b083-118">Nazwa certyfikatu TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="1b083-118">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="1b083-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1b083-119">-Confirm</span></span>
<span data-ttu-id="1b083-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b083-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b083-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b083-121">-WhatIf</span></span>
<span data-ttu-id="1b083-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b083-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b083-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1b083-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b083-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b083-124">CommonParameters</span></span>
<span data-ttu-id="1b083-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b083-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b083-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b083-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b083-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b083-127">INPUTS</span></span>

### <span data-ttu-id="1b083-128">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b083-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1b083-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b083-129">OUTPUTS</span></span>

### <span data-ttu-id="1b083-130">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b083-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1b083-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b083-131">NOTES</span></span>

## <span data-ttu-id="1b083-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b083-132">RELATED LINKS</span></span>

[<span data-ttu-id="1b083-133">Dodaj-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1b083-133">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="1b083-134">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1b083-134">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="1b083-135">Nowe — AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1b083-135">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="1b083-136">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1b083-136">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)

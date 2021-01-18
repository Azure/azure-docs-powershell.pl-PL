---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 40f31fc2c8cc4d0cb3a9637b39d8c3fcbd18ee42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503216"
---
# <span data-ttu-id="65036-101">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="65036-101">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="65036-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65036-102">SYNOPSIS</span></span>
<span data-ttu-id="65036-103">Usuwa obiekt łańcuch certyfikatu zaufanego urzędu certyfikacji klienta z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="65036-103">Removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="65036-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65036-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedClientCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65036-105">Opis</span><span class="sxs-lookup"><span data-stu-id="65036-105">DESCRIPTION</span></span>
<span data-ttu-id="65036-106">Polecenie cmdlet **Remove-AzApplicationGatewayTrustedClientCertificate** usuwa obiekt łańcuch certyfikatu zaufanego urzędu certyfikacji klienta z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="65036-106">The **Remove-AzApplicationGatewayTrustedClientCertificate** cmdlet removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="65036-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65036-107">EXAMPLES</span></span>

### <span data-ttu-id="65036-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="65036-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name "TrustedClientCertificate01"
```

<span data-ttu-id="65036-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $gw.</span><span class="sxs-lookup"><span data-stu-id="65036-109">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="65036-110">Drugie polecenie usuwa łańcuch certyfikatów zaufanego urzędu certyfikacji klienta o nazwie "TrustedClientCertificate01" z bramy Application Gateway przechowywanej w $gw.</span><span class="sxs-lookup"><span data-stu-id="65036-110">The second command removes the trusted client CA certificate chain named "TrustedClientCertificate01" from the application gateway stored in $gw.</span></span>

## <span data-ttu-id="65036-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65036-111">PARAMETERS</span></span>

### <span data-ttu-id="65036-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65036-112">-ApplicationGateway</span></span>
<span data-ttu-id="65036-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65036-113">The applicationGateway</span></span>

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

### <span data-ttu-id="65036-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65036-114">-DefaultProfile</span></span>
<span data-ttu-id="65036-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="65036-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65036-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="65036-116">-Name</span></span>
<span data-ttu-id="65036-117">Nazwa łańcucha certyfikatów zaufanego urzędu certyfikacji klienta</span><span class="sxs-lookup"><span data-stu-id="65036-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="65036-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65036-118">-Confirm</span></span>
<span data-ttu-id="65036-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65036-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65036-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65036-120">-WhatIf</span></span>
<span data-ttu-id="65036-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65036-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65036-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="65036-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65036-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65036-123">CommonParameters</span></span>
<span data-ttu-id="65036-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65036-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65036-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65036-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65036-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65036-126">INPUTS</span></span>

### <span data-ttu-id="65036-127">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65036-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="65036-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65036-128">OUTPUTS</span></span>

### <span data-ttu-id="65036-129">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65036-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="65036-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65036-130">NOTES</span></span>

## <span data-ttu-id="65036-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65036-131">RELATED LINKS</span></span>

[<span data-ttu-id="65036-132">Nowe — AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="65036-132">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="65036-133">Dodaj-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="65036-133">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="65036-134">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="65036-134">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="65036-135">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="65036-135">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)
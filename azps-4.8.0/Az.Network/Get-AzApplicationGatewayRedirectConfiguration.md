---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 8a49bdeed095ee277d632559402c55ca3baf784c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221473"
---
# <span data-ttu-id="8f3d2-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f3d2-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="8f3d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8f3d2-102">SYNOPSIS</span></span>
<span data-ttu-id="8f3d2-103">Pobiera istniejącą konfigurację przekierowania od bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8f3d2-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="8f3d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8f3d2-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f3d2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8f3d2-105">DESCRIPTION</span></span>
<span data-ttu-id="8f3d2-106">Polecenie cmdlet **Get-AzApplicationGatewayRedirectConfiguration** pobiera istniejącą konfigurację przekierowania od bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8f3d2-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="8f3d2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8f3d2-107">EXAMPLES</span></span>

### <span data-ttu-id="8f3d2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8f3d2-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="8f3d2-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="8f3d2-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="8f3d2-110">Drugie polecenie pobiera konfigurację przekierowania o nazwie Redirect01 od bramy aplikacji przechowywanej w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="8f3d2-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="8f3d2-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8f3d2-111">PARAMETERS</span></span>

### <span data-ttu-id="8f3d2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8f3d2-112">-ApplicationGateway</span></span>
<span data-ttu-id="8f3d2-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8f3d2-113">The applicationGateway</span></span>

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

### <span data-ttu-id="8f3d2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f3d2-114">-DefaultProfile</span></span>
<span data-ttu-id="8f3d2-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f3d2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f3d2-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8f3d2-116">-Name</span></span>
<span data-ttu-id="8f3d2-117">Nazwa reguły rozsyłania żądań</span><span class="sxs-lookup"><span data-stu-id="8f3d2-117">The name of the request routing rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3d2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f3d2-118">CommonParameters</span></span>
<span data-ttu-id="8f3d2-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f3d2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f3d2-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f3d2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f3d2-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f3d2-121">INPUTS</span></span>

### <span data-ttu-id="8f3d2-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8f3d2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8f3d2-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8f3d2-123">OUTPUTS</span></span>

### <span data-ttu-id="8f3d2-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f3d2-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="8f3d2-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8f3d2-125">NOTES</span></span>

## <span data-ttu-id="8f3d2-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f3d2-126">RELATED LINKS</span></span>

[<span data-ttu-id="8f3d2-127">Dodaj-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f3d2-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="8f3d2-128">Nowe — AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f3d2-128">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="8f3d2-129">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f3d2-129">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="8f3d2-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f3d2-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)

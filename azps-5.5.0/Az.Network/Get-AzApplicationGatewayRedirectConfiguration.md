---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 8a49bdeed095ee277d632559402c55ca3baf784c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192011"
---
# <span data-ttu-id="daa11-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="daa11-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="daa11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daa11-102">SYNOPSIS</span></span>
<span data-ttu-id="daa11-103">Pobiera istniejącą konfigurację przekierowywania z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="daa11-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="daa11-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="daa11-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daa11-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="daa11-105">DESCRIPTION</span></span>
<span data-ttu-id="daa11-106">Polecenie **cmdlet Get-AzApplicationGatewayRedirectConfiguration** pobiera istniejącą konfigurację przekierowywania z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="daa11-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="daa11-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="daa11-107">EXAMPLES</span></span>

### <span data-ttu-id="daa11-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="daa11-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="daa11-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 i przechowuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="daa11-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="daa11-110">Drugie polecenie pobiera konfigurację przekierowywania o nazwie Redirect01 z bramy aplikacji przechowywaną w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="daa11-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="daa11-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="daa11-111">PARAMETERS</span></span>

### <span data-ttu-id="daa11-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daa11-112">-ApplicationGateway</span></span>
<span data-ttu-id="daa11-113">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="daa11-113">The applicationGateway</span></span>

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

### <span data-ttu-id="daa11-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daa11-114">-DefaultProfile</span></span>
<span data-ttu-id="daa11-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="daa11-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="daa11-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="daa11-116">-Name</span></span>
<span data-ttu-id="daa11-117">Nazwa reguły routingu żądania</span><span class="sxs-lookup"><span data-stu-id="daa11-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="daa11-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa11-118">CommonParameters</span></span>
<span data-ttu-id="daa11-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daa11-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa11-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="daa11-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa11-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="daa11-121">INPUTS</span></span>

### <span data-ttu-id="daa11-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daa11-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="daa11-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="daa11-123">OUTPUTS</span></span>

### <span data-ttu-id="daa11-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="daa11-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="daa11-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="daa11-125">NOTES</span></span>

## <span data-ttu-id="daa11-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="daa11-126">RELATED LINKS</span></span>

[<span data-ttu-id="daa11-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="daa11-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="daa11-128">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="daa11-128">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="daa11-129">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="daa11-129">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="daa11-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="daa11-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)

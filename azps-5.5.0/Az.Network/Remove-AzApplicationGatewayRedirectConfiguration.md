---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: fdd461ea2908e59ba824b09a49bed3b6b8f4d38f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179546"
---
# <span data-ttu-id="557fe-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="557fe-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="557fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="557fe-102">SYNOPSIS</span></span>
<span data-ttu-id="557fe-103">Usuwa konfigurację przekierowywania z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="557fe-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="557fe-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="557fe-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="557fe-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="557fe-105">DESCRIPTION</span></span>
<span data-ttu-id="557fe-106">Polecenie **cmdlet Remove-AzApplicationGatewayRedirectConfiguration** usuwa konfigurację przekierowywania z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="557fe-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="557fe-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="557fe-107">EXAMPLES</span></span>

### <span data-ttu-id="557fe-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="557fe-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="557fe-109">Pierwsze polecenie pobiera bramę aplikacji i przechowuje je w $AppGw aplikacji.</span><span class="sxs-lookup"><span data-stu-id="557fe-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="557fe-110">Drugie polecenie usuwa konfigurację przekierowywania o nazwie Redirect01 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="557fe-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="557fe-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="557fe-111">PARAMETERS</span></span>

### <span data-ttu-id="557fe-112">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="557fe-112">-ApplicationGateway</span></span>
<span data-ttu-id="557fe-113">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="557fe-113">The applicationGateway</span></span>

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

### <span data-ttu-id="557fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="557fe-114">-DefaultProfile</span></span>
<span data-ttu-id="557fe-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="557fe-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="557fe-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="557fe-116">-Name</span></span>
<span data-ttu-id="557fe-117">Nazwa konfiguracji przekierowywania</span><span class="sxs-lookup"><span data-stu-id="557fe-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="557fe-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="557fe-118">CommonParameters</span></span>
<span data-ttu-id="557fe-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="557fe-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="557fe-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="557fe-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="557fe-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="557fe-121">INPUTS</span></span>

### <span data-ttu-id="557fe-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="557fe-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="557fe-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="557fe-123">OUTPUTS</span></span>

### <span data-ttu-id="557fe-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="557fe-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="557fe-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="557fe-125">NOTES</span></span>

## <span data-ttu-id="557fe-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="557fe-126">RELATED LINKS</span></span>

[<span data-ttu-id="557fe-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="557fe-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="557fe-128">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="557fe-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="557fe-129">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="557fe-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="557fe-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="557fe-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 367e54036d7665cf59ebcc6f1a10b3060b97580d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991019"
---
# <span data-ttu-id="2ab3b-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ab3b-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="2ab3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ab3b-102">SYNOPSIS</span></span>
<span data-ttu-id="2ab3b-103">Usuwa konfigurację privateLink z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2ab3b-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="2ab3b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2ab3b-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ab3b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2ab3b-105">DESCRIPTION</span></span>
<span data-ttu-id="2ab3b-106">Polecenie **cmdlet Remove-AzApplicationGatewayPrivateLinkConfiguration** usuwa konfigurację privateLink z bramy aplikacji Azure.</span><span class="sxs-lookup"><span data-stu-id="2ab3b-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="2ab3b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2ab3b-107">EXAMPLES</span></span>

### <span data-ttu-id="2ab3b-108">Przykład 1. Usuwanie konfiguracji privatelinku bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="2ab3b-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="2ab3b-109">Pierwsze polecenie otrzymuje bramę aplikacji i zapisuje je w $AppGw aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2ab3b-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2ab3b-110">Drugie polecenie usuwa konfigurację privateLink o nazwie privateLinkConfig01 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2ab3b-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="2ab3b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ab3b-111">PARAMETERS</span></span>

### <span data-ttu-id="2ab3b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2ab3b-112">-ApplicationGateway</span></span>
<span data-ttu-id="2ab3b-113">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="2ab3b-113">The applicationGateway</span></span>

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

### <span data-ttu-id="2ab3b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ab3b-114">-DefaultProfile</span></span>
<span data-ttu-id="2ab3b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ab3b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ab3b-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2ab3b-116">-Name</span></span>
<span data-ttu-id="2ab3b-117">Nazwa konfiguracji privateLink bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="2ab3b-117">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="2ab3b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ab3b-118">CommonParameters</span></span>
<span data-ttu-id="2ab3b-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ab3b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ab3b-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ab3b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ab3b-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ab3b-121">INPUTS</span></span>

### <span data-ttu-id="2ab3b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2ab3b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2ab3b-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ab3b-123">OUTPUTS</span></span>

### <span data-ttu-id="2ab3b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2ab3b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2ab3b-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2ab3b-125">NOTES</span></span>

## <span data-ttu-id="2ab3b-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ab3b-126">RELATED LINKS</span></span>

[<span data-ttu-id="2ab3b-127">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ab3b-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="2ab3b-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ab3b-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="2ab3b-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ab3b-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="2ab3b-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ab3b-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
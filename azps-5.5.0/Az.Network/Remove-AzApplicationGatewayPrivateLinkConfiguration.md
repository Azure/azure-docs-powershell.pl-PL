---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 8d222f4eaaa9d37a4f87f5f19604bdef9cff9e39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193515"
---
# <span data-ttu-id="019ba-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="019ba-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="019ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="019ba-102">SYNOPSIS</span></span>
<span data-ttu-id="019ba-103">Usuwa konfigurację privateLink z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="019ba-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="019ba-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="019ba-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="019ba-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="019ba-105">DESCRIPTION</span></span>
<span data-ttu-id="019ba-106">Polecenie **cmdlet Remove-AzApplicationGatewayPrivateLinkConfiguration** usuwa konfigurację privateLink z bramy aplikacji Azure.</span><span class="sxs-lookup"><span data-stu-id="019ba-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="019ba-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="019ba-107">EXAMPLES</span></span>

### <span data-ttu-id="019ba-108">Przykład 1. Usuwanie konfiguracji privatelinku bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="019ba-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="019ba-109">Pierwsze polecenie otrzymuje bramę aplikacji i zapisuje je w $AppGw aplikacji.</span><span class="sxs-lookup"><span data-stu-id="019ba-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="019ba-110">Drugie polecenie usuwa konfigurację privateLink o nazwie privateLinkConfig01 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="019ba-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="019ba-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="019ba-111">PARAMETERS</span></span>

### <span data-ttu-id="019ba-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="019ba-112">-ApplicationGateway</span></span>
<span data-ttu-id="019ba-113">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="019ba-113">The applicationGateway</span></span>

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

### <span data-ttu-id="019ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="019ba-114">-DefaultProfile</span></span>
<span data-ttu-id="019ba-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="019ba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="019ba-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="019ba-116">-Name</span></span>
<span data-ttu-id="019ba-117">Nazwa konfiguracji privateLink bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="019ba-117">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="019ba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="019ba-118">CommonParameters</span></span>
<span data-ttu-id="019ba-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="019ba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="019ba-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="019ba-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="019ba-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="019ba-121">INPUTS</span></span>

### <span data-ttu-id="019ba-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="019ba-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="019ba-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="019ba-123">OUTPUTS</span></span>

### <span data-ttu-id="019ba-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="019ba-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="019ba-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="019ba-125">NOTES</span></span>

## <span data-ttu-id="019ba-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="019ba-126">RELATED LINKS</span></span>

[<span data-ttu-id="019ba-127">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="019ba-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="019ba-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="019ba-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="019ba-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="019ba-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="019ba-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="019ba-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
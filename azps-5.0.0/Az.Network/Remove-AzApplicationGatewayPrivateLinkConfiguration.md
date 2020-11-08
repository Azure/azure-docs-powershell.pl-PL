---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 8d222f4eaaa9d37a4f87f5f19604bdef9cff9e39
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233293"
---
# <span data-ttu-id="79ff2-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="79ff2-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="79ff2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79ff2-102">SYNOPSIS</span></span>
<span data-ttu-id="79ff2-103">Usuwa konfigurację privateLink z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79ff2-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="79ff2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79ff2-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79ff2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="79ff2-105">DESCRIPTION</span></span>
<span data-ttu-id="79ff2-106">Polecenie cmdlet **Remove-AzApplicationGatewayPrivateLinkConfiguration** usuwa konfigurację privateLink z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="79ff2-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="79ff2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79ff2-107">EXAMPLES</span></span>

### <span data-ttu-id="79ff2-108">Przykład 1: Usuwanie konfiguracji PrivateLink bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="79ff2-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="79ff2-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="79ff2-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="79ff2-110">Drugie polecenie usuwa konfigurację privateLink o nazwie privateLinkConfig01 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="79ff2-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="79ff2-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79ff2-111">PARAMETERS</span></span>

### <span data-ttu-id="79ff2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79ff2-112">-ApplicationGateway</span></span>
<span data-ttu-id="79ff2-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79ff2-113">The applicationGateway</span></span>

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

### <span data-ttu-id="79ff2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79ff2-114">-DefaultProfile</span></span>
<span data-ttu-id="79ff2-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79ff2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79ff2-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="79ff2-116">-Name</span></span>
<span data-ttu-id="79ff2-117">Nazwa konfiguracji usługi Application Gateway privateLink</span><span class="sxs-lookup"><span data-stu-id="79ff2-117">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="79ff2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79ff2-118">CommonParameters</span></span>
<span data-ttu-id="79ff2-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79ff2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79ff2-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79ff2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79ff2-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79ff2-121">INPUTS</span></span>

### <span data-ttu-id="79ff2-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79ff2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="79ff2-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79ff2-123">OUTPUTS</span></span>

### <span data-ttu-id="79ff2-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79ff2-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="79ff2-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79ff2-125">NOTES</span></span>

## <span data-ttu-id="79ff2-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79ff2-126">RELATED LINKS</span></span>

[<span data-ttu-id="79ff2-127">Nowe — AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="79ff2-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="79ff2-128">Dodaj-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="79ff2-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="79ff2-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="79ff2-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="79ff2-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="79ff2-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
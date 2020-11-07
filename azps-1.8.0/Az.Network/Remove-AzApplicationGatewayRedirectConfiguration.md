---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: d75cbcbf89fde83419b9a1f97c0f66805258c82d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709171"
---
# <span data-ttu-id="027a9-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="027a9-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="027a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="027a9-102">SYNOPSIS</span></span>
<span data-ttu-id="027a9-103">Usuwa konfigurację przekierowania z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="027a9-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="027a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="027a9-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="027a9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="027a9-105">DESCRIPTION</span></span>
<span data-ttu-id="027a9-106">Polecenie cmdlet **Remove-AzApplicationGatewayRedirectConfiguration** usuwa konfigurację przekierowania z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="027a9-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="027a9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="027a9-107">EXAMPLES</span></span>

### <span data-ttu-id="027a9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="027a9-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="027a9-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="027a9-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="027a9-110">Drugie polecenie usuwa konfigurację przekierowania o nazwie Redirect01 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="027a9-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="027a9-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="027a9-111">PARAMETERS</span></span>

### <span data-ttu-id="027a9-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="027a9-112">-ApplicationGateway</span></span>
<span data-ttu-id="027a9-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="027a9-113">The applicationGateway</span></span>

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

### <span data-ttu-id="027a9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="027a9-114">-DefaultProfile</span></span>
<span data-ttu-id="027a9-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="027a9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="027a9-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="027a9-116">-Name</span></span>
<span data-ttu-id="027a9-117">Nazwa konfiguracji przekierowania</span><span class="sxs-lookup"><span data-stu-id="027a9-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="027a9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="027a9-118">CommonParameters</span></span>
<span data-ttu-id="027a9-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="027a9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="027a9-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="027a9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="027a9-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="027a9-121">INPUTS</span></span>

### <span data-ttu-id="027a9-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="027a9-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="027a9-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="027a9-123">OUTPUTS</span></span>

### <span data-ttu-id="027a9-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="027a9-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="027a9-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="027a9-125">NOTES</span></span>

## <span data-ttu-id="027a9-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="027a9-126">RELATED LINKS</span></span>

[<span data-ttu-id="027a9-127">Dodaj-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="027a9-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="027a9-128">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="027a9-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="027a9-129">Nowe — AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="027a9-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="027a9-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="027a9-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)

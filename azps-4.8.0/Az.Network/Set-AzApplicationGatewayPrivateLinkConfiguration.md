---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 78af871cf476ee80c57e22e2469b48bb4d4337a1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063325"
---
# <span data-ttu-id="68e9e-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="68e9e-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="68e9e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68e9e-102">SYNOPSIS</span></span>
<span data-ttu-id="68e9e-103">Modyfikuje konfigurację PrivateLink dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="68e9e-103">Modifies an PrivateLink Configuration for an application gateway.</span></span>

## <span data-ttu-id="68e9e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68e9e-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68e9e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="68e9e-105">DESCRIPTION</span></span>
<span data-ttu-id="68e9e-106">Polecenie cmdlet **Set-AzApplicationGatewayPrivateLinkConfiguration** modyfikuje konfigurację privateLink dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="68e9e-106">The **Set-AzApplicationGatewayPrivateLinkConfiguration** cmdlet modifies an privateLink configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="68e9e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68e9e-107">EXAMPLES</span></span>

### <span data-ttu-id="68e9e-108">Przykład 1: Ustawianie konfiguracji PrivateLink</span><span class="sxs-lookup"><span data-stu-id="68e9e-108">Example 1: Set a PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration01
```

<span data-ttu-id="68e9e-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="68e9e-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="68e9e-110">Drugie polecenie ustawia konfigurację privateLink o nazwie privateLinkConfig01 w celu używania konfiguracji adresu IP przechowywanej w $privateLinkIpConfiguration 01</span><span class="sxs-lookup"><span data-stu-id="68e9e-110">The second command sets the privateLink configuration with name privateLinkConfig01 to use the ip configuration stored in $privateLinkIpConfiguration01</span></span>

## <span data-ttu-id="68e9e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68e9e-111">PARAMETERS</span></span>

### <span data-ttu-id="68e9e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68e9e-112">-ApplicationGateway</span></span>
<span data-ttu-id="68e9e-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68e9e-113">The applicationGateway</span></span>

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

### <span data-ttu-id="68e9e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68e9e-114">-DefaultProfile</span></span>
<span data-ttu-id="68e9e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="68e9e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68e9e-116">-Element IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="68e9e-116">-IpConfiguration</span></span>
<span data-ttu-id="68e9e-117">Lista elementu ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="68e9e-117">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68e9e-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="68e9e-118">-Name</span></span>
<span data-ttu-id="68e9e-119">Nazwa konfiguracji privateLink</span><span class="sxs-lookup"><span data-stu-id="68e9e-119">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="68e9e-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="68e9e-120">-Confirm</span></span>
<span data-ttu-id="68e9e-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68e9e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68e9e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68e9e-122">-WhatIf</span></span>
<span data-ttu-id="68e9e-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68e9e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68e9e-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="68e9e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68e9e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68e9e-125">CommonParameters</span></span>
<span data-ttu-id="68e9e-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68e9e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68e9e-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68e9e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68e9e-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68e9e-128">INPUTS</span></span>

### <span data-ttu-id="68e9e-129">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68e9e-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="68e9e-130">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="68e9e-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="68e9e-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68e9e-131">OUTPUTS</span></span>

### <span data-ttu-id="68e9e-132">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68e9e-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="68e9e-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68e9e-133">NOTES</span></span>

## <span data-ttu-id="68e9e-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68e9e-134">RELATED LINKS</span></span>

[<span data-ttu-id="68e9e-135">Nowe — AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="68e9e-135">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="68e9e-136">Dodaj-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="68e9e-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="68e9e-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="68e9e-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="68e9e-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="68e9e-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)
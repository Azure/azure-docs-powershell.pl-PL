---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2083dd00c5163a67492ff9973fdf7399d67d7cb6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062186"
---
# <span data-ttu-id="3b447-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b447-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="3b447-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b447-102">SYNOPSIS</span></span>
<span data-ttu-id="3b447-103">Dodaje konfigurację linku prywatnego do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3b447-103">Adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="3b447-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b447-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3b447-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3b447-105">DESCRIPTION</span></span>
<span data-ttu-id="3b447-106">Polecenie cmdlet **Add-AzApplicationGatewayPrivateLinkConfiguration** umożliwia dodanie prywatnej konfiguracji linku do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3b447-106">The **Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="3b447-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b447-107">EXAMPLES</span></span>

### <span data-ttu-id="3b447-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3b447-108">Example 1</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $PrivateLinkIpConfiguration
```

<span data-ttu-id="3b447-109">Pierwsze polecenie tworzy privateLinkIpConfiguration i zapisuje je w zmiennej $PrivateLinkIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3b447-109">The first command creates a privateLinkIpConfiguration and stores it in the $PrivateLinkIpConfiguration variable.</span></span>
<span data-ttu-id="3b447-110">Drugie polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3b447-110">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3b447-111">Trzecie polecenie dodaje konfigurację linku prywatnego o nazwie privateLinkConfig01 dla bramy w $AppGw</span><span class="sxs-lookup"><span data-stu-id="3b447-111">The third command adds the private link configuration named privateLinkConfig01, for the gateway in $AppGw</span></span>

## <span data-ttu-id="3b447-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b447-112">PARAMETERS</span></span>

### <span data-ttu-id="3b447-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3b447-113">-ApplicationGateway</span></span>
<span data-ttu-id="3b447-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3b447-114">The applicationGateway</span></span>

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

### <span data-ttu-id="3b447-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b447-115">-DefaultProfile</span></span>
<span data-ttu-id="3b447-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b447-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b447-117">-Element IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b447-117">-IpConfiguration</span></span>
<span data-ttu-id="3b447-118">Lista elementu ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b447-118">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="3b447-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3b447-119">-Name</span></span>
<span data-ttu-id="3b447-120">Nazwa konfiguracji privateLink</span><span class="sxs-lookup"><span data-stu-id="3b447-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="3b447-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b447-121">CommonParameters</span></span>
<span data-ttu-id="3b447-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b447-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b447-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b447-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b447-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b447-124">INPUTS</span></span>

### <span data-ttu-id="3b447-125">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3b447-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="3b447-126">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="3b447-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="3b447-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b447-127">OUTPUTS</span></span>

### <span data-ttu-id="3b447-128">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3b447-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3b447-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b447-129">NOTES</span></span>

## <span data-ttu-id="3b447-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b447-130">RELATED LINKS</span></span>

[<span data-ttu-id="3b447-131">Nowe — AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b447-131">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="3b447-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b447-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="3b447-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b447-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="3b447-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b447-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
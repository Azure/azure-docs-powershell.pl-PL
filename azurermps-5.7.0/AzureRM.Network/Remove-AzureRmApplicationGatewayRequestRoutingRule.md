---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 635e1377c5120fcfb1c623634bf857e3f33bd162
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548883"
---
# <span data-ttu-id="ea806-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ea806-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="ea806-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea806-102">SYNOPSIS</span></span>
<span data-ttu-id="ea806-103">Usuwa regułę rozsyłania żądań z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ea806-103">Removes a request routing rule from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea806-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea806-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea806-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ea806-105">DESCRIPTION</span></span>
<span data-ttu-id="ea806-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayRequestRoutingRule** usuwa regułę rozsyłania żądań z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ea806-106">The **Remove-AzureRmApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="ea806-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea806-107">EXAMPLES</span></span>

### <span data-ttu-id="ea806-108">Przykład 1: Usuwanie reguły rozsyłania żądań z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="ea806-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="ea806-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ea806-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="ea806-110">Drugie polecenie usuwa regułę rozsyłania żądań o nazwie Rule02 od bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ea806-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="ea806-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea806-111">PARAMETERS</span></span>

### <span data-ttu-id="ea806-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ea806-112">-ApplicationGateway</span></span>
<span data-ttu-id="ea806-113">Określa bramę aplikacji, z której ma zostać usunięta reguła routingu żądań.</span><span class="sxs-lookup"><span data-stu-id="ea806-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="ea806-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea806-114">-DefaultProfile</span></span>
<span data-ttu-id="ea806-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea806-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea806-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ea806-116">-Name</span></span>
<span data-ttu-id="ea806-117">Określa nazwę reguły rozsyłania żądań, dla której zostanie usunięte to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea806-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="ea806-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea806-118">CommonParameters</span></span>
<span data-ttu-id="ea806-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea806-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea806-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea806-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea806-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea806-121">INPUTS</span></span>

### <span data-ttu-id="ea806-122">System. String</span><span class="sxs-lookup"><span data-stu-id="ea806-122">System.String</span></span>

## <span data-ttu-id="ea806-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea806-123">OUTPUTS</span></span>

### <span data-ttu-id="ea806-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ea806-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="ea806-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea806-125">NOTES</span></span>

## <span data-ttu-id="ea806-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea806-126">RELATED LINKS</span></span>

[<span data-ttu-id="ea806-127">Dodaj-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ea806-127">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="ea806-128">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ea806-128">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="ea806-129">Nowe — AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ea806-129">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="ea806-130">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ea806-130">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)



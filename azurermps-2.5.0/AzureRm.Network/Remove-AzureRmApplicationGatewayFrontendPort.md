---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendport
schema: 2.0.0
ms.openlocfilehash: ecee205ee831c5ba7a2fa78c00f005af3303a13a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897914"
---
# <span data-ttu-id="742d6-101">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="742d6-101">Remove-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="742d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="742d6-102">SYNOPSIS</span></span>
<span data-ttu-id="742d6-103">Usuwa port frontonu z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="742d6-103">Removes a front-end port from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="742d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="742d6-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="742d6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="742d6-105">DESCRIPTION</span></span>
<span data-ttu-id="742d6-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayFrontendPort** usuwa port frontonu z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="742d6-106">The **Remove-AzureRmApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="742d6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="742d6-107">EXAMPLES</span></span>

### <span data-ttu-id="742d6-108">Przykład: usuwanie portu frontonu z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="742d6-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="742d6-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje bramę w $AppGw zmiennej.</span><span class="sxs-lookup"><span data-stu-id="742d6-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>

<span data-ttu-id="742d6-110">Drugie polecenie usuwa port o nazwie FrontEndPort02 z bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="742d6-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="742d6-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="742d6-111">PARAMETERS</span></span>

### <span data-ttu-id="742d6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="742d6-112">-ApplicationGateway</span></span>
<span data-ttu-id="742d6-113">Określa bramę aplikacji, z której ma zostać usunięty port frontonu.</span><span class="sxs-lookup"><span data-stu-id="742d6-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="742d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="742d6-114">-DefaultProfile</span></span>
<span data-ttu-id="742d6-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="742d6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="742d6-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="742d6-116">-Name</span></span>
<span data-ttu-id="742d6-117">Określa nazwę portu frontonu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="742d6-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="742d6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="742d6-118">CommonParameters</span></span>
<span data-ttu-id="742d6-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="742d6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="742d6-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="742d6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="742d6-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="742d6-121">INPUTS</span></span>

### <span data-ttu-id="742d6-122">System. String</span><span class="sxs-lookup"><span data-stu-id="742d6-122">System.String</span></span>

## <span data-ttu-id="742d6-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="742d6-123">OUTPUTS</span></span>

### <span data-ttu-id="742d6-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="742d6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="742d6-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="742d6-125">NOTES</span></span>

## <span data-ttu-id="742d6-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="742d6-126">RELATED LINKS</span></span>

[<span data-ttu-id="742d6-127">Dodaj-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="742d6-127">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="742d6-128">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="742d6-128">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="742d6-129">Nowe — AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="742d6-129">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="742d6-130">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="742d6-130">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)



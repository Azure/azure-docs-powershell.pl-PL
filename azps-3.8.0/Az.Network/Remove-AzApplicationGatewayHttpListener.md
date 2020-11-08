---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 81b750188a85add491e519c023c765f302e31dea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049326"
---
# <span data-ttu-id="af937-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="af937-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="af937-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af937-102">SYNOPSIS</span></span>
<span data-ttu-id="af937-103">Usuwa odbiornik HTTP z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="af937-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="af937-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af937-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af937-105">Opis</span><span class="sxs-lookup"><span data-stu-id="af937-105">DESCRIPTION</span></span>
<span data-ttu-id="af937-106">Polecenie cmdlet **Remove-AzApplicationGatewayHttpListener** usuwa odbiornik http z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="af937-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="af937-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af937-107">EXAMPLES</span></span>

### <span data-ttu-id="af937-108">Przykład 1: usuwanie odbiornika HTTP bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="af937-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="af937-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="af937-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="af937-110">Drugie polecenie usuwa odbiornik HTTP o nazwie Listener02 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="af937-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="af937-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af937-111">PARAMETERS</span></span>

### <span data-ttu-id="af937-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="af937-112">-ApplicationGateway</span></span>
<span data-ttu-id="af937-113">Określa bramę aplikacji, z której ma zostać usunięty odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="af937-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="af937-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af937-114">-DefaultProfile</span></span>
<span data-ttu-id="af937-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="af937-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af937-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="af937-116">-Name</span></span>
<span data-ttu-id="af937-117">Określa nazwę odbiornika HTTP, który usuwa ten polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af937-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="af937-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af937-118">CommonParameters</span></span>
<span data-ttu-id="af937-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af937-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af937-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af937-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af937-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af937-121">INPUTS</span></span>

### <span data-ttu-id="af937-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="af937-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="af937-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af937-123">OUTPUTS</span></span>

### <span data-ttu-id="af937-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="af937-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="af937-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af937-125">NOTES</span></span>

## <span data-ttu-id="af937-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af937-126">RELATED LINKS</span></span>

[<span data-ttu-id="af937-127">Dodaj-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="af937-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="af937-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="af937-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="af937-129">Nowe — AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="af937-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="af937-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="af937-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)



---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: a60fa54e5d705a71407f2c56986200c897b838e3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898258"
---
# <span data-ttu-id="83365-101">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="83365-101">Remove-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="83365-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="83365-102">SYNOPSIS</span></span>
<span data-ttu-id="83365-103">Usuwa odbiornik HTTP z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="83365-103">Removes an HTTP listener from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83365-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="83365-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83365-105">Opis</span><span class="sxs-lookup"><span data-stu-id="83365-105">DESCRIPTION</span></span>
<span data-ttu-id="83365-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayHttpListener** usuwa odbiornik http z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="83365-106">The **Remove-AzureRmApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="83365-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="83365-107">EXAMPLES</span></span>

### <span data-ttu-id="83365-108">Przykład 1: usuwanie odbiornika HTTP bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="83365-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="83365-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="83365-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="83365-110">Drugie polecenie usuwa odbiornik HTTP o nazwie Listener02 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="83365-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="83365-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83365-111">PARAMETERS</span></span>

### <span data-ttu-id="83365-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="83365-112">-ApplicationGateway</span></span>
<span data-ttu-id="83365-113">Określa bramę aplikacji, z której ma zostać usunięty odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="83365-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="83365-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83365-114">-DefaultProfile</span></span>
<span data-ttu-id="83365-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="83365-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83365-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="83365-116">-Name</span></span>
<span data-ttu-id="83365-117">Określa nazwę odbiornika HTTP, który usuwa ten polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83365-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="83365-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83365-118">CommonParameters</span></span>
<span data-ttu-id="83365-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83365-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83365-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83365-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83365-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83365-121">INPUTS</span></span>

### <span data-ttu-id="83365-122">System. String</span><span class="sxs-lookup"><span data-stu-id="83365-122">System.String</span></span>

## <span data-ttu-id="83365-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="83365-123">OUTPUTS</span></span>

### <span data-ttu-id="83365-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="83365-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="83365-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="83365-125">NOTES</span></span>

## <span data-ttu-id="83365-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83365-126">RELATED LINKS</span></span>

[<span data-ttu-id="83365-127">Dodaj-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="83365-127">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="83365-128">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="83365-128">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="83365-129">Nowe — AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="83365-129">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="83365-130">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="83365-130">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)



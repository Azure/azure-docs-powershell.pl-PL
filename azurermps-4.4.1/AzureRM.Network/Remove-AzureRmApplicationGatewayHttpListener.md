---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 58c7e2770380d309125b3e242c854fcdb86a8f08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546227"
---
# <span data-ttu-id="09c60-101">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="09c60-101">Remove-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="09c60-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09c60-102">SYNOPSIS</span></span>
<span data-ttu-id="09c60-103">Usuwa odbiornik HTTP z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="09c60-103">Removes an HTTP listener from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09c60-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09c60-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09c60-105">Opis</span><span class="sxs-lookup"><span data-stu-id="09c60-105">DESCRIPTION</span></span>
<span data-ttu-id="09c60-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayHttpListener** usuwa odbiornik http z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="09c60-106">The **Remove-AzureRmApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="09c60-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09c60-107">EXAMPLES</span></span>

### <span data-ttu-id="09c60-108">Przykład 1: usuwanie odbiornika HTTP bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="09c60-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="09c60-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="09c60-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="09c60-110">Drugie polecenie usuwa odbiornik HTTP o nazwie Listener02 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="09c60-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="09c60-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09c60-111">PARAMETERS</span></span>

### <span data-ttu-id="09c60-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="09c60-112">-ApplicationGateway</span></span>
<span data-ttu-id="09c60-113">Określa bramę aplikacji, z której ma zostać usunięty odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="09c60-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="09c60-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="09c60-114">-Name</span></span>
<span data-ttu-id="09c60-115">Określa nazwę odbiornika HTTP, który usuwa ten polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09c60-115">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="09c60-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09c60-116">-DefaultProfile</span></span>
<span data-ttu-id="09c60-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="09c60-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09c60-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09c60-118">CommonParameters</span></span>
<span data-ttu-id="09c60-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09c60-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09c60-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09c60-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09c60-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09c60-121">INPUTS</span></span>

### <span data-ttu-id="09c60-122">System. String</span><span class="sxs-lookup"><span data-stu-id="09c60-122">System.String</span></span>

## <span data-ttu-id="09c60-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09c60-123">OUTPUTS</span></span>

### <span data-ttu-id="09c60-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="09c60-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="09c60-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09c60-125">NOTES</span></span>

## <span data-ttu-id="09c60-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09c60-126">RELATED LINKS</span></span>

[<span data-ttu-id="09c60-127">Dodaj-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="09c60-127">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="09c60-128">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="09c60-128">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="09c60-129">Nowe — AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="09c60-129">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="09c60-130">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="09c60-130">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)



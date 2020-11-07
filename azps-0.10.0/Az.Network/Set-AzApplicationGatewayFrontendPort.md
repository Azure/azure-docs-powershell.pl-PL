---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 20ba9060184ae7678b41792ae2a963138d804ff9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892849"
---
# <span data-ttu-id="10826-101">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="10826-101">Set-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="10826-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10826-102">SYNOPSIS</span></span>
<span data-ttu-id="10826-103">Modyfikuje port frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="10826-103">Modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="10826-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10826-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10826-105">Opis</span><span class="sxs-lookup"><span data-stu-id="10826-105">DESCRIPTION</span></span>
<span data-ttu-id="10826-106">Polecenie cmdlet **Set-AzApplicationGatewayFrontendPort** modyfikuje port frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="10826-106">The **Set-AzApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="10826-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10826-107">EXAMPLES</span></span>

### <span data-ttu-id="10826-108">Przykład 1. Ustaw port frontonu bramy aplikacji na 80</span><span class="sxs-lookup"><span data-stu-id="10826-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="10826-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="10826-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="10826-110">Drugie polecenie modyfikuje bramę w $AppGw, aby używać portu 80 dla portu frontonu o nazwie FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="10826-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="10826-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10826-111">PARAMETERS</span></span>

### <span data-ttu-id="10826-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="10826-112">-ApplicationGateway</span></span>
<span data-ttu-id="10826-113">Określa obiekt bramy aplikacji, za pomocą którego to polecenie cmdlet kojarzy port frontonu.</span><span class="sxs-lookup"><span data-stu-id="10826-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="10826-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10826-114">-DefaultProfile</span></span>
<span data-ttu-id="10826-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="10826-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10826-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="10826-116">-Name</span></span>
<span data-ttu-id="10826-117">Określa nazwę portu frontonu do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="10826-117">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="10826-118">-Port</span><span class="sxs-lookup"><span data-stu-id="10826-118">-Port</span></span>
<span data-ttu-id="10826-119">Określa numer portu, który ma być używany dla portu frontonu.</span><span class="sxs-lookup"><span data-stu-id="10826-119">Specifies the port number to use for the front-end port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10826-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10826-120">CommonParameters</span></span>
<span data-ttu-id="10826-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10826-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10826-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10826-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10826-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10826-123">INPUTS</span></span>

### <span data-ttu-id="10826-124">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="10826-124">PSApplicationGateway</span></span>
<span data-ttu-id="10826-125">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="10826-125">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="10826-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10826-126">OUTPUTS</span></span>

### <span data-ttu-id="10826-127">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="10826-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="10826-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10826-128">NOTES</span></span>

## <span data-ttu-id="10826-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10826-129">RELATED LINKS</span></span>

[<span data-ttu-id="10826-130">Dodaj-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="10826-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="10826-131">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="10826-131">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="10826-132">Nowe — AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="10826-132">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="10826-133">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="10826-133">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

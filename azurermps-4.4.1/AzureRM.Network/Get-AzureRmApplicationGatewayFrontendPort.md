---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: f0a897dfcc68d2313326d974d1b5a172bd79db6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527457"
---
# <span data-ttu-id="01bb6-101">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="01bb6-101">Get-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="01bb6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01bb6-102">SYNOPSIS</span></span>
<span data-ttu-id="01bb6-103">Pobiera port frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="01bb6-103">Gets the front-end port of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01bb6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01bb6-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01bb6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="01bb6-105">DESCRIPTION</span></span>
<span data-ttu-id="01bb6-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayFrontendPort** pobiera port frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="01bb6-106">The **Get-AzureRmApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="01bb6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01bb6-107">EXAMPLES</span></span>

### <span data-ttu-id="01bb6-108">Przykład 1: uzyskiwanie określonego portu frontonu</span><span class="sxs-lookup"><span data-stu-id="01bb6-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzureRmApplicationGatewayFrontendIPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="01bb6-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="01bb6-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="01bb6-110">Drugie polecenie pobiera port frontonu o nazwie FrontEndPort01 z $AppGw i zapisuje go w zmiennej $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="01bb6-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="01bb6-111">Przykład 2: uzyskiwanie listy portów frontonu</span><span class="sxs-lookup"><span data-stu-id="01bb6-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzureRmApplicationGatewayFrontendIPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="01bb6-112">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="01bb6-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="01bb6-113">Drugie polecenie pobiera listę portów frontonu z $AppGw i zapisuje je w zmiennej $FrontEndPorts.</span><span class="sxs-lookup"><span data-stu-id="01bb6-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="01bb6-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01bb6-114">PARAMETERS</span></span>

### <span data-ttu-id="01bb6-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01bb6-115">-ApplicationGateway</span></span>
<span data-ttu-id="01bb6-116">Określa obiekt bramy aplikacji, który zawiera port frontonu.</span><span class="sxs-lookup"><span data-stu-id="01bb6-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="01bb6-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="01bb6-117">-Name</span></span>
<span data-ttu-id="01bb6-118">Określa nazwę portu frontonu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="01bb6-118">Specifies the name of the front-end port to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01bb6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01bb6-119">-DefaultProfile</span></span>
<span data-ttu-id="01bb6-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="01bb6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01bb6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01bb6-121">CommonParameters</span></span>
<span data-ttu-id="01bb6-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01bb6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01bb6-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01bb6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01bb6-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01bb6-124">INPUTS</span></span>

### <span data-ttu-id="01bb6-125">System. String</span><span class="sxs-lookup"><span data-stu-id="01bb6-125">System.String</span></span>

## <span data-ttu-id="01bb6-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01bb6-126">OUTPUTS</span></span>

### <span data-ttu-id="01bb6-127">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="01bb6-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="01bb6-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01bb6-128">NOTES</span></span>

## <span data-ttu-id="01bb6-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01bb6-129">RELATED LINKS</span></span>

[<span data-ttu-id="01bb6-130">Dodaj-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="01bb6-130">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="01bb6-131">Nowe — AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="01bb6-131">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="01bb6-132">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="01bb6-132">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="01bb6-133">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="01bb6-133">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)



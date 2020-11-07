---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 3ebe90d5f28adf0e7e4a9de66b04a1ea000cc69e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545603"
---
# <span data-ttu-id="6c35a-101">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c35a-101">Get-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="6c35a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c35a-102">SYNOPSIS</span></span>
<span data-ttu-id="6c35a-103">Pobiera konfigurację IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6c35a-103">Gets the IP configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c35a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c35a-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c35a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6c35a-105">DESCRIPTION</span></span>
<span data-ttu-id="6c35a-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayIPConfiguration** Pobiera konfigurację IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6c35a-106">The **Get-AzureRmApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="6c35a-107">Konfiguracja IP zawiera podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6c35a-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="6c35a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c35a-108">EXAMPLES</span></span>

### <span data-ttu-id="6c35a-109">Przykład 1: uzyskiwanie określonej konfiguracji adresów IP</span><span class="sxs-lookup"><span data-stu-id="6c35a-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzureRmApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="6c35a-110">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw. Drugie polecenie pobiera konfigurację IP o nazwie GateSubnet01 od bramy przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="6c35a-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="6c35a-111">Przykład 2: uzyskiwanie listy konfiguracji adresów IP</span><span class="sxs-lookup"><span data-stu-id="6c35a-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="6c35a-112">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw. Drugie polecenie otrzymuje listę wszystkich konfiguracji IP.</span><span class="sxs-lookup"><span data-stu-id="6c35a-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="6c35a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c35a-113">PARAMETERS</span></span>

### <span data-ttu-id="6c35a-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c35a-114">-ApplicationGateway</span></span>
<span data-ttu-id="6c35a-115">Określa obiekt bramy aplikacji, który zawiera konfigurację protokołu IP.</span><span class="sxs-lookup"><span data-stu-id="6c35a-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="6c35a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c35a-116">-DefaultProfile</span></span>
<span data-ttu-id="6c35a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c35a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c35a-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6c35a-118">-Name</span></span>
<span data-ttu-id="6c35a-119">Określa nazwę konfiguracji IP, którą jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c35a-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c35a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c35a-120">CommonParameters</span></span>
<span data-ttu-id="6c35a-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c35a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c35a-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c35a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c35a-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c35a-123">INPUTS</span></span>

### <span data-ttu-id="6c35a-124">System. String</span><span class="sxs-lookup"><span data-stu-id="6c35a-124">System.String</span></span>

## <span data-ttu-id="6c35a-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c35a-125">OUTPUTS</span></span>

### <span data-ttu-id="6c35a-126">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c35a-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="6c35a-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c35a-127">NOTES</span></span>

## <span data-ttu-id="6c35a-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c35a-128">RELATED LINKS</span></span>

[<span data-ttu-id="6c35a-129">Dodaj-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c35a-129">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="6c35a-130">Nowe — AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c35a-130">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="6c35a-131">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c35a-131">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="6c35a-132">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c35a-132">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


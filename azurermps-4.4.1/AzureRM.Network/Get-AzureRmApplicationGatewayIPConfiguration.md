---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 6959f75822143688249b97ee3beaa038ed33a2ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716679"
---
# <span data-ttu-id="addfe-101">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="addfe-101">Get-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="addfe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="addfe-102">SYNOPSIS</span></span>
<span data-ttu-id="addfe-103">Pobiera konfigurację IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="addfe-103">Gets the IP configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="addfe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="addfe-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="addfe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="addfe-105">DESCRIPTION</span></span>
<span data-ttu-id="addfe-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayIPConfiguration** Pobiera konfigurację IP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="addfe-106">The **Get-AzureRmApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="addfe-107">Konfiguracja IP zawiera podsieć, w której wdrożono bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="addfe-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="addfe-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="addfe-108">EXAMPLES</span></span>

### <span data-ttu-id="addfe-109">Przykład 1: uzyskiwanie określonej konfiguracji adresów IP</span><span class="sxs-lookup"><span data-stu-id="addfe-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzureRmApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="addfe-110">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw. Drugie polecenie pobiera konfigurację IP o nazwie GateSubnet01 od bramy przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="addfe-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="addfe-111">Przykład 2: uzyskiwanie listy konfiguracji adresów IP</span><span class="sxs-lookup"><span data-stu-id="addfe-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="addfe-112">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw. Drugie polecenie otrzymuje listę wszystkich konfiguracji IP.</span><span class="sxs-lookup"><span data-stu-id="addfe-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="addfe-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="addfe-113">PARAMETERS</span></span>

### <span data-ttu-id="addfe-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="addfe-114">-ApplicationGateway</span></span>
<span data-ttu-id="addfe-115">Określa obiekt bramy aplikacji, który zawiera konfigurację protokołu IP.</span><span class="sxs-lookup"><span data-stu-id="addfe-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="addfe-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="addfe-116">-Name</span></span>
<span data-ttu-id="addfe-117">Określa nazwę konfiguracji IP, którą jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="addfe-117">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

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

### <span data-ttu-id="addfe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="addfe-118">-DefaultProfile</span></span>
<span data-ttu-id="addfe-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="addfe-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="addfe-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="addfe-120">CommonParameters</span></span>
<span data-ttu-id="addfe-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="addfe-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="addfe-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="addfe-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="addfe-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="addfe-123">INPUTS</span></span>

### <span data-ttu-id="addfe-124">System. String</span><span class="sxs-lookup"><span data-stu-id="addfe-124">System.String</span></span>

## <span data-ttu-id="addfe-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="addfe-125">OUTPUTS</span></span>

### <span data-ttu-id="addfe-126">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="addfe-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="addfe-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="addfe-127">NOTES</span></span>

## <span data-ttu-id="addfe-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="addfe-128">RELATED LINKS</span></span>

[<span data-ttu-id="addfe-129">Dodaj-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="addfe-129">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="addfe-130">Nowe — AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="addfe-130">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="addfe-131">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="addfe-131">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="addfe-132">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="addfe-132">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)



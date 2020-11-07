---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: dd7ad8110afad4302c393295599ed1ef9d6fd4bf
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897618"
---
# <span data-ttu-id="d27c0-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d27c0-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="d27c0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d27c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d27c0-103">Pobiera tablicę mapowań ścieżek adresów URL do puli serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d27c0-103">Gets an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d27c0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d27c0-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d27c0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d27c0-105">DESCRIPTION</span></span>
<span data-ttu-id="d27c0-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayURLPathMapConfig** pobiera tablicę mapowań ścieżek adresów URL do puli serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d27c0-106">The **Get-AzureRmApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="d27c0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d27c0-107">EXAMPLES</span></span>

### <span data-ttu-id="d27c0-108">Przykład 1: Pobieranie konfiguracji mapowania ścieżki URL</span><span class="sxs-lookup"><span data-stu-id="d27c0-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="d27c0-109">To polecenie pobiera konfiguracje mapowania ścieżki URL z serwera wewnętrznej bazy danych znajdującego się na bramie Application Gateway o nazwie Gateway.</span><span class="sxs-lookup"><span data-stu-id="d27c0-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="d27c0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d27c0-110">PARAMETERS</span></span>

### <span data-ttu-id="d27c0-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d27c0-111">-ApplicationGateway</span></span>
<span data-ttu-id="d27c0-112">Określa bramę aplikacji, z którą to polecenie cmdlet pobiera konfigurację mapowania ścieżki adresu URL.</span><span class="sxs-lookup"><span data-stu-id="d27c0-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="d27c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d27c0-113">-DefaultProfile</span></span>
<span data-ttu-id="d27c0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d27c0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d27c0-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d27c0-115">-Name</span></span>
<span data-ttu-id="d27c0-116">Określa nazwę mapy ścieżki URL, w której to polecenie cmdlet umożliwia pobranie konfiguracji mapy ścieżki.</span><span class="sxs-lookup"><span data-stu-id="d27c0-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="d27c0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d27c0-117">CommonParameters</span></span>
<span data-ttu-id="d27c0-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d27c0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d27c0-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d27c0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d27c0-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d27c0-120">INPUTS</span></span>

### <span data-ttu-id="d27c0-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d27c0-121">PSApplicationGateway</span></span>
<span data-ttu-id="d27c0-122">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="d27c0-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="d27c0-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d27c0-123">OUTPUTS</span></span>

### <span data-ttu-id="d27c0-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="d27c0-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

### <span data-ttu-id="d27c0-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. models. PSApplicationGatewayUrlPathMap]</span><span class="sxs-lookup"><span data-stu-id="d27c0-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]</span></span>

## <span data-ttu-id="d27c0-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d27c0-126">NOTES</span></span>

## <span data-ttu-id="d27c0-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d27c0-127">RELATED LINKS</span></span>

[<span data-ttu-id="d27c0-128">Dodaj-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d27c0-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d27c0-129">Nowe — AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d27c0-129">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d27c0-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d27c0-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d27c0-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d27c0-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)



---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 68676c05757a58f2c1094e36338d17a52de6b040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527826"
---
# <span data-ttu-id="28686-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="28686-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="28686-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28686-102">SYNOPSIS</span></span>
<span data-ttu-id="28686-103">Usuwa mapowania ścieżek adresów URL do puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="28686-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28686-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28686-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28686-105">Opis</span><span class="sxs-lookup"><span data-stu-id="28686-105">DESCRIPTION</span></span>
<span data-ttu-id="28686-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayUrlPathMapConfig** usuwa mapowania ścieżek adresów URL do puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="28686-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="28686-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28686-107">EXAMPLES</span></span>

## <span data-ttu-id="28686-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28686-108">PARAMETERS</span></span>

### <span data-ttu-id="28686-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="28686-109">-ApplicationGateway</span></span>
<span data-ttu-id="28686-110">Określa bramę aplikacji, z którą to polecenie cmdlet usuwa konfigurację mapowania ścieżki adresu URL.</span><span class="sxs-lookup"><span data-stu-id="28686-110">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="28686-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28686-111">-DefaultProfile</span></span>
<span data-ttu-id="28686-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="28686-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28686-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="28686-113">-Name</span></span>
<span data-ttu-id="28686-114">Określa nazwę mapy ścieżki URL, którą to polecenie cmdlet usuwa z serwera wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="28686-114">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="28686-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28686-115">CommonParameters</span></span>
<span data-ttu-id="28686-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28686-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28686-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28686-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28686-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28686-118">INPUTS</span></span>

### <span data-ttu-id="28686-119">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="28686-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="28686-120">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="28686-120">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="28686-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28686-121">OUTPUTS</span></span>

### <span data-ttu-id="28686-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="28686-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="28686-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28686-123">NOTES</span></span>

## <span data-ttu-id="28686-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28686-124">RELATED LINKS</span></span>

[<span data-ttu-id="28686-125">Dodaj-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="28686-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="28686-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="28686-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="28686-127">Nowe — AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="28686-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="28686-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="28686-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)



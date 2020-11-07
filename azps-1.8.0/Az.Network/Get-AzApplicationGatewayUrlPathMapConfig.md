---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ac85a308b73d822846a2f2a0a7b9ddf9ccc05cbf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709589"
---
# <span data-ttu-id="26824-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26824-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="26824-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26824-102">SYNOPSIS</span></span>
<span data-ttu-id="26824-103">Pobiera tablicę mapowań ścieżek adresów URL do puli serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="26824-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="26824-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26824-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26824-105">Opis</span><span class="sxs-lookup"><span data-stu-id="26824-105">DESCRIPTION</span></span>
<span data-ttu-id="26824-106">Polecenie cmdlet **Get-AzApplicationGatewayURLPathMapConfig** pobiera tablicę mapowań ścieżek adresów URL do puli serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="26824-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="26824-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26824-107">EXAMPLES</span></span>

### <span data-ttu-id="26824-108">Przykład 1: Pobieranie konfiguracji mapowania ścieżki URL</span><span class="sxs-lookup"><span data-stu-id="26824-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="26824-109">To polecenie pobiera konfiguracje mapowania ścieżki URL z serwera wewnętrznej bazy danych znajdującego się na bramie Application Gateway o nazwie Gateway.</span><span class="sxs-lookup"><span data-stu-id="26824-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="26824-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26824-110">PARAMETERS</span></span>

### <span data-ttu-id="26824-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26824-111">-ApplicationGateway</span></span>
<span data-ttu-id="26824-112">Określa bramę aplikacji, z którą to polecenie cmdlet pobiera konfigurację mapowania ścieżki adresu URL.</span><span class="sxs-lookup"><span data-stu-id="26824-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="26824-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26824-113">-DefaultProfile</span></span>
<span data-ttu-id="26824-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="26824-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26824-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="26824-115">-Name</span></span>
<span data-ttu-id="26824-116">Określa nazwę mapy ścieżki URL, w której to polecenie cmdlet umożliwia pobranie konfiguracji mapy ścieżki.</span><span class="sxs-lookup"><span data-stu-id="26824-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="26824-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26824-117">CommonParameters</span></span>
<span data-ttu-id="26824-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26824-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26824-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26824-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26824-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26824-120">INPUTS</span></span>

### <span data-ttu-id="26824-121">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26824-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="26824-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26824-122">OUTPUTS</span></span>

### <span data-ttu-id="26824-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="26824-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="26824-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26824-124">NOTES</span></span>

## <span data-ttu-id="26824-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26824-125">RELATED LINKS</span></span>

[<span data-ttu-id="26824-126">Dodaj-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26824-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="26824-127">Nowe — AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26824-127">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="26824-128">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26824-128">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="26824-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26824-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


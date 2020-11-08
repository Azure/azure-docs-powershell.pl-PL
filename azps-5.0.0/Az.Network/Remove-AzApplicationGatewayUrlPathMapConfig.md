---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2c73be940e887b4cd1ca96da1442f8ae007ab6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224928"
---
# <span data-ttu-id="4c520-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4c520-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="4c520-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4c520-102">SYNOPSIS</span></span>
<span data-ttu-id="4c520-103">Usuwa mapowania ścieżek adresów URL do puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="4c520-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="4c520-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4c520-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c520-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4c520-105">DESCRIPTION</span></span>
<span data-ttu-id="4c520-106">Polecenie cmdlet **Remove-AzApplicationGatewayUrlPathMapConfig** usuwa mapowania ścieżek adresów URL do puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="4c520-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="4c520-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4c520-107">EXAMPLES</span></span>

### <span data-ttu-id="4c520-108">Przykład 1: Usuwanie mapowania ścieżki URL z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="4c520-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="4c520-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie appGwName i zapisuje wynik w zmiennej $appgw.</span><span class="sxs-lookup"><span data-stu-id="4c520-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="4c520-110">Drugie polecenie usuwa mapowanie ścieżki URL o nazwie map01 z bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4c520-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="4c520-111">W trzecim poleceniu jest aktualizowana Brama Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4c520-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="4c520-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c520-112">PARAMETERS</span></span>

### <span data-ttu-id="4c520-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c520-113">-ApplicationGateway</span></span>
<span data-ttu-id="4c520-114">Określa bramę aplikacji, z którą to polecenie cmdlet usuwa konfigurację mapowania ścieżki adresu URL.</span><span class="sxs-lookup"><span data-stu-id="4c520-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="4c520-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c520-115">-DefaultProfile</span></span>
<span data-ttu-id="4c520-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4c520-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c520-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4c520-117">-Name</span></span>
<span data-ttu-id="4c520-118">Określa nazwę mapy ścieżki URL, którą to polecenie cmdlet usuwa z serwera wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4c520-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="4c520-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c520-119">CommonParameters</span></span>
<span data-ttu-id="4c520-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c520-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c520-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c520-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c520-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c520-122">INPUTS</span></span>

### <span data-ttu-id="4c520-123">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c520-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4c520-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4c520-124">OUTPUTS</span></span>

### <span data-ttu-id="4c520-125">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c520-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4c520-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4c520-126">NOTES</span></span>

## <span data-ttu-id="4c520-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c520-127">RELATED LINKS</span></span>

[<span data-ttu-id="4c520-128">Dodaj-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4c520-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4c520-129">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4c520-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4c520-130">Nowe — AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4c520-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4c520-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4c520-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)



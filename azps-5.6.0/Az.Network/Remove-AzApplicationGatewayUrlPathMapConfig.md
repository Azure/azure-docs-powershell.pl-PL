---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 1d9caf3c95d7f8a508a41b8c047684b86c66227a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996437"
---
# <span data-ttu-id="98de8-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="98de8-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="98de8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98de8-102">SYNOPSIS</span></span>
<span data-ttu-id="98de8-103">Usuwa mapowania ścieżek adresów URL na pulę serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="98de8-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="98de8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="98de8-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98de8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="98de8-105">DESCRIPTION</span></span>
<span data-ttu-id="98de8-106">Polecenie **cmdlet Remove-AzApplicationGatewayUrlPathMapConfig** usuwa mapowania ścieżek adresów URL na pulę serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="98de8-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="98de8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="98de8-107">EXAMPLES</span></span>

### <span data-ttu-id="98de8-108">Przykład 1. Usuwanie mapowania ścieżki adresu URL z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="98de8-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="98de8-109">Pierwsze polecenie pobiera nazwę bramy aplikacji appGwName i zapisuje wynik w $appgw zmienną.</span><span class="sxs-lookup"><span data-stu-id="98de8-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="98de8-110">Drugie polecenie usuwa mapowanie ścieżki adresu URL o nazwie map01 z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="98de8-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="98de8-111">Trzecie polecenie aktualizuje bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="98de8-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="98de8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98de8-112">PARAMETERS</span></span>

### <span data-ttu-id="98de8-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="98de8-113">-ApplicationGateway</span></span>
<span data-ttu-id="98de8-114">Określa bramę aplikacji, do której to polecenie cmdlet usuwa konfigurację mapy ścieżki adresu URL.</span><span class="sxs-lookup"><span data-stu-id="98de8-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="98de8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98de8-115">-DefaultProfile</span></span>
<span data-ttu-id="98de8-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="98de8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98de8-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="98de8-117">-Name</span></span>
<span data-ttu-id="98de8-118">Określa nazwę mapy ścieżki adresu URL, którą to polecenie cmdlet usuwa z serwera zaplecza.</span><span class="sxs-lookup"><span data-stu-id="98de8-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="98de8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98de8-119">CommonParameters</span></span>
<span data-ttu-id="98de8-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98de8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98de8-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98de8-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98de8-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98de8-122">INPUTS</span></span>

### <span data-ttu-id="98de8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="98de8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="98de8-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98de8-124">OUTPUTS</span></span>

### <span data-ttu-id="98de8-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="98de8-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="98de8-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="98de8-126">NOTES</span></span>

## <span data-ttu-id="98de8-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98de8-127">RELATED LINKS</span></span>

[<span data-ttu-id="98de8-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="98de8-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="98de8-129">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="98de8-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="98de8-130">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="98de8-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="98de8-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="98de8-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)



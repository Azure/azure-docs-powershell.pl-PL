---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2c73be940e887b4cd1ca96da1442f8ae007ab6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191779"
---
# <span data-ttu-id="9daf2-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9daf2-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="9daf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9daf2-102">SYNOPSIS</span></span>
<span data-ttu-id="9daf2-103">Usuwa mapowania ścieżek adresów URL na pulę serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="9daf2-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="9daf2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9daf2-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9daf2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9daf2-105">DESCRIPTION</span></span>
<span data-ttu-id="9daf2-106">Polecenie **cmdlet Remove-AzApplicationGatewayUrlPathMapConfig** usuwa mapowania ścieżek adresów URL na pulę serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="9daf2-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="9daf2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9daf2-107">EXAMPLES</span></span>

### <span data-ttu-id="9daf2-108">Przykład 1. Usuwanie mapowania ścieżki adresu URL z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="9daf2-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="9daf2-109">Pierwsze polecenie pobiera nazwę bramy aplikacji appGwName i zapisuje wynik w $appgw zmienną.</span><span class="sxs-lookup"><span data-stu-id="9daf2-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="9daf2-110">Drugie polecenie usuwa mapowanie ścieżki adresu URL o nazwie map01 z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9daf2-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="9daf2-111">Trzecie polecenie aktualizuje bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9daf2-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="9daf2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9daf2-112">PARAMETERS</span></span>

### <span data-ttu-id="9daf2-113">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9daf2-113">-ApplicationGateway</span></span>
<span data-ttu-id="9daf2-114">Określa bramę aplikacji, do której to polecenie cmdlet usuwa konfigurację mapy ścieżki adresu URL.</span><span class="sxs-lookup"><span data-stu-id="9daf2-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="9daf2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9daf2-115">-DefaultProfile</span></span>
<span data-ttu-id="9daf2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9daf2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9daf2-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9daf2-117">-Name</span></span>
<span data-ttu-id="9daf2-118">Określa nazwę mapy ścieżki adresu URL, którą to polecenie cmdlet usuwa z serwera zaplecza.</span><span class="sxs-lookup"><span data-stu-id="9daf2-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="9daf2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9daf2-119">CommonParameters</span></span>
<span data-ttu-id="9daf2-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9daf2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9daf2-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9daf2-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9daf2-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9daf2-122">INPUTS</span></span>

### <span data-ttu-id="9daf2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9daf2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9daf2-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9daf2-124">OUTPUTS</span></span>

### <span data-ttu-id="9daf2-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9daf2-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9daf2-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9daf2-126">NOTES</span></span>

## <span data-ttu-id="9daf2-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9daf2-127">RELATED LINKS</span></span>

[<span data-ttu-id="9daf2-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9daf2-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9daf2-129">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9daf2-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9daf2-130">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9daf2-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9daf2-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9daf2-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)



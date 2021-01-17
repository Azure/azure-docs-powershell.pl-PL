---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: d376bc1e70d0441f139b64c19466a88daf6877c4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340702"
---
# <span data-ttu-id="8179a-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="8179a-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="8179a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8179a-102">SYNOPSIS</span></span>
<span data-ttu-id="8179a-103">Usuwa konfigurację frontonu IP od bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8179a-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="8179a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8179a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8179a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8179a-105">DESCRIPTION</span></span>
<span data-ttu-id="8179a-106">Polecenie cmdlet **Remove-AzApplicationGatewayFrontendIPConfig** usuwa adres IP frontonu z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8179a-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="8179a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8179a-107">EXAMPLES</span></span>

### <span data-ttu-id="8179a-108">Przykład 1: Usuwanie konfiguracji frontonu IP</span><span class="sxs-lookup"><span data-stu-id="8179a-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="8179a-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8179a-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8179a-110">Drugie polecenie usuwa konfigurację adresu IP frontonu o nazwie FrontEndIP02 od bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8179a-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="8179a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8179a-111">PARAMETERS</span></span>

### <span data-ttu-id="8179a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8179a-112">-ApplicationGateway</span></span>
<span data-ttu-id="8179a-113">Określa bramę aplikacji, z której ma zostać usunięta konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="8179a-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="8179a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8179a-114">-DefaultProfile</span></span>
<span data-ttu-id="8179a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8179a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8179a-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8179a-116">-Name</span></span>
<span data-ttu-id="8179a-117">Określa nazwę konfiguracji adresu IP frontonu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="8179a-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="8179a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8179a-118">CommonParameters</span></span>
<span data-ttu-id="8179a-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8179a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8179a-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8179a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8179a-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8179a-121">INPUTS</span></span>

### <span data-ttu-id="8179a-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8179a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8179a-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8179a-123">OUTPUTS</span></span>

### <span data-ttu-id="8179a-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8179a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8179a-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8179a-125">NOTES</span></span>

## <span data-ttu-id="8179a-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8179a-126">RELATED LINKS</span></span>

[<span data-ttu-id="8179a-127">Dodaj-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="8179a-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="8179a-128">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="8179a-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="8179a-129">Nowe — AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="8179a-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="8179a-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="8179a-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)



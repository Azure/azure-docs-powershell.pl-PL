---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: d376bc1e70d0441f139b64c19466a88daf6877c4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063354"
---
# <span data-ttu-id="f7fc3-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f7fc3-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="f7fc3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="f7fc3-103">Usuwa konfigurację frontonu IP od bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f7fc3-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="f7fc3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7fc3-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7fc3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f7fc3-105">DESCRIPTION</span></span>
<span data-ttu-id="f7fc3-106">Polecenie cmdlet **Remove-AzApplicationGatewayFrontendIPConfig** usuwa adres IP frontonu z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f7fc3-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="f7fc3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7fc3-107">EXAMPLES</span></span>

### <span data-ttu-id="f7fc3-108">Przykład 1: Usuwanie konfiguracji frontonu IP</span><span class="sxs-lookup"><span data-stu-id="f7fc3-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="f7fc3-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f7fc3-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f7fc3-110">Drugie polecenie usuwa konfigurację adresu IP frontonu o nazwie FrontEndIP02 od bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f7fc3-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="f7fc3-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7fc3-111">PARAMETERS</span></span>

### <span data-ttu-id="f7fc3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7fc3-112">-ApplicationGateway</span></span>
<span data-ttu-id="f7fc3-113">Określa bramę aplikacji, z której ma zostać usunięta konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="f7fc3-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f7fc3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7fc3-114">-DefaultProfile</span></span>
<span data-ttu-id="f7fc3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7fc3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7fc3-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f7fc3-116">-Name</span></span>
<span data-ttu-id="f7fc3-117">Określa nazwę konfiguracji adresu IP frontonu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f7fc3-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="f7fc3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7fc3-118">CommonParameters</span></span>
<span data-ttu-id="f7fc3-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7fc3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7fc3-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7fc3-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7fc3-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7fc3-121">INPUTS</span></span>

### <span data-ttu-id="f7fc3-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7fc3-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f7fc3-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7fc3-123">OUTPUTS</span></span>

### <span data-ttu-id="f7fc3-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7fc3-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f7fc3-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7fc3-125">NOTES</span></span>

## <span data-ttu-id="f7fc3-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7fc3-126">RELATED LINKS</span></span>

[<span data-ttu-id="f7fc3-127">Dodaj-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f7fc3-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f7fc3-128">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f7fc3-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f7fc3-129">Nowe — AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f7fc3-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f7fc3-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f7fc3-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)



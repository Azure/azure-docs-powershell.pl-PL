---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 72cc21b697b2dbdc05ad7106fca5687203aec870
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869784"
---
# <span data-ttu-id="cfb86-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="cfb86-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="cfb86-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cfb86-102">SYNOPSIS</span></span>
<span data-ttu-id="cfb86-103">Usuwa konfigurację frontonu IP od bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cfb86-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="cfb86-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cfb86-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfb86-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cfb86-105">DESCRIPTION</span></span>
<span data-ttu-id="cfb86-106">Polecenie cmdlet **Remove-AzApplicationGatewayFrontendIPConfig** usuwa adres IP frontonu z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cfb86-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="cfb86-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cfb86-107">EXAMPLES</span></span>

### <span data-ttu-id="cfb86-108">Przykład 1: Usuwanie konfiguracji frontonu IP</span><span class="sxs-lookup"><span data-stu-id="cfb86-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="cfb86-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="cfb86-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="cfb86-110">Drugie polecenie usuwa konfigurację adresu IP frontonu o nazwie FrontEndIP02 od bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="cfb86-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="cfb86-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cfb86-111">PARAMETERS</span></span>

### <span data-ttu-id="cfb86-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cfb86-112">-ApplicationGateway</span></span>
<span data-ttu-id="cfb86-113">Określa bramę aplikacji, z której ma zostać usunięta konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="cfb86-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="cfb86-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfb86-114">-DefaultProfile</span></span>
<span data-ttu-id="cfb86-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cfb86-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfb86-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cfb86-116">-Name</span></span>
<span data-ttu-id="cfb86-117">Określa nazwę konfiguracji adresu IP frontonu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="cfb86-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="cfb86-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfb86-118">CommonParameters</span></span>
<span data-ttu-id="cfb86-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfb86-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfb86-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfb86-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfb86-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cfb86-121">INPUTS</span></span>

### <span data-ttu-id="cfb86-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cfb86-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cfb86-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cfb86-123">OUTPUTS</span></span>

### <span data-ttu-id="cfb86-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cfb86-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cfb86-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cfb86-125">NOTES</span></span>

## <span data-ttu-id="cfb86-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cfb86-126">RELATED LINKS</span></span>

[<span data-ttu-id="cfb86-127">Dodaj-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="cfb86-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="cfb86-128">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="cfb86-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="cfb86-129">Nowe — AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="cfb86-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="cfb86-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="cfb86-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)



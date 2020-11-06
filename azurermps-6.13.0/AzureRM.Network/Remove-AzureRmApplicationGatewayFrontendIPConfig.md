---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 94cb9e07bc5d4b8d59e543c39ddada5386ebcb27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527838"
---
# <span data-ttu-id="40248-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="40248-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="40248-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40248-102">SYNOPSIS</span></span>
<span data-ttu-id="40248-103">Usuwa konfigurację frontonu IP od bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="40248-103">Removes a front-end IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40248-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40248-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40248-105">Opis</span><span class="sxs-lookup"><span data-stu-id="40248-105">DESCRIPTION</span></span>
<span data-ttu-id="40248-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayFrontendIPConfig** usuwa adres IP frontonu z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="40248-106">The **Remove-AzureRmApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="40248-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40248-107">EXAMPLES</span></span>

### <span data-ttu-id="40248-108">Przykład 1: Usuwanie konfiguracji frontonu IP</span><span class="sxs-lookup"><span data-stu-id="40248-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="40248-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="40248-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="40248-110">Drugie polecenie usuwa konfigurację adresu IP frontonu o nazwie FrontEndIP02 od bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="40248-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="40248-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40248-111">PARAMETERS</span></span>

### <span data-ttu-id="40248-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="40248-112">-ApplicationGateway</span></span>
<span data-ttu-id="40248-113">Określa bramę aplikacji, z której ma zostać usunięta konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="40248-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="40248-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40248-114">-DefaultProfile</span></span>
<span data-ttu-id="40248-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="40248-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40248-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="40248-116">-Name</span></span>
<span data-ttu-id="40248-117">Określa nazwę konfiguracji adresu IP frontonu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="40248-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="40248-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40248-118">CommonParameters</span></span>
<span data-ttu-id="40248-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40248-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40248-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40248-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40248-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40248-121">INPUTS</span></span>

### <span data-ttu-id="40248-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="40248-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="40248-123">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="40248-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="40248-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40248-124">OUTPUTS</span></span>

### <span data-ttu-id="40248-125">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="40248-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="40248-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40248-126">NOTES</span></span>

## <span data-ttu-id="40248-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40248-127">RELATED LINKS</span></span>

[<span data-ttu-id="40248-128">Dodaj-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="40248-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="40248-129">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="40248-129">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="40248-130">Nowe — AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="40248-130">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="40248-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="40248-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)



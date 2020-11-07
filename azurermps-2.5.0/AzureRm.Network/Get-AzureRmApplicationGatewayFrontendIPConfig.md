---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: c138ced515932d158bb2a4a067ed405d8084db4e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898381"
---
# <span data-ttu-id="b4117-101">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b4117-101">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="b4117-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4117-102">SYNOPSIS</span></span>
<span data-ttu-id="b4117-103">Pobiera konfigurację IP frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b4117-103">Gets the front-end IP configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4117-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4117-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4117-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b4117-105">DESCRIPTION</span></span>
<span data-ttu-id="b4117-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayFrontendIPConfig** Pobiera konfigurację IP frontonu bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b4117-106">The **Get-AzureRmApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="b4117-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4117-107">EXAMPLES</span></span>

### <span data-ttu-id="b4117-108">Przykład 1: uzyskiwanie określonej konfiguracji frontonu IP</span><span class="sxs-lookup"><span data-stu-id="b4117-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="b4117-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw. Drugie polecenie pobiera konfigurację IP frontonu o nazwie FrontEndIP01 z $AppGw i zapisuje ją w zmiennej $FrontEndIP.</span><span class="sxs-lookup"><span data-stu-id="b4117-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="b4117-110">Przykład 2: uzyskiwanie listy konfiguracji adresów IP frontonu</span><span class="sxs-lookup"><span data-stu-id="b4117-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzureRmApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="b4117-111">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw. Drugie polecenie pobiera listę konfiguracji adresów IP frontonu z $AppGw i zapisuje ją w zmiennej $FrontEndIPs.</span><span class="sxs-lookup"><span data-stu-id="b4117-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="b4117-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4117-112">PARAMETERS</span></span>

### <span data-ttu-id="b4117-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4117-113">-ApplicationGateway</span></span>
<span data-ttu-id="b4117-114">Określa obiekt bramy aplikacji, który zawiera konfigurację adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="b4117-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="b4117-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4117-115">-DefaultProfile</span></span>
<span data-ttu-id="b4117-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b4117-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4117-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b4117-117">-Name</span></span>
<span data-ttu-id="b4117-118">Określa nazwę konfiguracji adresu IP frontonu, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4117-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b4117-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4117-119">CommonParameters</span></span>
<span data-ttu-id="b4117-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4117-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4117-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4117-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4117-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4117-122">INPUTS</span></span>

### <span data-ttu-id="b4117-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b4117-123">System.String</span></span>

## <span data-ttu-id="b4117-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4117-124">OUTPUTS</span></span>

### <span data-ttu-id="b4117-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4117-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="b4117-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4117-126">NOTES</span></span>

## <span data-ttu-id="b4117-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4117-127">RELATED LINKS</span></span>

[<span data-ttu-id="b4117-128">Dodaj-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b4117-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b4117-129">Nowe — AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b4117-129">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b4117-130">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b4117-130">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b4117-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b4117-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)



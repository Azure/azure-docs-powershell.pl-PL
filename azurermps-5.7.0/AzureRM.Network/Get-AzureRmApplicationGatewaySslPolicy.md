---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3a25db38f26fe1714035acebba1063303cdc0934
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717501"
---
# <span data-ttu-id="f21ff-101">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="f21ff-101">Get-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="f21ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f21ff-102">SYNOPSIS</span></span>
<span data-ttu-id="f21ff-103">Pobiera zasady SSL bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f21ff-103">Gets the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f21ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f21ff-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f21ff-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f21ff-105">DESCRIPTION</span></span>
<span data-ttu-id="f21ff-106">Polecenie cmdlet **Get-AzureRmApplicationGatewaySslPolicy** pobiera zasady SSL bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f21ff-106">The **Get-AzureRmApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="f21ff-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f21ff-107">EXAMPLES</span></span>

### <span data-ttu-id="f21ff-108">1:1</span><span class="sxs-lookup"><span data-stu-id="f21ff-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="f21ff-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="f21ff-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="f21ff-110">Drugie polecenie pobiera zasady SSL z bramy Application Gateway zapisanej w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="f21ff-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="f21ff-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f21ff-111">PARAMETERS</span></span>

### <span data-ttu-id="f21ff-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f21ff-112">-ApplicationGateway</span></span>
<span data-ttu-id="f21ff-113">Określa bramę aplikacji dla zasad SSL, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f21ff-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f21ff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f21ff-114">-DefaultProfile</span></span>
<span data-ttu-id="f21ff-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f21ff-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f21ff-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f21ff-116">CommonParameters</span></span>
<span data-ttu-id="f21ff-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f21ff-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f21ff-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f21ff-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f21ff-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f21ff-119">INPUTS</span></span>

### <span data-ttu-id="f21ff-120">System. String</span><span class="sxs-lookup"><span data-stu-id="f21ff-120">System.String</span></span>

## <span data-ttu-id="f21ff-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f21ff-121">OUTPUTS</span></span>

### <span data-ttu-id="f21ff-122">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="f21ff-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="f21ff-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f21ff-123">NOTES</span></span>
* <span data-ttu-id="f21ff-124">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="f21ff-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f21ff-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f21ff-125">RELATED LINKS</span></span>

[<span data-ttu-id="f21ff-126">Nowe — AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="f21ff-126">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="f21ff-127">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="f21ff-127">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)



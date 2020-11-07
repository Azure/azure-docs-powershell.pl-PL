---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayipconfiguration
schema: 2.0.0
ms.openlocfilehash: 901d8209cc18a5d64285bf45f7169d55d3c7a41e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899100"
---
# <span data-ttu-id="3103b-101">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3103b-101">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="3103b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3103b-102">SYNOPSIS</span></span>
<span data-ttu-id="3103b-103">Usuwa konfigurację IP z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3103b-103">Removes an IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3103b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3103b-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3103b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3103b-105">DESCRIPTION</span></span>
<span data-ttu-id="3103b-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayIPConfiguration** usuwa konfigurację IP z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3103b-106">The **Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="3103b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3103b-107">EXAMPLES</span></span>

### <span data-ttu-id="3103b-108">Przykład 1: Usuwanie konfiguracji adresów IP z bramy aplikacji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="3103b-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="3103b-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3103b-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="3103b-110">Drugie polecenie usuwa konfigurację adresu IP o nazwie Subnet02 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3103b-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="3103b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3103b-111">PARAMETERS</span></span>

### <span data-ttu-id="3103b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3103b-112">-ApplicationGateway</span></span>
<span data-ttu-id="3103b-113">Określa bramę aplikacji, z której ma zostać usunięta Konfiguracja IP.</span><span class="sxs-lookup"><span data-stu-id="3103b-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="3103b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3103b-114">-DefaultProfile</span></span>
<span data-ttu-id="3103b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3103b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3103b-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3103b-116">-Name</span></span>
<span data-ttu-id="3103b-117">Określa nazwę konfiguracji IP, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="3103b-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="3103b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3103b-118">CommonParameters</span></span>
<span data-ttu-id="3103b-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3103b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3103b-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3103b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3103b-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3103b-121">INPUTS</span></span>

### <span data-ttu-id="3103b-122">System. String</span><span class="sxs-lookup"><span data-stu-id="3103b-122">System.String</span></span>

## <span data-ttu-id="3103b-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3103b-123">OUTPUTS</span></span>

### <span data-ttu-id="3103b-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3103b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3103b-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3103b-125">NOTES</span></span>

## <span data-ttu-id="3103b-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3103b-126">RELATED LINKS</span></span>

[<span data-ttu-id="3103b-127">Dodaj-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3103b-127">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="3103b-128">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3103b-128">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="3103b-129">Nowe — AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3103b-129">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="3103b-130">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3103b-130">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)



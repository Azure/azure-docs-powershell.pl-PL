---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 884ff52132af34dad7c4498653233f0b122555ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552695"
---
# <span data-ttu-id="8ca1b-101">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ca1b-101">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="8ca1b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ca1b-102">SYNOPSIS</span></span>
<span data-ttu-id="8ca1b-103">Usuwa konfigurację IP z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8ca1b-103">Removes an IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ca1b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ca1b-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ca1b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8ca1b-105">DESCRIPTION</span></span>
<span data-ttu-id="8ca1b-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayIPConfiguration** usuwa konfigurację IP z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8ca1b-106">The **Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="8ca1b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ca1b-107">EXAMPLES</span></span>

### <span data-ttu-id="8ca1b-108">Przykład 1: Usuwanie konfiguracji adresów IP z bramy aplikacji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="8ca1b-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="8ca1b-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8ca1b-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8ca1b-110">Drugie polecenie usuwa konfigurację adresu IP o nazwie Subnet02 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8ca1b-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="8ca1b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ca1b-111">PARAMETERS</span></span>

### <span data-ttu-id="8ca1b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8ca1b-112">-ApplicationGateway</span></span>
<span data-ttu-id="8ca1b-113">Określa bramę aplikacji, z której ma zostać usunięta Konfiguracja IP.</span><span class="sxs-lookup"><span data-stu-id="8ca1b-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="8ca1b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ca1b-114">-DefaultProfile</span></span>
<span data-ttu-id="8ca1b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ca1b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ca1b-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8ca1b-116">-Name</span></span>
<span data-ttu-id="8ca1b-117">Określa nazwę konfiguracji IP, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="8ca1b-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="8ca1b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ca1b-118">CommonParameters</span></span>
<span data-ttu-id="8ca1b-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ca1b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ca1b-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ca1b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ca1b-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ca1b-121">INPUTS</span></span>

### <span data-ttu-id="8ca1b-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8ca1b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="8ca1b-123">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8ca1b-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="8ca1b-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ca1b-124">OUTPUTS</span></span>

### <span data-ttu-id="8ca1b-125">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8ca1b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8ca1b-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ca1b-126">NOTES</span></span>

## <span data-ttu-id="8ca1b-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ca1b-127">RELATED LINKS</span></span>

[<span data-ttu-id="8ca1b-128">Dodaj-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ca1b-128">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8ca1b-129">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ca1b-129">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8ca1b-130">Nowe — AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ca1b-130">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8ca1b-131">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ca1b-131">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)



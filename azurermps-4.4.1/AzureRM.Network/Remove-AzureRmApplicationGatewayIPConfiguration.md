---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 4ef644fb92bf3f872a9e80aef2674a3ffb56747b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546224"
---
# <span data-ttu-id="181f0-101">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="181f0-101">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="181f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="181f0-102">SYNOPSIS</span></span>
<span data-ttu-id="181f0-103">Usuwa konfigurację IP z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="181f0-103">Removes an IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="181f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="181f0-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="181f0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="181f0-105">DESCRIPTION</span></span>
<span data-ttu-id="181f0-106">Polecenie cmdlet **Remove-AzureRmApplicationGatewayIPConfiguration** usuwa konfigurację IP z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="181f0-106">The **Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="181f0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="181f0-107">EXAMPLES</span></span>

### <span data-ttu-id="181f0-108">Przykład 1: Usuwanie konfiguracji adresów IP z bramy aplikacji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="181f0-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="181f0-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="181f0-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="181f0-110">Drugie polecenie usuwa konfigurację adresu IP o nazwie Subnet02 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="181f0-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="181f0-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="181f0-111">PARAMETERS</span></span>

### <span data-ttu-id="181f0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="181f0-112">-ApplicationGateway</span></span>
<span data-ttu-id="181f0-113">Określa bramę aplikacji, z której ma zostać usunięta Konfiguracja IP.</span><span class="sxs-lookup"><span data-stu-id="181f0-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="181f0-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="181f0-114">-Name</span></span>
<span data-ttu-id="181f0-115">Określa nazwę konfiguracji IP, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="181f0-115">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="181f0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="181f0-116">-DefaultProfile</span></span>
<span data-ttu-id="181f0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="181f0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="181f0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="181f0-118">CommonParameters</span></span>
<span data-ttu-id="181f0-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="181f0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="181f0-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="181f0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="181f0-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="181f0-121">INPUTS</span></span>

### <span data-ttu-id="181f0-122">System. String</span><span class="sxs-lookup"><span data-stu-id="181f0-122">System.String</span></span>

## <span data-ttu-id="181f0-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="181f0-123">OUTPUTS</span></span>

### <span data-ttu-id="181f0-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="181f0-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="181f0-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="181f0-125">NOTES</span></span>

## <span data-ttu-id="181f0-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="181f0-126">RELATED LINKS</span></span>

[<span data-ttu-id="181f0-127">Dodaj-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="181f0-127">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="181f0-128">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="181f0-128">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="181f0-129">Nowe — AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="181f0-129">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="181f0-130">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="181f0-130">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)



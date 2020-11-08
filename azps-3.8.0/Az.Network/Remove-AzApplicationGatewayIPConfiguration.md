---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 87f6f441220f1f8ab47fee5356bddca8d02b96c0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049316"
---
# <span data-ttu-id="d01db-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d01db-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="d01db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d01db-102">SYNOPSIS</span></span>
<span data-ttu-id="d01db-103">Usuwa konfigurację IP z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d01db-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="d01db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d01db-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d01db-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d01db-105">DESCRIPTION</span></span>
<span data-ttu-id="d01db-106">Polecenie cmdlet **Remove-AzApplicationGatewayIPConfiguration** usuwa konfigurację IP z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d01db-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="d01db-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d01db-107">EXAMPLES</span></span>

### <span data-ttu-id="d01db-108">Przykład 1: Usuwanie konfiguracji adresów IP z bramy aplikacji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d01db-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="d01db-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d01db-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d01db-110">Drugie polecenie usuwa konfigurację adresu IP o nazwie Subnet02 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d01db-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="d01db-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d01db-111">PARAMETERS</span></span>

### <span data-ttu-id="d01db-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d01db-112">-ApplicationGateway</span></span>
<span data-ttu-id="d01db-113">Określa bramę aplikacji, z której ma zostać usunięta Konfiguracja IP.</span><span class="sxs-lookup"><span data-stu-id="d01db-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="d01db-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d01db-114">-DefaultProfile</span></span>
<span data-ttu-id="d01db-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d01db-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d01db-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d01db-116">-Name</span></span>
<span data-ttu-id="d01db-117">Określa nazwę konfiguracji IP, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="d01db-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="d01db-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d01db-118">CommonParameters</span></span>
<span data-ttu-id="d01db-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d01db-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d01db-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d01db-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d01db-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d01db-121">INPUTS</span></span>

### <span data-ttu-id="d01db-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d01db-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d01db-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d01db-123">OUTPUTS</span></span>

### <span data-ttu-id="d01db-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d01db-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d01db-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d01db-125">NOTES</span></span>

## <span data-ttu-id="d01db-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d01db-126">RELATED LINKS</span></span>

[<span data-ttu-id="d01db-127">Dodaj-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d01db-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="d01db-128">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d01db-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="d01db-129">Nowe — AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d01db-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="d01db-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d01db-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)



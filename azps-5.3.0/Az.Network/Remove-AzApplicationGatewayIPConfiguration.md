---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 87f6f441220f1f8ab47fee5356bddca8d02b96c0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503229"
---
# <span data-ttu-id="59bba-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="59bba-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="59bba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="59bba-102">SYNOPSIS</span></span>
<span data-ttu-id="59bba-103">Usuwa konfigurację IP z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="59bba-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="59bba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="59bba-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59bba-105">Opis</span><span class="sxs-lookup"><span data-stu-id="59bba-105">DESCRIPTION</span></span>
<span data-ttu-id="59bba-106">Polecenie cmdlet **Remove-AzApplicationGatewayIPConfiguration** usuwa konfigurację IP z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="59bba-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="59bba-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="59bba-107">EXAMPLES</span></span>

### <span data-ttu-id="59bba-108">Przykład 1: Usuwanie konfiguracji adresów IP z bramy aplikacji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="59bba-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="59bba-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="59bba-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="59bba-110">Drugie polecenie usuwa konfigurację adresu IP o nazwie Subnet02 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="59bba-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="59bba-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="59bba-111">PARAMETERS</span></span>

### <span data-ttu-id="59bba-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="59bba-112">-ApplicationGateway</span></span>
<span data-ttu-id="59bba-113">Określa bramę aplikacji, z której ma zostać usunięta Konfiguracja IP.</span><span class="sxs-lookup"><span data-stu-id="59bba-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="59bba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59bba-114">-DefaultProfile</span></span>
<span data-ttu-id="59bba-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="59bba-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59bba-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="59bba-116">-Name</span></span>
<span data-ttu-id="59bba-117">Określa nazwę konfiguracji IP, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="59bba-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="59bba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59bba-118">CommonParameters</span></span>
<span data-ttu-id="59bba-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59bba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59bba-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59bba-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59bba-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59bba-121">INPUTS</span></span>

### <span data-ttu-id="59bba-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="59bba-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="59bba-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="59bba-123">OUTPUTS</span></span>

### <span data-ttu-id="59bba-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="59bba-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="59bba-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="59bba-125">NOTES</span></span>

## <span data-ttu-id="59bba-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59bba-126">RELATED LINKS</span></span>

[<span data-ttu-id="59bba-127">Dodaj-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="59bba-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="59bba-128">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="59bba-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="59bba-129">Nowe — AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="59bba-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="59bba-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="59bba-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)



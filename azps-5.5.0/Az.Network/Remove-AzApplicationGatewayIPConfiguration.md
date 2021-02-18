---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 87f6f441220f1f8ab47fee5356bddca8d02b96c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240698"
---
# <span data-ttu-id="fe195-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe195-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="fe195-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe195-102">SYNOPSIS</span></span>
<span data-ttu-id="fe195-103">Usuwa konfigurację adresów IP z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fe195-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="fe195-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fe195-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe195-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fe195-105">DESCRIPTION</span></span>
<span data-ttu-id="fe195-106">Polecenie **cmdlet Remove-AzApplicationGatewayIPConfiguration** usuwa konfigurację adresów IP z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fe195-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="fe195-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fe195-107">EXAMPLES</span></span>

### <span data-ttu-id="fe195-108">Przykład 1. Usuwanie konfiguracji protokołu IP z bramy aplikacji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="fe195-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="fe195-109">Pierwsze polecenie pobiera bramę aplikacji i przechowuje je w $AppGw aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fe195-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fe195-110">Drugie polecenie usuwa konfigurację adresów IP o nazwie Subnet02 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="fe195-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="fe195-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe195-111">PARAMETERS</span></span>

### <span data-ttu-id="fe195-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe195-112">-ApplicationGateway</span></span>
<span data-ttu-id="fe195-113">Określa bramę aplikacji, z której ma być usuwana konfiguracja adresu IP.</span><span class="sxs-lookup"><span data-stu-id="fe195-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="fe195-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe195-114">-DefaultProfile</span></span>
<span data-ttu-id="fe195-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe195-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe195-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fe195-116">-Name</span></span>
<span data-ttu-id="fe195-117">Określa nazwę konfiguracji protokołu IP do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="fe195-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="fe195-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe195-118">CommonParameters</span></span>
<span data-ttu-id="fe195-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe195-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe195-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe195-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe195-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe195-121">INPUTS</span></span>

### <span data-ttu-id="fe195-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe195-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fe195-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe195-123">OUTPUTS</span></span>

### <span data-ttu-id="fe195-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe195-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fe195-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fe195-125">NOTES</span></span>

## <span data-ttu-id="fe195-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe195-126">RELATED LINKS</span></span>

[<span data-ttu-id="fe195-127">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe195-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="fe195-128">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe195-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="fe195-129">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe195-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="fe195-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe195-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 78af871cf476ee80c57e22e2469b48bb4d4337a1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179379"
---
# <span data-ttu-id="9cbc3-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="9cbc3-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="9cbc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cbc3-102">SYNOPSIS</span></span>
<span data-ttu-id="9cbc3-103">Modyfikuje konfigurację privatelinku dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-103">Modifies an PrivateLink Configuration for an application gateway.</span></span>

## <span data-ttu-id="9cbc3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9cbc3-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cbc3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9cbc3-105">DESCRIPTION</span></span>
<span data-ttu-id="9cbc3-106">Polecenie **cmdlet Set-AzApplicationGatewayPrivateLinkConfiguration** modyfikuje konfigurację privateLink bramy aplikacji Azure.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-106">The **Set-AzApplicationGatewayPrivateLinkConfiguration** cmdlet modifies an privateLink configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="9cbc3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9cbc3-107">EXAMPLES</span></span>

### <span data-ttu-id="9cbc3-108">Przykład 1. Ustawianie konfiguracji privatelinku</span><span class="sxs-lookup"><span data-stu-id="9cbc3-108">Example 1: Set a PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration01
```

<span data-ttu-id="9cbc3-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9cbc3-110">Drugie polecenie ustawia konfigurację privateLink o nazwie privateLinkConfig01 na używanie konfiguracji adresów IP przechowywanej w u $privateLinkIpConfiguration 01</span><span class="sxs-lookup"><span data-stu-id="9cbc3-110">The second command sets the privateLink configuration with name privateLinkConfig01 to use the ip configuration stored in $privateLinkIpConfiguration01</span></span>

## <span data-ttu-id="9cbc3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cbc3-111">PARAMETERS</span></span>

### <span data-ttu-id="9cbc3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9cbc3-112">-ApplicationGateway</span></span>
<span data-ttu-id="9cbc3-113">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="9cbc3-113">The applicationGateway</span></span>

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

### <span data-ttu-id="9cbc3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cbc3-114">-DefaultProfile</span></span>
<span data-ttu-id="9cbc3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cbc3-116">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9cbc3-116">-IpConfiguration</span></span>
<span data-ttu-id="9cbc3-117">Lista konfiguracji ip</span><span class="sxs-lookup"><span data-stu-id="9cbc3-117">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbc3-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9cbc3-118">-Name</span></span>
<span data-ttu-id="9cbc3-119">Nazwa konfiguracji privateLink</span><span class="sxs-lookup"><span data-stu-id="9cbc3-119">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="9cbc3-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9cbc3-120">-Confirm</span></span>
<span data-ttu-id="9cbc3-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cbc3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cbc3-122">-WhatIf</span></span>
<span data-ttu-id="9cbc3-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cbc3-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cbc3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cbc3-125">CommonParameters</span></span>
<span data-ttu-id="9cbc3-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cbc3-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9cbc3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cbc3-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cbc3-128">INPUTS</span></span>

### <span data-ttu-id="9cbc3-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9cbc3-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="9cbc3-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="9cbc3-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="9cbc3-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9cbc3-131">OUTPUTS</span></span>

### <span data-ttu-id="9cbc3-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9cbc3-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9cbc3-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9cbc3-133">NOTES</span></span>

## <span data-ttu-id="9cbc3-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9cbc3-134">RELATED LINKS</span></span>

[<span data-ttu-id="9cbc3-135">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="9cbc3-135">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="9cbc3-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="9cbc3-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="9cbc3-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="9cbc3-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="9cbc3-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="9cbc3-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)
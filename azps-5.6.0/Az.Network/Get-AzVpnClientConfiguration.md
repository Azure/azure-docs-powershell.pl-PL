---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: 03ed4fe9ad6e8b2e7c5af0b24e29c351a2b776f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010426"
---
# <span data-ttu-id="4bb6f-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bb6f-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="4bb6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bb6f-102">SYNOPSIS</span></span>
<span data-ttu-id="4bb6f-103">Umożliwia użytkownikom łatwe pobieranie pakietu profilu vpn wygenerowanego za pomocą New-AzVpnClientConfiguration commandlet.</span><span class="sxs-lookup"><span data-stu-id="4bb6f-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="4bb6f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4bb6f-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bb6f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4bb6f-105">DESCRIPTION</span></span>
<span data-ttu-id="4bb6f-106">Adres Get-AzVpnClientConfiguration URL, z którego można pobrać klienta SIECI VPN.</span><span class="sxs-lookup"><span data-stu-id="4bb6f-106">The Get-AzVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="4bb6f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4bb6f-107">EXAMPLES</span></span>

### <span data-ttu-id="4bb6f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4bb6f-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="4bb6f-109">Pobiera adres URL, aby pobrać profil usługi VpnClient, który został wcześniej wygenerowany przy użyciu New-AzVpnClientConfiguration sieci.</span><span class="sxs-lookup"><span data-stu-id="4bb6f-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="4bb6f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bb6f-110">PARAMETERS</span></span>

### <span data-ttu-id="4bb6f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bb6f-111">-DefaultProfile</span></span>
<span data-ttu-id="4bb6f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb6f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bb6f-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4bb6f-113">-Name</span></span>
<span data-ttu-id="4bb6f-114">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="4bb6f-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb6f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bb6f-115">-ResourceGroupName</span></span>
<span data-ttu-id="4bb6f-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4bb6f-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb6f-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4bb6f-117">-Confirm</span></span>
<span data-ttu-id="4bb6f-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4bb6f-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bb6f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bb6f-119">-WhatIf</span></span>
<span data-ttu-id="4bb6f-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bb6f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4bb6f-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4bb6f-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bb6f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bb6f-122">CommonParameters</span></span>
<span data-ttu-id="4bb6f-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bb6f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bb6f-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4bb6f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bb6f-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4bb6f-125">INPUTS</span></span>

### <span data-ttu-id="4bb6f-126">System.String</span><span class="sxs-lookup"><span data-stu-id="4bb6f-126">System.String</span></span>

## <span data-ttu-id="4bb6f-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4bb6f-127">OUTPUTS</span></span>

### <span data-ttu-id="4bb6f-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="4bb6f-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="4bb6f-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4bb6f-129">NOTES</span></span>

## <span data-ttu-id="4bb6f-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4bb6f-130">RELATED LINKS</span></span>

[<span data-ttu-id="4bb6f-131">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bb6f-131">New-AzVpnClientConfiguration</span></span>](./New-AzVpnClientConfiguration.md)

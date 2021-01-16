---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: ba73b61d34e0f6422defb9e9d6f84c22945ec124
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379696"
---
# <span data-ttu-id="3b342-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b342-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="3b342-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b342-102">SYNOPSIS</span></span>
<span data-ttu-id="3b342-103">Umożliwia użytkownikom łatwe pobieranie pakietu profilu sieci VPN wygenerowanego przy użyciu New-AzVpnClientConfiguration unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="3b342-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="3b342-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b342-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b342-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3b342-105">DESCRIPTION</span></span>
<span data-ttu-id="3b342-106">Get-AzVpnClientConfiguration zwraca adres URL, z którego można pobrać klienta sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="3b342-106">The Get-AzVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="3b342-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b342-107">EXAMPLES</span></span>

### <span data-ttu-id="3b342-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3b342-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="3b342-109">Pobiera adres URL umożliwiający pobranie profilu VpnClient, który został wcześniej wygenerowany przy użyciu polecenia New-AzVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3b342-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="3b342-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b342-110">PARAMETERS</span></span>

### <span data-ttu-id="3b342-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b342-111">-DefaultProfile</span></span>
<span data-ttu-id="3b342-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b342-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b342-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3b342-113">-Name</span></span>
<span data-ttu-id="3b342-114">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="3b342-114">The resource name.</span></span>

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

### <span data-ttu-id="3b342-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b342-115">-ResourceGroupName</span></span>
<span data-ttu-id="3b342-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3b342-116">The resource group name.</span></span>

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

### <span data-ttu-id="3b342-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3b342-117">-Confirm</span></span>
<span data-ttu-id="3b342-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b342-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b342-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b342-119">-WhatIf</span></span>
<span data-ttu-id="3b342-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b342-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b342-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3b342-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b342-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b342-122">CommonParameters</span></span>
<span data-ttu-id="3b342-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b342-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b342-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b342-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b342-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b342-125">INPUTS</span></span>

### <span data-ttu-id="3b342-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3b342-126">System.String</span></span>

## <span data-ttu-id="3b342-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b342-127">OUTPUTS</span></span>

### <span data-ttu-id="3b342-128">Microsoft. Azure. Commands. Network. models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="3b342-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="3b342-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b342-129">NOTES</span></span>

## <span data-ttu-id="3b342-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b342-130">RELATED LINKS</span></span>

[<span data-ttu-id="3b342-131">Nowe — AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b342-131">New-AzVpnClientConfiguration</span></span>](./New-AzVpnClientConfiguration.md)

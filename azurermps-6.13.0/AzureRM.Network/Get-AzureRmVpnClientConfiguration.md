---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
ms.openlocfilehash: 9ab4af1eefa6214d43eca84f65053eeecb12d912
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543739"
---
# <span data-ttu-id="e692d-101">Get-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="e692d-101">Get-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="e692d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e692d-102">SYNOPSIS</span></span>
<span data-ttu-id="e692d-103">Umożliwia użytkownikom łatwe pobieranie pakietu profilu sieci VPN wygenerowanego przy użyciu New-AzureRmVpnClientConfiguration unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="e692d-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzureRmVpnClientConfiguration commandlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e692d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e692d-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e692d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e692d-105">DESCRIPTION</span></span>
<span data-ttu-id="e692d-106">Get-AzureRmVpnClientConfiguration zwraca adres URL, z którego można pobrać klienta sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="e692d-106">The Get-AzureRmVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="e692d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e692d-107">EXAMPLES</span></span>

### <span data-ttu-id="e692d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e692d-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="e692d-109">Pobiera adres URL umożliwiający pobranie profilu VpnClient, który został wcześniej wygenerowany przy użyciu polecenia New-AzureRMVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e692d-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzureRMVpnClientConfiguration command.</span></span>

## <span data-ttu-id="e692d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e692d-110">PARAMETERS</span></span>

### <span data-ttu-id="e692d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e692d-111">-DefaultProfile</span></span>
<span data-ttu-id="e692d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e692d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e692d-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e692d-113">-Name</span></span>
<span data-ttu-id="e692d-114">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="e692d-114">The resource name.</span></span>

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

### <span data-ttu-id="e692d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e692d-115">-ResourceGroupName</span></span>
<span data-ttu-id="e692d-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e692d-116">The resource group name.</span></span>

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

### <span data-ttu-id="e692d-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e692d-117">-Confirm</span></span>
<span data-ttu-id="e692d-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e692d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e692d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e692d-119">-WhatIf</span></span>
<span data-ttu-id="e692d-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e692d-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e692d-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e692d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e692d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e692d-122">CommonParameters</span></span>
<span data-ttu-id="e692d-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e692d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e692d-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e692d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e692d-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e692d-125">INPUTS</span></span>

### <span data-ttu-id="e692d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e692d-126">System.String</span></span>

## <span data-ttu-id="e692d-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e692d-127">OUTPUTS</span></span>

### <span data-ttu-id="e692d-128">Microsoft. Azure. Commands. Network. models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="e692d-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="e692d-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e692d-129">NOTES</span></span>

## <span data-ttu-id="e692d-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e692d-130">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientconfiguration
schema: 2.0.0
ms.openlocfilehash: 4d6e95534cdadd694fa2ed87d43d3f7387ec9b20
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897925"
---
# <span data-ttu-id="7663c-101">Get-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="7663c-101">Get-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="7663c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7663c-102">SYNOPSIS</span></span>
<span data-ttu-id="7663c-103">Umożliwia użytkownikom łatwe pobieranie pakietu profilu sieci VPN wygenerowanego przy użyciu New-AzureRmVpnClientConfiguration unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="7663c-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzureRmVpnClientConfiguration commandlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7663c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7663c-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7663c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7663c-105">DESCRIPTION</span></span>
<span data-ttu-id="7663c-106">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="7663c-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="7663c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7663c-107">EXAMPLES</span></span>

### <span data-ttu-id="7663c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7663c-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="7663c-109">Pobiera adres URL umożliwiający pobranie profilu VpnClient, który został wcześniej wygenerowany przy użyciu polecenia New-AzureRMVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7663c-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzureRMVpnClientConfiguration command.</span></span>

## <span data-ttu-id="7663c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7663c-110">PARAMETERS</span></span>

### <span data-ttu-id="7663c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7663c-111">-DefaultProfile</span></span>
<span data-ttu-id="7663c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7663c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="7663c-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7663c-113">-Name</span></span>
<span data-ttu-id="7663c-114">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="7663c-114">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7663c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7663c-115">-ResourceGroupName</span></span>
<span data-ttu-id="7663c-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7663c-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7663c-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7663c-117">-Confirm</span></span>
<span data-ttu-id="7663c-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7663c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7663c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7663c-119">-WhatIf</span></span>
<span data-ttu-id="7663c-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7663c-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7663c-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7663c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7663c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7663c-122">CommonParameters</span></span>
<span data-ttu-id="7663c-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7663c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7663c-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7663c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7663c-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7663c-125">INPUTS</span></span>

### <span data-ttu-id="7663c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7663c-126">System.String</span></span>

## <span data-ttu-id="7663c-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7663c-127">OUTPUTS</span></span>

### <span data-ttu-id="7663c-128">Microsoft. Azure. Commands. Network. models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="7663c-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="7663c-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7663c-129">NOTES</span></span>

## <span data-ttu-id="7663c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7663c-130">RELATED LINKS</span></span>


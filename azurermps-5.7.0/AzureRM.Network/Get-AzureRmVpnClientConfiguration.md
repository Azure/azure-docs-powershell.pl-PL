---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
ms.openlocfilehash: 09c3862513b893003908b07992ae479656ba7ab1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554118"
---
# <span data-ttu-id="f9669-101">Get-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9669-101">Get-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="f9669-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9669-102">SYNOPSIS</span></span>
<span data-ttu-id="f9669-103">Umożliwia użytkownikom łatwe pobieranie pakietu profilu sieci VPN wygenerowanego przy użyciu New-AzureRmVpnClientConfiguration unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="f9669-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzureRmVpnClientConfiguration commandlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9669-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9669-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9669-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f9669-105">DESCRIPTION</span></span>
<span data-ttu-id="f9669-106">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="f9669-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="f9669-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9669-107">EXAMPLES</span></span>

### <span data-ttu-id="f9669-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f9669-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="f9669-109">Pobiera adres URL umożliwiający pobranie profilu VpnClient, który został wcześniej wygenerowany przy użyciu polecenia New-AzureRMVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f9669-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzureRMVpnClientConfiguration command.</span></span>

## <span data-ttu-id="f9669-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9669-110">PARAMETERS</span></span>

### <span data-ttu-id="f9669-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9669-111">-DefaultProfile</span></span>
<span data-ttu-id="f9669-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9669-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="f9669-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f9669-113">-Name</span></span>
<span data-ttu-id="f9669-114">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="f9669-114">The resource name.</span></span>

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

### <span data-ttu-id="f9669-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9669-115">-ResourceGroupName</span></span>
<span data-ttu-id="f9669-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f9669-116">The resource group name.</span></span>

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

### <span data-ttu-id="f9669-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f9669-117">-Confirm</span></span>
<span data-ttu-id="f9669-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9669-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9669-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9669-119">-WhatIf</span></span>
<span data-ttu-id="f9669-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9669-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9669-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f9669-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9669-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9669-122">CommonParameters</span></span>
<span data-ttu-id="f9669-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9669-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9669-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9669-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9669-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9669-125">INPUTS</span></span>

### <span data-ttu-id="f9669-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f9669-126">System.String</span></span>

## <span data-ttu-id="f9669-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9669-127">OUTPUTS</span></span>

### <span data-ttu-id="f9669-128">Microsoft. Azure. Commands. Network. models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="f9669-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="f9669-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9669-129">NOTES</span></span>

## <span data-ttu-id="f9669-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9669-130">RELATED LINKS</span></span>


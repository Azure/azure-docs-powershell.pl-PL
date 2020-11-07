---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: 63b044c4a9736aca72e9713cd8ec5833e7b056ab
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890638"
---
# <span data-ttu-id="cebb6-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="cebb6-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="cebb6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cebb6-102">SYNOPSIS</span></span>
<span data-ttu-id="cebb6-103">Umożliwia użytkownikom łatwe pobieranie pakietu profilu sieci VPN wygenerowanego przy użyciu New-AzVpnClientConfiguration unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="cebb6-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="cebb6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cebb6-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cebb6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cebb6-105">DESCRIPTION</span></span>
<span data-ttu-id="cebb6-106">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="cebb6-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="cebb6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cebb6-107">EXAMPLES</span></span>

### <span data-ttu-id="cebb6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cebb6-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="cebb6-109">Pobiera adres URL umożliwiający pobranie profilu VpnClient, który został wcześniej wygenerowany przy użyciu polecenia New-AzVpnClientConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cebb6-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="cebb6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cebb6-110">PARAMETERS</span></span>

### <span data-ttu-id="cebb6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cebb6-111">-DefaultProfile</span></span>
<span data-ttu-id="cebb6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cebb6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="cebb6-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cebb6-113">-Name</span></span>
<span data-ttu-id="cebb6-114">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="cebb6-114">The resource name.</span></span>

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

### <span data-ttu-id="cebb6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cebb6-115">-ResourceGroupName</span></span>
<span data-ttu-id="cebb6-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cebb6-116">The resource group name.</span></span>

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

### <span data-ttu-id="cebb6-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cebb6-117">-Confirm</span></span>
<span data-ttu-id="cebb6-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cebb6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cebb6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cebb6-119">-WhatIf</span></span>
<span data-ttu-id="cebb6-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cebb6-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cebb6-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cebb6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cebb6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cebb6-122">CommonParameters</span></span>
<span data-ttu-id="cebb6-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cebb6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cebb6-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cebb6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cebb6-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cebb6-125">INPUTS</span></span>

### <span data-ttu-id="cebb6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="cebb6-126">System.String</span></span>

## <span data-ttu-id="cebb6-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cebb6-127">OUTPUTS</span></span>

### <span data-ttu-id="cebb6-128">Microsoft. Azure. Commands. Network. models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="cebb6-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="cebb6-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cebb6-129">NOTES</span></span>

## <span data-ttu-id="cebb6-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cebb6-130">RELATED LINKS</span></span>


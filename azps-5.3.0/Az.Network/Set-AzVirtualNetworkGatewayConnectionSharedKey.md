---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: a35d659de6019d9d9451289716a7acac7e33a8b7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498654"
---
# <span data-ttu-id="c9df6-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c9df6-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="c9df6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9df6-102">SYNOPSIS</span></span>
<span data-ttu-id="c9df6-103">Konfiguruje klucz udostępniony połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c9df6-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="c9df6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9df6-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9df6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c9df6-105">DESCRIPTION</span></span>
<span data-ttu-id="c9df6-106">Polecenie cmdlet **Set-AzVirtualNetworkGatewayConnectionSharedKey** konfiguruje klucz współużytkowany połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c9df6-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="c9df6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9df6-107">EXAMPLES</span></span>

### <span data-ttu-id="c9df6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c9df6-108">Example 1</span></span>
```powershell
PS C:\Users\alzam> Set-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

## <span data-ttu-id="c9df6-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9df6-109">PARAMETERS</span></span>

### <span data-ttu-id="c9df6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9df6-110">-DefaultProfile</span></span>
<span data-ttu-id="c9df6-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9df6-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9df6-112">-Force</span><span class="sxs-lookup"><span data-stu-id="c9df6-112">-Force</span></span>
<span data-ttu-id="c9df6-113">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c9df6-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9df6-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c9df6-114">-Name</span></span>
<span data-ttu-id="c9df6-115">Określa nazwę klucza udostępnionego bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c9df6-115">Specifies the name of the virtual network gateway shared key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9df6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9df6-116">-ResourceGroupName</span></span>
<span data-ttu-id="c9df6-117">Określa nazwę grupy zasobów, do której należy Brama sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c9df6-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="c9df6-118">-Value</span><span class="sxs-lookup"><span data-stu-id="c9df6-118">-Value</span></span>
<span data-ttu-id="c9df6-119">Określa wartość klucza udostępnionego.</span><span class="sxs-lookup"><span data-stu-id="c9df6-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="c9df6-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9df6-120">-Confirm</span></span>
<span data-ttu-id="c9df6-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9df6-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9df6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9df6-122">-WhatIf</span></span>
<span data-ttu-id="c9df6-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9df6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9df6-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c9df6-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9df6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9df6-125">CommonParameters</span></span>
<span data-ttu-id="c9df6-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9df6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9df6-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9df6-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9df6-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9df6-128">INPUTS</span></span>

### <span data-ttu-id="c9df6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c9df6-129">System.String</span></span>

## <span data-ttu-id="c9df6-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9df6-130">OUTPUTS</span></span>

### <span data-ttu-id="c9df6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c9df6-131">System.String</span></span>

## <span data-ttu-id="c9df6-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9df6-132">NOTES</span></span>

## <span data-ttu-id="c9df6-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9df6-133">RELATED LINKS</span></span>

[<span data-ttu-id="c9df6-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c9df6-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="c9df6-135">Resetowanie — AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c9df6-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

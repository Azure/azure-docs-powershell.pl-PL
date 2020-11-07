---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: f3268d78ac0630e18307646086689cb8d435c290
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717383"
---
# <span data-ttu-id="43ea1-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="43ea1-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="43ea1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43ea1-102">SYNOPSIS</span></span>
<span data-ttu-id="43ea1-103">Konfiguruje klucz udostępniony połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="43ea1-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43ea1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43ea1-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43ea1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="43ea1-105">DESCRIPTION</span></span>
<span data-ttu-id="43ea1-106">Polecenie cmdlet **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** konfiguruje klucz współużytkowany połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="43ea1-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="43ea1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43ea1-107">EXAMPLES</span></span>

### <span data-ttu-id="43ea1-108">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="43ea1-108">Example 1:</span></span>
```
PS C:\Users\alzam> Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

## <span data-ttu-id="43ea1-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43ea1-109">PARAMETERS</span></span>

### <span data-ttu-id="43ea1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43ea1-110">-DefaultProfile</span></span>
<span data-ttu-id="43ea1-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="43ea1-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43ea1-112">-Force</span><span class="sxs-lookup"><span data-stu-id="43ea1-112">-Force</span></span>
<span data-ttu-id="43ea1-113">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="43ea1-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="43ea1-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="43ea1-114">-Name</span></span>
<span data-ttu-id="43ea1-115">Określa nazwę klucza udostępnionego bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="43ea1-115">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="43ea1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43ea1-116">-ResourceGroupName</span></span>
<span data-ttu-id="43ea1-117">Określa nazwę grupy zasobów, do której należy Brama sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="43ea1-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="43ea1-118">-Value</span><span class="sxs-lookup"><span data-stu-id="43ea1-118">-Value</span></span>
<span data-ttu-id="43ea1-119">Określa wartość klucza udostępnionego.</span><span class="sxs-lookup"><span data-stu-id="43ea1-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="43ea1-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="43ea1-120">-Confirm</span></span>
<span data-ttu-id="43ea1-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43ea1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43ea1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43ea1-122">-WhatIf</span></span>
<span data-ttu-id="43ea1-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43ea1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43ea1-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="43ea1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43ea1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ea1-125">CommonParameters</span></span>
<span data-ttu-id="43ea1-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43ea1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43ea1-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43ea1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ea1-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43ea1-128">INPUTS</span></span>

### <span data-ttu-id="43ea1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="43ea1-129">System.String</span></span>

## <span data-ttu-id="43ea1-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43ea1-130">OUTPUTS</span></span>

### <span data-ttu-id="43ea1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="43ea1-131">System.String</span></span>

## <span data-ttu-id="43ea1-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43ea1-132">NOTES</span></span>

## <span data-ttu-id="43ea1-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43ea1-133">RELATED LINKS</span></span>

[<span data-ttu-id="43ea1-134">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="43ea1-134">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="43ea1-135">Resetowanie — AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="43ea1-135">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)



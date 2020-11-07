---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 8c7c1a86b4db7c479367fa83a16888717f1f8079
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708925"
---
# <span data-ttu-id="9e797-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="9e797-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="9e797-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e797-102">SYNOPSIS</span></span>
<span data-ttu-id="9e797-103">Konfiguruje klucz udostępniony połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9e797-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="9e797-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e797-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e797-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9e797-105">DESCRIPTION</span></span>
<span data-ttu-id="9e797-106">Polecenie cmdlet **Set-AzVirtualNetworkGatewayConnectionSharedKey** konfiguruje klucz współużytkowany połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9e797-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="9e797-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e797-107">EXAMPLES</span></span>

### <span data-ttu-id="9e797-108">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="9e797-108">Example 1:</span></span>
```
PS C:\Users\alzam> Set-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

## <span data-ttu-id="9e797-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e797-109">PARAMETERS</span></span>

### <span data-ttu-id="9e797-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e797-110">-DefaultProfile</span></span>
<span data-ttu-id="9e797-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e797-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e797-112">-Force</span><span class="sxs-lookup"><span data-stu-id="9e797-112">-Force</span></span>
<span data-ttu-id="9e797-113">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9e797-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9e797-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9e797-114">-Name</span></span>
<span data-ttu-id="9e797-115">Określa nazwę klucza udostępnionego bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9e797-115">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="9e797-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e797-116">-ResourceGroupName</span></span>
<span data-ttu-id="9e797-117">Określa nazwę grupy zasobów, do której należy Brama sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9e797-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="9e797-118">-Value</span><span class="sxs-lookup"><span data-stu-id="9e797-118">-Value</span></span>
<span data-ttu-id="9e797-119">Określa wartość klucza udostępnionego.</span><span class="sxs-lookup"><span data-stu-id="9e797-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="9e797-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9e797-120">-Confirm</span></span>
<span data-ttu-id="9e797-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e797-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e797-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e797-122">-WhatIf</span></span>
<span data-ttu-id="9e797-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e797-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e797-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9e797-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e797-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e797-125">CommonParameters</span></span>
<span data-ttu-id="9e797-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e797-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e797-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e797-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e797-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e797-128">INPUTS</span></span>

### <span data-ttu-id="9e797-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9e797-129">System.String</span></span>

## <span data-ttu-id="9e797-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e797-130">OUTPUTS</span></span>

### <span data-ttu-id="9e797-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9e797-131">System.String</span></span>

## <span data-ttu-id="9e797-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e797-132">NOTES</span></span>

## <span data-ttu-id="9e797-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e797-133">RELATED LINKS</span></span>

[<span data-ttu-id="9e797-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="9e797-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="9e797-135">Resetowanie — AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="9e797-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)
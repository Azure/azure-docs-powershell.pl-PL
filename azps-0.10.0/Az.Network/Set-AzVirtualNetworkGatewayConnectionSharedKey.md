---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 2683af757bc1b0b58ebb6865a1cfd1edeef580e3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892709"
---
# <span data-ttu-id="1c23c-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="1c23c-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="1c23c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c23c-102">SYNOPSIS</span></span>
<span data-ttu-id="1c23c-103">Konfiguruje klucz udostępniony połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1c23c-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="1c23c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c23c-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c23c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1c23c-105">DESCRIPTION</span></span>
<span data-ttu-id="1c23c-106">Polecenie cmdlet **Set-AzVirtualNetworkGatewayConnectionSharedKey** konfiguruje klucz współużytkowany połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1c23c-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="1c23c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c23c-107">EXAMPLES</span></span>

### <span data-ttu-id="1c23c-108">1:1</span><span class="sxs-lookup"><span data-stu-id="1c23c-108">1:</span></span>
```

```

## <span data-ttu-id="1c23c-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c23c-109">PARAMETERS</span></span>

### <span data-ttu-id="1c23c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c23c-110">-DefaultProfile</span></span>
<span data-ttu-id="1c23c-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c23c-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c23c-112">-Force</span><span class="sxs-lookup"><span data-stu-id="1c23c-112">-Force</span></span>
<span data-ttu-id="1c23c-113">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1c23c-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c23c-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1c23c-114">-Name</span></span>
<span data-ttu-id="1c23c-115">Określa nazwę klucza udostępnionego bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1c23c-115">Specifies the name of the virtual network gateway shared key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c23c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c23c-116">-ResourceGroupName</span></span>
<span data-ttu-id="1c23c-117">Określa nazwę grupy zasobów, do której należy Brama sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1c23c-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="1c23c-118">-Value</span><span class="sxs-lookup"><span data-stu-id="1c23c-118">-Value</span></span>
<span data-ttu-id="1c23c-119">Określa wartość klucza udostępnionego.</span><span class="sxs-lookup"><span data-stu-id="1c23c-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="1c23c-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1c23c-120">-Confirm</span></span>
<span data-ttu-id="1c23c-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c23c-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c23c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c23c-122">-WhatIf</span></span>
<span data-ttu-id="1c23c-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c23c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c23c-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1c23c-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c23c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c23c-125">CommonParameters</span></span>
<span data-ttu-id="1c23c-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c23c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c23c-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c23c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c23c-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c23c-128">INPUTS</span></span>

## <span data-ttu-id="1c23c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c23c-129">OUTPUTS</span></span>

### <span data-ttu-id="1c23c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1c23c-130">System.String</span></span>

## <span data-ttu-id="1c23c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c23c-131">NOTES</span></span>

## <span data-ttu-id="1c23c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c23c-132">RELATED LINKS</span></span>

[<span data-ttu-id="1c23c-133">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="1c23c-133">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="1c23c-134">Resetowanie — AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="1c23c-134">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)



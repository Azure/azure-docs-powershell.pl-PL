---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
ms.openlocfilehash: be59f9ec0728b60314f137dcc5a57c7883935e52
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898881"
---
# <span data-ttu-id="8e1a7-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="8e1a7-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="8e1a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e1a7-102">SYNOPSIS</span></span>
<span data-ttu-id="8e1a7-103">Konfiguruje klucz udostępniony połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8e1a7-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e1a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e1a7-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e1a7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8e1a7-105">DESCRIPTION</span></span>
<span data-ttu-id="8e1a7-106">Polecenie cmdlet **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** konfiguruje klucz współużytkowany połączenia bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8e1a7-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="8e1a7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e1a7-107">EXAMPLES</span></span>

### <span data-ttu-id="8e1a7-108">1:1</span><span class="sxs-lookup"><span data-stu-id="8e1a7-108">1:</span></span>
```

```

## <span data-ttu-id="8e1a7-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e1a7-109">PARAMETERS</span></span>

### <span data-ttu-id="8e1a7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e1a7-110">-DefaultProfile</span></span>
<span data-ttu-id="8e1a7-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e1a7-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e1a7-112">-Force</span><span class="sxs-lookup"><span data-stu-id="8e1a7-112">-Force</span></span>
<span data-ttu-id="8e1a7-113">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8e1a7-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8e1a7-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8e1a7-114">-Name</span></span>
<span data-ttu-id="8e1a7-115">Określa nazwę klucza udostępnionego bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8e1a7-115">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="8e1a7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e1a7-116">-ResourceGroupName</span></span>
<span data-ttu-id="8e1a7-117">Określa nazwę grupy zasobów, do której należy Brama sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8e1a7-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="8e1a7-118">-Value</span><span class="sxs-lookup"><span data-stu-id="8e1a7-118">-Value</span></span>
<span data-ttu-id="8e1a7-119">Określa wartość klucza udostępnionego.</span><span class="sxs-lookup"><span data-stu-id="8e1a7-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="8e1a7-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8e1a7-120">-Confirm</span></span>
<span data-ttu-id="8e1a7-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e1a7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e1a7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e1a7-122">-WhatIf</span></span>
<span data-ttu-id="8e1a7-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e1a7-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e1a7-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8e1a7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e1a7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e1a7-125">CommonParameters</span></span>
<span data-ttu-id="8e1a7-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e1a7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e1a7-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e1a7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e1a7-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e1a7-128">INPUTS</span></span>

## <span data-ttu-id="8e1a7-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e1a7-129">OUTPUTS</span></span>

### <span data-ttu-id="8e1a7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8e1a7-130">System.String</span></span>

## <span data-ttu-id="8e1a7-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e1a7-131">NOTES</span></span>

## <span data-ttu-id="8e1a7-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e1a7-132">RELATED LINKS</span></span>

[<span data-ttu-id="8e1a7-133">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="8e1a7-133">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="8e1a7-134">Resetowanie — AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="8e1a7-134">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)



---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
ms.openlocfilehash: 160fb1b7455a2440773978ec80741922248a8af4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899218"
---
# <span data-ttu-id="f3fe6-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f3fe6-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="f3fe6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3fe6-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3fe6-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3fe6-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3fe6-104">Opis</span><span class="sxs-lookup"><span data-stu-id="f3fe6-104">DESCRIPTION</span></span>

## <span data-ttu-id="f3fe6-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3fe6-105">EXAMPLES</span></span>

### <span data-ttu-id="f3fe6-106">1:1</span><span class="sxs-lookup"><span data-stu-id="f3fe6-106">1:</span></span>
```

```

## <span data-ttu-id="f3fe6-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3fe6-107">PARAMETERS</span></span>

### <span data-ttu-id="f3fe6-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3fe6-108">-DefaultProfile</span></span>
<span data-ttu-id="f3fe6-109">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3fe6-110">-Force</span><span class="sxs-lookup"><span data-stu-id="f3fe6-110">-Force</span></span>
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

### <span data-ttu-id="f3fe6-111">-Length</span><span class="sxs-lookup"><span data-stu-id="f3fe6-111">-KeyLength</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3fe6-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f3fe6-112">-Name</span></span>
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

### <span data-ttu-id="f3fe6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3fe6-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="f3fe6-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f3fe6-114">-Confirm</span></span>
<span data-ttu-id="f3fe6-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3fe6-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3fe6-116">-WhatIf</span></span>
<span data-ttu-id="f3fe6-117">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3fe6-118">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3fe6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3fe6-119">CommonParameters</span></span>
<span data-ttu-id="f3fe6-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3fe6-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3fe6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3fe6-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3fe6-122">INPUTS</span></span>

## <span data-ttu-id="f3fe6-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3fe6-123">OUTPUTS</span></span>

### <span data-ttu-id="f3fe6-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f3fe6-124">System.String</span></span>

## <span data-ttu-id="f3fe6-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3fe6-125">NOTES</span></span>

## <span data-ttu-id="f3fe6-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3fe6-126">RELATED LINKS</span></span>

[<span data-ttu-id="f3fe6-127">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f3fe6-127">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="f3fe6-128">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="f3fe6-128">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)



---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: a805145445f8bd17ac60497e2c7d7e89ea56a3c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553653"
---
# <span data-ttu-id="bfa5a-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="bfa5a-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="bfa5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bfa5a-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfa5a-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bfa5a-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bfa5a-104">Opis</span><span class="sxs-lookup"><span data-stu-id="bfa5a-104">DESCRIPTION</span></span>

## <span data-ttu-id="bfa5a-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bfa5a-105">EXAMPLES</span></span>

## <span data-ttu-id="bfa5a-106">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bfa5a-106">PARAMETERS</span></span>

### <span data-ttu-id="bfa5a-107">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfa5a-107">-DefaultProfile</span></span>
<span data-ttu-id="bfa5a-108">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-108">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfa5a-109">-Force</span><span class="sxs-lookup"><span data-stu-id="bfa5a-109">-Force</span></span>
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

### <span data-ttu-id="bfa5a-110">-Length</span><span class="sxs-lookup"><span data-stu-id="bfa5a-110">-KeyLength</span></span>
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

### <span data-ttu-id="bfa5a-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bfa5a-111">-Name</span></span>
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

### <span data-ttu-id="bfa5a-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfa5a-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="bfa5a-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bfa5a-113">-Confirm</span></span>
<span data-ttu-id="bfa5a-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfa5a-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfa5a-115">-WhatIf</span></span>
<span data-ttu-id="bfa5a-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfa5a-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfa5a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfa5a-118">CommonParameters</span></span>
<span data-ttu-id="bfa5a-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfa5a-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfa5a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfa5a-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfa5a-121">INPUTS</span></span>

### <span data-ttu-id="bfa5a-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bfa5a-122">None</span></span>
<span data-ttu-id="bfa5a-123">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bfa5a-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bfa5a-124">OUTPUTS</span></span>

### <span data-ttu-id="bfa5a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="bfa5a-125">System.String</span></span>

## <span data-ttu-id="bfa5a-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bfa5a-126">NOTES</span></span>

## <span data-ttu-id="bfa5a-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bfa5a-127">RELATED LINKS</span></span>

[<span data-ttu-id="bfa5a-128">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="bfa5a-128">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="bfa5a-129">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="bfa5a-129">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)



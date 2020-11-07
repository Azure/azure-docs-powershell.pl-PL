---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 3519fd616be92e2404ef7b4d51241b675240470c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892886"
---
# <span data-ttu-id="a60da-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="a60da-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="a60da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a60da-102">SYNOPSIS</span></span>

## <span data-ttu-id="a60da-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a60da-103">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a60da-104">Opis</span><span class="sxs-lookup"><span data-stu-id="a60da-104">DESCRIPTION</span></span>

## <span data-ttu-id="a60da-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a60da-105">EXAMPLES</span></span>

### <span data-ttu-id="a60da-106">1:1</span><span class="sxs-lookup"><span data-stu-id="a60da-106">1:</span></span>
```

```

## <span data-ttu-id="a60da-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a60da-107">PARAMETERS</span></span>

### <span data-ttu-id="a60da-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a60da-108">-DefaultProfile</span></span>
<span data-ttu-id="a60da-109">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a60da-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a60da-110">-Force</span><span class="sxs-lookup"><span data-stu-id="a60da-110">-Force</span></span>
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

### <span data-ttu-id="a60da-111">-Length</span><span class="sxs-lookup"><span data-stu-id="a60da-111">-KeyLength</span></span>
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

### <span data-ttu-id="a60da-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a60da-112">-Name</span></span>
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

### <span data-ttu-id="a60da-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a60da-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="a60da-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a60da-114">-Confirm</span></span>
<span data-ttu-id="a60da-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a60da-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a60da-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a60da-116">-WhatIf</span></span>
<span data-ttu-id="a60da-117">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a60da-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a60da-118">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a60da-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a60da-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a60da-119">CommonParameters</span></span>
<span data-ttu-id="a60da-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a60da-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a60da-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a60da-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a60da-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a60da-122">INPUTS</span></span>

## <span data-ttu-id="a60da-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a60da-123">OUTPUTS</span></span>

### <span data-ttu-id="a60da-124">System. String</span><span class="sxs-lookup"><span data-stu-id="a60da-124">System.String</span></span>

## <span data-ttu-id="a60da-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a60da-125">NOTES</span></span>

## <span data-ttu-id="a60da-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a60da-126">RELATED LINKS</span></span>

[<span data-ttu-id="a60da-127">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="a60da-127">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="a60da-128">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="a60da-128">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)



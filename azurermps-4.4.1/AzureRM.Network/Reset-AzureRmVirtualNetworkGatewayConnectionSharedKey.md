---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 65540c331074b5c140bafe9e87d625dfaec2f252
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554337"
---
# <span data-ttu-id="d7380-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="d7380-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="d7380-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7380-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7380-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7380-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7380-104">Opis</span><span class="sxs-lookup"><span data-stu-id="d7380-104">DESCRIPTION</span></span>

## <span data-ttu-id="d7380-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7380-105">EXAMPLES</span></span>

## <span data-ttu-id="d7380-106">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7380-106">PARAMETERS</span></span>

### <span data-ttu-id="d7380-107">-Force</span><span class="sxs-lookup"><span data-stu-id="d7380-107">-Force</span></span>
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

### <span data-ttu-id="d7380-108">-Length</span><span class="sxs-lookup"><span data-stu-id="d7380-108">-KeyLength</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7380-109">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d7380-109">-Name</span></span>
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

### <span data-ttu-id="d7380-110">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7380-110">-ResourceGroupName</span></span>
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

### <span data-ttu-id="d7380-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7380-111">-Confirm</span></span>
<span data-ttu-id="d7380-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7380-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7380-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7380-113">-WhatIf</span></span>
<span data-ttu-id="d7380-114">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7380-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7380-115">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d7380-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7380-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7380-116">-DefaultProfile</span></span>
<span data-ttu-id="d7380-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7380-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7380-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7380-118">CommonParameters</span></span>
<span data-ttu-id="d7380-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7380-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7380-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7380-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7380-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7380-121">INPUTS</span></span>

## <span data-ttu-id="d7380-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7380-122">OUTPUTS</span></span>

### <span data-ttu-id="d7380-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d7380-123">System.String</span></span>

## <span data-ttu-id="d7380-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7380-124">NOTES</span></span>

## <span data-ttu-id="d7380-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7380-125">RELATED LINKS</span></span>

[<span data-ttu-id="d7380-126">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="d7380-126">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="d7380-127">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="d7380-127">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)



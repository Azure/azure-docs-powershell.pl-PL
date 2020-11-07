---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 872683cbf4e26601ec16f05256f0011b0441127c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717709"
---
# <span data-ttu-id="90bb7-101">Remove-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="90bb7-101">Remove-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="90bb7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90bb7-102">SYNOPSIS</span></span>
<span data-ttu-id="90bb7-103">Usuwa HybridConnection z określonej przestrzeni nazw HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="90bb7-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90bb7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90bb7-104">SYNTAX</span></span>

```
Remove-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90bb7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="90bb7-105">DESCRIPTION</span></span>
<span data-ttu-id="90bb7-106">Polecenie cmdlet **Remove-AzureRmRelayHybridConnection** usuwa HybridConnection z określonego obszaru nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="90bb7-106">The **Remove-AzureRmRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="90bb7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90bb7-107">EXAMPLES</span></span>

### <span data-ttu-id="90bb7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="90bb7-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="90bb7-109">Usuwa HybridConnection `TestHybridConnection` z obszaru nazw `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="90bb7-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="90bb7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90bb7-110">PARAMETERS</span></span>

### <span data-ttu-id="90bb7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90bb7-111">-DefaultProfile</span></span>
<span data-ttu-id="90bb7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="90bb7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90bb7-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="90bb7-113">-Name</span></span>
<span data-ttu-id="90bb7-114">Nazwa HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="90bb7-114">HybridConnections Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90bb7-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="90bb7-115">-Namespace</span></span>
<span data-ttu-id="90bb7-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="90bb7-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90bb7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90bb7-117">-ResourceGroupName</span></span>
<span data-ttu-id="90bb7-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="90bb7-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90bb7-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="90bb7-119">-Confirm</span></span>
<span data-ttu-id="90bb7-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90bb7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90bb7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90bb7-121">-WhatIf</span></span>
<span data-ttu-id="90bb7-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90bb7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90bb7-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="90bb7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90bb7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90bb7-124">CommonParameters</span></span>
<span data-ttu-id="90bb7-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90bb7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90bb7-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90bb7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90bb7-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90bb7-127">INPUTS</span></span>

### <span data-ttu-id="90bb7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90bb7-128">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="90bb7-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="90bb7-129">-Namespace</span></span>
    System.String

### <span data-ttu-id="90bb7-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="90bb7-130">-Name</span></span>
    System.String

## <span data-ttu-id="90bb7-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90bb7-131">OUTPUTS</span></span>

### <span data-ttu-id="90bb7-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="90bb7-132">System.Object</span></span>

## <span data-ttu-id="90bb7-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90bb7-133">NOTES</span></span>

## <span data-ttu-id="90bb7-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90bb7-134">RELATED LINKS</span></span>


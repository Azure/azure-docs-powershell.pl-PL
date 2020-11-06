---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 746033cfdf48782d10c0fdabf7a018d309269afb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524286"
---
# <span data-ttu-id="1ba5c-101">Remove-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="1ba5c-101">Remove-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="1ba5c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ba5c-102">SYNOPSIS</span></span>
<span data-ttu-id="1ba5c-103">Usuwa HybridConnection z określonej przestrzeni nazw HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="1ba5c-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ba5c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ba5c-104">SYNTAX</span></span>

```
Remove-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ba5c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ba5c-105">DESCRIPTION</span></span>
<span data-ttu-id="1ba5c-106">Polecenie cmdlet **Remove-AzureRmRelayHybridConnection** usuwa HybridConnection z określonego obszaru nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="1ba5c-106">The **Remove-AzureRmRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="1ba5c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ba5c-107">EXAMPLES</span></span>

### <span data-ttu-id="1ba5c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1ba5c-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="1ba5c-109">Usuwa HybridConnection `TestHybridConnection` z obszaru nazw `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="1ba5c-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="1ba5c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ba5c-110">PARAMETERS</span></span>

### <span data-ttu-id="1ba5c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ba5c-111">-DefaultProfile</span></span>
<span data-ttu-id="1ba5c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ba5c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ba5c-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1ba5c-113">-Name</span></span>
<span data-ttu-id="1ba5c-114">Nazwa HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="1ba5c-114">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba5c-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1ba5c-115">-Namespace</span></span>
<span data-ttu-id="1ba5c-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="1ba5c-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba5c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ba5c-117">-ResourceGroupName</span></span>
<span data-ttu-id="1ba5c-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1ba5c-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba5c-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1ba5c-119">-Confirm</span></span>
<span data-ttu-id="1ba5c-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ba5c-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba5c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ba5c-121">-WhatIf</span></span>
<span data-ttu-id="1ba5c-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ba5c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ba5c-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1ba5c-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba5c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ba5c-124">CommonParameters</span></span>
<span data-ttu-id="1ba5c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ba5c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1ba5c-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ba5c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ba5c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ba5c-127">INPUTS</span></span>

### <span data-ttu-id="1ba5c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1ba5c-128">System.String</span></span>


## <span data-ttu-id="1ba5c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ba5c-129">OUTPUTS</span></span>

### <span data-ttu-id="1ba5c-130">System. void</span><span class="sxs-lookup"><span data-stu-id="1ba5c-130">System.Void</span></span>


## <span data-ttu-id="1ba5c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ba5c-131">NOTES</span></span>

## <span data-ttu-id="1ba5c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ba5c-132">RELATED LINKS</span></span>

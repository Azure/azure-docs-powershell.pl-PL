---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
ms.openlocfilehash: da563f063fb22ffd5c21dfc3d330a59a122c9a84
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222974"
---
# <span data-ttu-id="cb161-101">Remove-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="cb161-101">Remove-AzRelayHybridConnection</span></span>

## <span data-ttu-id="cb161-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cb161-102">SYNOPSIS</span></span>
<span data-ttu-id="cb161-103">Usuwa HybridConnection z określonej przestrzeni nazw HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="cb161-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

## <span data-ttu-id="cb161-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cb161-104">SYNTAX</span></span>

```
Remove-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb161-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cb161-105">DESCRIPTION</span></span>
<span data-ttu-id="cb161-106">Polecenie cmdlet **Remove-AzRelayHybridConnection** usuwa HybridConnection z określonego obszaru nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="cb161-106">The **Remove-AzRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="cb161-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cb161-107">EXAMPLES</span></span>

### <span data-ttu-id="cb161-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cb161-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="cb161-109">Usuwa HybridConnection `TestHybridConnection` z obszaru nazw `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="cb161-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="cb161-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cb161-110">PARAMETERS</span></span>

### <span data-ttu-id="cb161-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb161-111">-DefaultProfile</span></span>
<span data-ttu-id="cb161-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cb161-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb161-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cb161-113">-Name</span></span>
<span data-ttu-id="cb161-114">Nazwa HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="cb161-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="cb161-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cb161-115">-Namespace</span></span>
<span data-ttu-id="cb161-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="cb161-116">Namespace Name.</span></span>

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

### <span data-ttu-id="cb161-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb161-117">-ResourceGroupName</span></span>
<span data-ttu-id="cb161-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cb161-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="cb161-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cb161-119">-Confirm</span></span>
<span data-ttu-id="cb161-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb161-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb161-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb161-121">-WhatIf</span></span>
<span data-ttu-id="cb161-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb161-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb161-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cb161-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb161-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb161-124">CommonParameters</span></span>
<span data-ttu-id="cb161-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb161-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb161-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb161-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb161-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb161-127">INPUTS</span></span>

### <span data-ttu-id="cb161-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cb161-128">System.String</span></span>

## <span data-ttu-id="cb161-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cb161-129">OUTPUTS</span></span>

### <span data-ttu-id="cb161-130">System. void</span><span class="sxs-lookup"><span data-stu-id="cb161-130">System.Void</span></span>

## <span data-ttu-id="cb161-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cb161-131">NOTES</span></span>

## <span data-ttu-id="cb161-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb161-132">RELATED LINKS</span></span>

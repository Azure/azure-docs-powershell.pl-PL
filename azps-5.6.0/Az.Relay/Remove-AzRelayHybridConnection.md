---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/remove-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
ms.openlocfilehash: b426eda2ab7e9714cd46a95c25d248adef5464a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000465"
---
# <span data-ttu-id="2a355-101">Remove-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="2a355-101">Remove-AzRelayHybridConnection</span></span>

## <span data-ttu-id="2a355-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a355-102">SYNOPSIS</span></span>
<span data-ttu-id="2a355-103">Usuwa połączenie hybrydowe z określonej przestrzeni nazw usługi HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="2a355-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

## <span data-ttu-id="2a355-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2a355-104">SYNTAX</span></span>

```
Remove-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a355-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2a355-105">DESCRIPTION</span></span>
<span data-ttu-id="2a355-106">Polecenie **cmdlet Remove-AzRelayHybridConnection** usuwa połączenie hybrydowe z określonej przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="2a355-106">The **Remove-AzRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="2a355-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2a355-107">EXAMPLES</span></span>

### <span data-ttu-id="2a355-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2a355-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="2a355-109">Usuwa połączenie hybrydowe z `TestHybridConnection` przestrzeni `TestNameSpace-Relay1` nazw.</span><span class="sxs-lookup"><span data-stu-id="2a355-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="2a355-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a355-110">PARAMETERS</span></span>

### <span data-ttu-id="2a355-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a355-111">-DefaultProfile</span></span>
<span data-ttu-id="2a355-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a355-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a355-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2a355-113">-Name</span></span>
<span data-ttu-id="2a355-114">Nazwa usługi HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="2a355-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="2a355-115">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="2a355-115">-Namespace</span></span>
<span data-ttu-id="2a355-116">Nazwa przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="2a355-116">Namespace Name.</span></span>

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

### <span data-ttu-id="2a355-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a355-117">-ResourceGroupName</span></span>
<span data-ttu-id="2a355-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2a355-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="2a355-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a355-119">-Confirm</span></span>
<span data-ttu-id="2a355-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2a355-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a355-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a355-121">-WhatIf</span></span>
<span data-ttu-id="2a355-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a355-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a355-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2a355-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a355-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a355-124">CommonParameters</span></span>
<span data-ttu-id="2a355-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a355-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a355-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a355-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a355-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a355-127">INPUTS</span></span>

### <span data-ttu-id="2a355-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2a355-128">System.String</span></span>

## <span data-ttu-id="2a355-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a355-129">OUTPUTS</span></span>

### <span data-ttu-id="2a355-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="2a355-130">System.Void</span></span>

## <span data-ttu-id="2a355-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2a355-131">NOTES</span></span>

## <span data-ttu-id="2a355-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a355-132">RELATED LINKS</span></span>

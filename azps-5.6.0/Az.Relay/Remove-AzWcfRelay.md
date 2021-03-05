---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: f99a3a999baad580e04c6872f047c02d4a99091f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000433"
---
# <span data-ttu-id="e4b35-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="e4b35-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="e4b35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4b35-102">SYNOPSIS</span></span>
<span data-ttu-id="e4b35-103">Usuwa plik WcfRelay z określonej przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="e4b35-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="e4b35-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e4b35-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4b35-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e4b35-105">DESCRIPTION</span></span>
<span data-ttu-id="e4b35-106">Polecenie **cmdlet Remove-AzWcfRelay** usuwa plik WcfRelay z określonej przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="e4b35-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="e4b35-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e4b35-107">EXAMPLES</span></span>

### <span data-ttu-id="e4b35-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e4b35-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="e4b35-109">Usuwa wcfRelay `TestWCFRelay1` z przestrzeni `TestNameSpace-Relay1` nazw.</span><span class="sxs-lookup"><span data-stu-id="e4b35-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="e4b35-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4b35-110">PARAMETERS</span></span>

### <span data-ttu-id="e4b35-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4b35-111">-DefaultProfile</span></span>
<span data-ttu-id="e4b35-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4b35-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4b35-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e4b35-113">-Name</span></span>
<span data-ttu-id="e4b35-114">Nazwa aplikacji WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="e4b35-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="e4b35-115">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="e4b35-115">-Namespace</span></span>
<span data-ttu-id="e4b35-116">Nazwa przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="e4b35-116">Namespace Name.</span></span>

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

### <span data-ttu-id="e4b35-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4b35-117">-ResourceGroupName</span></span>
<span data-ttu-id="e4b35-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e4b35-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="e4b35-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4b35-119">-Confirm</span></span>
<span data-ttu-id="e4b35-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e4b35-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4b35-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4b35-121">-WhatIf</span></span>
<span data-ttu-id="e4b35-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4b35-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4b35-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e4b35-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4b35-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4b35-124">CommonParameters</span></span>
<span data-ttu-id="e4b35-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4b35-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4b35-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4b35-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4b35-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4b35-127">INPUTS</span></span>

### <span data-ttu-id="e4b35-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e4b35-128">System.String</span></span>

## <span data-ttu-id="e4b35-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4b35-129">OUTPUTS</span></span>

### <span data-ttu-id="e4b35-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="e4b35-130">System.Void</span></span>

## <span data-ttu-id="e4b35-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e4b35-131">NOTES</span></span>

## <span data-ttu-id="e4b35-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4b35-132">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: 238c4ecf92cbdd1dc6e9e0a430ec8e6ad200b967
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201946"
---
# <span data-ttu-id="37aa5-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="37aa5-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="37aa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37aa5-102">SYNOPSIS</span></span>
<span data-ttu-id="37aa5-103">Usuwa plik WcfRelay z określonej przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="37aa5-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="37aa5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="37aa5-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37aa5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="37aa5-105">DESCRIPTION</span></span>
<span data-ttu-id="37aa5-106">Polecenie **cmdlet Remove-AzWcfRelay** usuwa plik WcfRelay z określonej przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="37aa5-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="37aa5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="37aa5-107">EXAMPLES</span></span>

### <span data-ttu-id="37aa5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="37aa5-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="37aa5-109">Usuwa wcfRelay `TestWCFRelay1` z przestrzeni `TestNameSpace-Relay1` nazw.</span><span class="sxs-lookup"><span data-stu-id="37aa5-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="37aa5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37aa5-110">PARAMETERS</span></span>

### <span data-ttu-id="37aa5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37aa5-111">-DefaultProfile</span></span>
<span data-ttu-id="37aa5-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="37aa5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37aa5-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="37aa5-113">-Name</span></span>
<span data-ttu-id="37aa5-114">Nazwa aplikacji WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="37aa5-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="37aa5-115">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="37aa5-115">-Namespace</span></span>
<span data-ttu-id="37aa5-116">Nazwa przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="37aa5-116">Namespace Name.</span></span>

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

### <span data-ttu-id="37aa5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37aa5-117">-ResourceGroupName</span></span>
<span data-ttu-id="37aa5-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="37aa5-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="37aa5-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="37aa5-119">-Confirm</span></span>
<span data-ttu-id="37aa5-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="37aa5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37aa5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37aa5-121">-WhatIf</span></span>
<span data-ttu-id="37aa5-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37aa5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37aa5-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="37aa5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37aa5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37aa5-124">CommonParameters</span></span>
<span data-ttu-id="37aa5-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37aa5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37aa5-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37aa5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37aa5-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37aa5-127">INPUTS</span></span>

### <span data-ttu-id="37aa5-128">System.String</span><span class="sxs-lookup"><span data-stu-id="37aa5-128">System.String</span></span>

## <span data-ttu-id="37aa5-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="37aa5-129">OUTPUTS</span></span>

### <span data-ttu-id="37aa5-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="37aa5-130">System.Void</span></span>

## <span data-ttu-id="37aa5-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="37aa5-131">NOTES</span></span>

## <span data-ttu-id="37aa5-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37aa5-132">RELATED LINKS</span></span>

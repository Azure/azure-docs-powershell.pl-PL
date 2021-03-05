---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: 17a5cb5c05b9bd3293b15ef48b90c8d7387744da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000458"
---
# <span data-ttu-id="a6bda-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="a6bda-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="a6bda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6bda-102">SYNOPSIS</span></span>
<span data-ttu-id="a6bda-103">Usuwa przestrzeń nazw z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a6bda-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="a6bda-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a6bda-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6bda-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a6bda-105">DESCRIPTION</span></span>
<span data-ttu-id="a6bda-106">Polecenie **cmdlet Remove-AzRelayNamespace** usuwa przestrzeń nazw z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a6bda-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="a6bda-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a6bda-107">EXAMPLES</span></span>

### <span data-ttu-id="a6bda-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a6bda-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="a6bda-109">Usuwa przestrzeń nazw Przekazywanie `TestNameSpace-Relay1` z określonej grupy `Default-ServiceBus-WestUS` zasobów.</span><span class="sxs-lookup"><span data-stu-id="a6bda-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="a6bda-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6bda-110">PARAMETERS</span></span>

### <span data-ttu-id="a6bda-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6bda-111">-DefaultProfile</span></span>
<span data-ttu-id="a6bda-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6bda-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6bda-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a6bda-113">-Name</span></span>
<span data-ttu-id="a6bda-114">Nazwa przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="a6bda-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="a6bda-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6bda-115">-ResourceGroupName</span></span>
<span data-ttu-id="a6bda-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a6bda-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="a6bda-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a6bda-117">-Confirm</span></span>
<span data-ttu-id="a6bda-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a6bda-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6bda-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6bda-119">-WhatIf</span></span>
<span data-ttu-id="a6bda-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6bda-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6bda-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a6bda-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6bda-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6bda-122">CommonParameters</span></span>
<span data-ttu-id="a6bda-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6bda-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6bda-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6bda-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6bda-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6bda-125">INPUTS</span></span>

### <span data-ttu-id="a6bda-126">System.String</span><span class="sxs-lookup"><span data-stu-id="a6bda-126">System.String</span></span>

## <span data-ttu-id="a6bda-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6bda-127">OUTPUTS</span></span>

### <span data-ttu-id="a6bda-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="a6bda-128">System.Void</span></span>

## <span data-ttu-id="a6bda-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a6bda-129">NOTES</span></span>

## <span data-ttu-id="a6bda-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6bda-130">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
ms.openlocfilehash: 30d13f9a5f9338a33f8ec6f6aaba9b40e028f087
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967658"
---
# <span data-ttu-id="df206-101">Remove-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="df206-101">Remove-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="df206-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df206-102">SYNOPSIS</span></span>
<span data-ttu-id="df206-103">Usuwa subskrypcję z grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="df206-103">Removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="df206-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="df206-104">SYNTAX</span></span>

```
Remove-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df206-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="df206-105">DESCRIPTION</span></span>
<span data-ttu-id="df206-106">Polecenie **cmdlet Remove-AzManagementGroupSubscription** usuwa subskrypcję z grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="df206-106">The **Remove-AzManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="df206-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="df206-107">EXAMPLES</span></span>

### <span data-ttu-id="df206-108">Przykład 1. Usuwanie subskrypcji z grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="df206-108">Example 1: Remove Subscription from a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="df206-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df206-109">PARAMETERS</span></span>

### <span data-ttu-id="df206-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df206-110">-DefaultProfile</span></span>
<span data-ttu-id="df206-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="df206-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df206-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="df206-112">-GroupName</span></span>
<span data-ttu-id="df206-113">Identyfikator grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="df206-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df206-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df206-114">-PassThru</span></span>
<span data-ttu-id="df206-115">Powrót `true` do pomyślnego wykonania</span><span class="sxs-lookup"><span data-stu-id="df206-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="df206-116">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="df206-116">-SubscriptionId</span></span>
<span data-ttu-id="df206-117">Identyfikator subskrypcji skojarzonej z zarządzaniem</span><span class="sxs-lookup"><span data-stu-id="df206-117">Subscription Id of the subscription associated with the management</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df206-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="df206-118">-Confirm</span></span>
<span data-ttu-id="df206-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="df206-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df206-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df206-120">-WhatIf</span></span>
<span data-ttu-id="df206-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df206-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df206-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="df206-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df206-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df206-123">CommonParameters</span></span>
<span data-ttu-id="df206-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df206-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df206-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df206-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df206-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df206-126">INPUTS</span></span>

### <span data-ttu-id="df206-127">Brak</span><span class="sxs-lookup"><span data-stu-id="df206-127">None</span></span>

## <span data-ttu-id="df206-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df206-128">OUTPUTS</span></span>

### <span data-ttu-id="df206-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="df206-129">System.Boolean</span></span>

## <span data-ttu-id="df206-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="df206-130">NOTES</span></span>

## <span data-ttu-id="df206-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df206-131">RELATED LINKS</span></span>

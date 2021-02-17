---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
ms.openlocfilehash: 39325462d9c2cfb9c06296ff98e5595d2c2c2c06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183667"
---
# <span data-ttu-id="f31d8-101">New-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="f31d8-101">New-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="f31d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f31d8-102">SYNOPSIS</span></span>
<span data-ttu-id="f31d8-103">Dodaje subskrypcję do grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="f31d8-103">Adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="f31d8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f31d8-104">SYNTAX</span></span>

```
New-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f31d8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f31d8-105">DESCRIPTION</span></span>
<span data-ttu-id="f31d8-106">Polecenie **cmdlet New-AzManagementGroupSubscription** dodaje subskrypcję do grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="f31d8-106">The **New-AzManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="f31d8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f31d8-107">EXAMPLES</span></span>

### <span data-ttu-id="f31d8-108">Przykład 1. Dodawanie subskrypcji do grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="f31d8-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="f31d8-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f31d8-109">PARAMETERS</span></span>

### <span data-ttu-id="f31d8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f31d8-110">-DefaultProfile</span></span>
<span data-ttu-id="f31d8-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f31d8-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f31d8-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="f31d8-112">-GroupName</span></span>
<span data-ttu-id="f31d8-113">Identyfikator grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="f31d8-113">Management Group Id</span></span>

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

### <span data-ttu-id="f31d8-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f31d8-114">-PassThru</span></span>
<span data-ttu-id="f31d8-115">Powrót `true` do pomyślnego wykonania</span><span class="sxs-lookup"><span data-stu-id="f31d8-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="f31d8-116">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f31d8-116">-SubscriptionId</span></span>
<span data-ttu-id="f31d8-117">Identyfikator subskrypcji skojarzonej z zarządzaniem</span><span class="sxs-lookup"><span data-stu-id="f31d8-117">Subscription Id of the subscription associated with the management</span></span>

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

### <span data-ttu-id="f31d8-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f31d8-118">-Confirm</span></span>
<span data-ttu-id="f31d8-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f31d8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f31d8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f31d8-120">-WhatIf</span></span>
<span data-ttu-id="f31d8-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f31d8-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f31d8-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f31d8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f31d8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f31d8-123">CommonParameters</span></span>
<span data-ttu-id="f31d8-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f31d8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f31d8-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f31d8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f31d8-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f31d8-126">INPUTS</span></span>

### <span data-ttu-id="f31d8-127">Brak</span><span class="sxs-lookup"><span data-stu-id="f31d8-127">None</span></span>

## <span data-ttu-id="f31d8-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f31d8-128">OUTPUTS</span></span>

### <span data-ttu-id="f31d8-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f31d8-129">System.Boolean</span></span>

## <span data-ttu-id="f31d8-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f31d8-130">NOTES</span></span>

## <span data-ttu-id="f31d8-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f31d8-131">RELATED LINKS</span></span>

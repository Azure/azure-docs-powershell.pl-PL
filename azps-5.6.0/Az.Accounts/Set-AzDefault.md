---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/set-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
ms.openlocfilehash: 98e7877ba075aacc1da00291bb557c2e94e276e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010097"
---
# <span data-ttu-id="8bb08-101">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="8bb08-101">Set-AzDefault</span></span>

## <span data-ttu-id="8bb08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bb08-102">SYNOPSIS</span></span>
<span data-ttu-id="8bb08-103">Ustawia wartość domyślną w bieżącym kontekście</span><span class="sxs-lookup"><span data-stu-id="8bb08-103">Sets a default in the current context</span></span>

## <span data-ttu-id="8bb08-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8bb08-104">SYNTAX</span></span>

```
Set-AzDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bb08-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8bb08-105">DESCRIPTION</span></span>
<span data-ttu-id="8bb08-106">Polecenie Set-AzDefault cmdlet dodaje lub zmienia wartości domyślne w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="8bb08-106">The Set-AzDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="8bb08-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8bb08-107">EXAMPLES</span></span>

### <span data-ttu-id="8bb08-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8bb08-108">Example 1</span></span>
```
PS C:\> Set-AzDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="8bb08-109">To polecenie ustawia domyślną grupę zasobów na grupę zasobów określoną przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8bb08-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="8bb08-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bb08-110">PARAMETERS</span></span>

### <span data-ttu-id="8bb08-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bb08-111">-DefaultProfile</span></span>
<span data-ttu-id="8bb08-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8bb08-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bb08-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="8bb08-113">-Force</span></span>
<span data-ttu-id="8bb08-114">Tworzenie nowej grupy zasobów, jeśli określone ustawienie domyślne nie istnieje</span><span class="sxs-lookup"><span data-stu-id="8bb08-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="8bb08-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bb08-115">-ResourceGroupName</span></span>
<span data-ttu-id="8bb08-116">Nazwa grupy zasobów ustawiana jako domyślna</span><span class="sxs-lookup"><span data-stu-id="8bb08-116">Name of the resource group being set as default</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb08-117">— Zakres</span><span class="sxs-lookup"><span data-stu-id="8bb08-117">-Scope</span></span>
<span data-ttu-id="8bb08-118">Określa zakres zmian kontekstu, na przykład tego, czy zmiany mają zastosowanie tylko do bieżącego procesu, czy do wszystkich sesji rozpoczętych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8bb08-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bb08-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8bb08-119">-Confirm</span></span>
<span data-ttu-id="8bb08-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8bb08-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bb08-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bb08-121">-WhatIf</span></span>
<span data-ttu-id="8bb08-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bb08-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bb08-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8bb08-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bb08-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bb08-124">CommonParameters</span></span>
<span data-ttu-id="8bb08-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bb08-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bb08-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8bb08-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bb08-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bb08-127">INPUTS</span></span>

### <span data-ttu-id="8bb08-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8bb08-128">System.String</span></span>

## <span data-ttu-id="8bb08-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bb08-129">OUTPUTS</span></span>

### <span data-ttu-id="8bb08-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8bb08-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="8bb08-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8bb08-131">NOTES</span></span>

## <span data-ttu-id="8bb08-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8bb08-132">RELATED LINKS</span></span>

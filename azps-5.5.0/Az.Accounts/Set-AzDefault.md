---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
ms.openlocfilehash: 25fd0e1cd651f70fa0900c528f9e5297a8eaf2df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176522"
---
# <span data-ttu-id="f7b65-101">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="f7b65-101">Set-AzDefault</span></span>

## <span data-ttu-id="f7b65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7b65-102">SYNOPSIS</span></span>
<span data-ttu-id="f7b65-103">Ustawia wartość domyślną w bieżącym kontekście</span><span class="sxs-lookup"><span data-stu-id="f7b65-103">Sets a default in the current context</span></span>

## <span data-ttu-id="f7b65-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f7b65-104">SYNTAX</span></span>

```
Set-AzDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7b65-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f7b65-105">DESCRIPTION</span></span>
<span data-ttu-id="f7b65-106">Polecenie Set-AzDefault cmdlet dodaje lub zmienia wartości domyślne w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="f7b65-106">The Set-AzDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="f7b65-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f7b65-107">EXAMPLES</span></span>

### <span data-ttu-id="f7b65-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f7b65-108">Example 1</span></span>
```
PS C:\> Set-AzDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="f7b65-109">To polecenie ustawia domyślną grupę zasobów na grupę zasobów określoną przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f7b65-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="f7b65-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7b65-110">PARAMETERS</span></span>

### <span data-ttu-id="f7b65-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7b65-111">-DefaultProfile</span></span>
<span data-ttu-id="f7b65-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7b65-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7b65-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="f7b65-113">-Force</span></span>
<span data-ttu-id="f7b65-114">Tworzenie nowej grupy zasobów, jeśli określone ustawienie domyślne nie istnieje</span><span class="sxs-lookup"><span data-stu-id="f7b65-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="f7b65-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7b65-115">-ResourceGroupName</span></span>
<span data-ttu-id="f7b65-116">Nazwa grupy zasobów ustawiana jako domyślna</span><span class="sxs-lookup"><span data-stu-id="f7b65-116">Name of the resource group being set as default</span></span>

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

### <span data-ttu-id="f7b65-117">— Zakres</span><span class="sxs-lookup"><span data-stu-id="f7b65-117">-Scope</span></span>
<span data-ttu-id="f7b65-118">Określa zakres zmian kontekstu, na przykład tego, czy zmiany mają zastosowanie tylko do bieżącego procesu, czy do wszystkich sesji rozpoczętych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f7b65-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="f7b65-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f7b65-119">-Confirm</span></span>
<span data-ttu-id="f7b65-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f7b65-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7b65-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7b65-121">-WhatIf</span></span>
<span data-ttu-id="f7b65-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7b65-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7b65-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f7b65-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7b65-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b65-124">CommonParameters</span></span>
<span data-ttu-id="f7b65-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7b65-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b65-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7b65-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b65-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7b65-127">INPUTS</span></span>

### <span data-ttu-id="f7b65-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f7b65-128">System.String</span></span>

## <span data-ttu-id="f7b65-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f7b65-129">OUTPUTS</span></span>

### <span data-ttu-id="f7b65-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f7b65-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="f7b65-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f7b65-131">NOTES</span></span>

## <span data-ttu-id="f7b65-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7b65-132">RELATED LINKS</span></span>

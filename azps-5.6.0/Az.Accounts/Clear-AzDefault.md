---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/clear-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
ms.openlocfilehash: ac017af710531ff3294f858a8f95ad7529cd1c11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990613"
---
# <span data-ttu-id="11eb9-101">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="11eb9-101">Clear-AzDefault</span></span>

## <span data-ttu-id="11eb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="11eb9-103">Wyczyszczenie ustawień domyślnych ustawionych przez użytkownika w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="11eb9-103">Clears the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="11eb9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="11eb9-104">SYNTAX</span></span>

```
Clear-AzDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11eb9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="11eb9-105">DESCRIPTION</span></span>
<span data-ttu-id="11eb9-106">Polecenie Clear-AzDefault cmdlet usuwa wartości domyślne ustawione przez użytkownika w zależności od parametrów przełącznika określonych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="11eb9-106">The Clear-AzDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="11eb9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="11eb9-107">EXAMPLES</span></span>

### <span data-ttu-id="11eb9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="11eb9-108">Example 1</span></span>
```powershell
PS C:\> Clear-AzDefault
```

<span data-ttu-id="11eb9-109">To polecenie usuwa wszystkie ustawienia domyślne ustawione przez użytkownika w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="11eb9-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="11eb9-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="11eb9-110">Example 2</span></span>
```powershell
PS C:\> Clear-AzDefault -ResourceGroup
```

<span data-ttu-id="11eb9-111">To polecenie usuwa domyślną grupę zasobów ustawioną przez użytkownika w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="11eb9-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="11eb9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11eb9-112">PARAMETERS</span></span>

### <span data-ttu-id="11eb9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11eb9-113">-DefaultProfile</span></span>
<span data-ttu-id="11eb9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="11eb9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11eb9-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="11eb9-115">-Force</span></span>
<span data-ttu-id="11eb9-116">Usuwanie wszystkich ustawień domyślnych, jeśli nie określono wartości domyślnej</span><span class="sxs-lookup"><span data-stu-id="11eb9-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="11eb9-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11eb9-117">-PassThru</span></span>
<span data-ttu-id="11eb9-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="11eb9-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="11eb9-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="11eb9-119">-ResourceGroup</span></span>
<span data-ttu-id="11eb9-120">Wyczyść domyślną grupę zasobów</span><span class="sxs-lookup"><span data-stu-id="11eb9-120">Clear Default Resource Group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11eb9-121">— Zakres</span><span class="sxs-lookup"><span data-stu-id="11eb9-121">-Scope</span></span>
<span data-ttu-id="11eb9-122">Określa zakres zmian kontekstu, na przykład tego, czy zmiany mają zastosowanie tylko do bieżącego procesu, czy do wszystkich sesji rozpoczętych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="11eb9-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="11eb9-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11eb9-123">-Confirm</span></span>
<span data-ttu-id="11eb9-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="11eb9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11eb9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11eb9-125">-WhatIf</span></span>
<span data-ttu-id="11eb9-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11eb9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11eb9-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="11eb9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11eb9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11eb9-128">CommonParameters</span></span>
<span data-ttu-id="11eb9-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11eb9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11eb9-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11eb9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11eb9-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11eb9-131">INPUTS</span></span>

### <span data-ttu-id="11eb9-132">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="11eb9-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="11eb9-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11eb9-133">OUTPUTS</span></span>

### <span data-ttu-id="11eb9-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="11eb9-134">System.Boolean</span></span>

## <span data-ttu-id="11eb9-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="11eb9-135">NOTES</span></span>

## <span data-ttu-id="11eb9-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11eb9-136">RELATED LINKS</span></span>

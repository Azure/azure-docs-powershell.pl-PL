---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: f5307df3a91503f072c8292fe37957ce9af0df49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954929"
---
# <span data-ttu-id="97b80-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="97b80-101">Remove-AzContext</span></span>

## <span data-ttu-id="97b80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97b80-102">SYNOPSIS</span></span>
<span data-ttu-id="97b80-103">Usuwanie kontekstu z zestawu dostępnych kontekstów</span><span class="sxs-lookup"><span data-stu-id="97b80-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="97b80-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="97b80-104">SYNTAX</span></span>

### <span data-ttu-id="97b80-105">RemoveByInputObject (domyślne)</span><span class="sxs-lookup"><span data-stu-id="97b80-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97b80-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="97b80-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="97b80-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="97b80-107">DESCRIPTION</span></span>
<span data-ttu-id="97b80-108">Usuwanie kontekstu platformy Azure z zestawu kontekstów</span><span class="sxs-lookup"><span data-stu-id="97b80-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="97b80-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="97b80-109">EXAMPLES</span></span>

### <span data-ttu-id="97b80-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="97b80-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="97b80-111">Usuwanie kontekstu o nazwie domyślnej</span><span class="sxs-lookup"><span data-stu-id="97b80-111">Remove the context named default</span></span>

## <span data-ttu-id="97b80-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97b80-112">PARAMETERS</span></span>

### <span data-ttu-id="97b80-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b80-113">-DefaultProfile</span></span>
<span data-ttu-id="97b80-114">Poświadczenia, dzierżawy i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="97b80-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97b80-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="97b80-115">-Force</span></span>
<span data-ttu-id="97b80-116">Usuwanie kontekstu, nawet jeśli jest to ustawienie domyślne</span><span class="sxs-lookup"><span data-stu-id="97b80-116">Remove context even if it is the default</span></span>

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

### <span data-ttu-id="97b80-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97b80-117">-InputObject</span></span>
<span data-ttu-id="97b80-118">Obiekt kontekstowy, który zwykle przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="97b80-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97b80-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="97b80-119">-Name</span></span>
<span data-ttu-id="97b80-120">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="97b80-120">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b80-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97b80-121">-PassThru</span></span>
<span data-ttu-id="97b80-122">Zwracanie usuniętego kontekstu</span><span class="sxs-lookup"><span data-stu-id="97b80-122">Return the removed context</span></span>

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

### <span data-ttu-id="97b80-123">— Zakres</span><span class="sxs-lookup"><span data-stu-id="97b80-123">-Scope</span></span>
<span data-ttu-id="97b80-124">Określa zakres zmian kontekstu, na przykład to, czy zmiany mają zastosowanie tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="97b80-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="97b80-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="97b80-125">-Confirm</span></span>
<span data-ttu-id="97b80-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="97b80-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97b80-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97b80-127">-WhatIf</span></span>
<span data-ttu-id="97b80-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97b80-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97b80-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="97b80-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97b80-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b80-130">CommonParameters</span></span>
<span data-ttu-id="97b80-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97b80-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b80-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97b80-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b80-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97b80-133">INPUTS</span></span>

### <span data-ttu-id="97b80-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="97b80-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="97b80-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97b80-135">OUTPUTS</span></span>

### <span data-ttu-id="97b80-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="97b80-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="97b80-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="97b80-137">NOTES</span></span>

## <span data-ttu-id="97b80-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97b80-138">RELATED LINKS</span></span>

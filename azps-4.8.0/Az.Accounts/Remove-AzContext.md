---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: d5c31519ba55babb79e3e902a01e46746c5b70f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220874"
---
# <span data-ttu-id="dd19e-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="dd19e-101">Remove-AzContext</span></span>

## <span data-ttu-id="dd19e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd19e-102">SYNOPSIS</span></span>
<span data-ttu-id="dd19e-103">Usuwanie kontekstu z zestawu dostępnych kontekstów</span><span class="sxs-lookup"><span data-stu-id="dd19e-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="dd19e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd19e-104">SYNTAX</span></span>

### <span data-ttu-id="dd19e-105">RemoveByInputObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dd19e-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd19e-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="dd19e-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="dd19e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dd19e-107">DESCRIPTION</span></span>
<span data-ttu-id="dd19e-108">Usuwanie kontekstu platformy Azure z zestawu kontekstów</span><span class="sxs-lookup"><span data-stu-id="dd19e-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="dd19e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd19e-109">EXAMPLES</span></span>

### <span data-ttu-id="dd19e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dd19e-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="dd19e-111">Usuwanie kontekstu o nazwie Default</span><span class="sxs-lookup"><span data-stu-id="dd19e-111">Remove the context named default</span></span>

## <span data-ttu-id="dd19e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd19e-112">PARAMETERS</span></span>

### <span data-ttu-id="dd19e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd19e-113">-DefaultProfile</span></span>
<span data-ttu-id="dd19e-114">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd19e-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd19e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dd19e-115">-Force</span></span>
<span data-ttu-id="dd19e-116">Usuwanie kontekstu nawet w przypadku, gdy jest to ustawienie domyślne</span><span class="sxs-lookup"><span data-stu-id="dd19e-116">Remove context even if it is the default</span></span>

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

### <span data-ttu-id="dd19e-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dd19e-117">-InputObject</span></span>
<span data-ttu-id="dd19e-118">Obiekt kontekstu, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="dd19e-118">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="dd19e-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dd19e-119">-Name</span></span>
<span data-ttu-id="dd19e-120">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="dd19e-120">The name of the context</span></span>

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

### <span data-ttu-id="dd19e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd19e-121">-PassThru</span></span>
<span data-ttu-id="dd19e-122">Zwracanie usuniętego kontekstu</span><span class="sxs-lookup"><span data-stu-id="dd19e-122">Return the removed context</span></span>

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

### <span data-ttu-id="dd19e-123">-Zakres</span><span class="sxs-lookup"><span data-stu-id="dd19e-123">-Scope</span></span>
<span data-ttu-id="dd19e-124">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dd19e-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="dd19e-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd19e-125">-Confirm</span></span>
<span data-ttu-id="dd19e-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd19e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd19e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd19e-127">-WhatIf</span></span>
<span data-ttu-id="dd19e-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd19e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd19e-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dd19e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd19e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd19e-130">CommonParameters</span></span>
<span data-ttu-id="dd19e-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd19e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd19e-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd19e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd19e-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd19e-133">INPUTS</span></span>

### <span data-ttu-id="dd19e-134">Microsoft. Azure. Commands. profile. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="dd19e-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="dd19e-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd19e-135">OUTPUTS</span></span>

### <span data-ttu-id="dd19e-136">Microsoft. Azure. Commands. profile. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="dd19e-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="dd19e-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd19e-137">NOTES</span></span>

## <span data-ttu-id="dd19e-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd19e-138">RELATED LINKS</span></span>

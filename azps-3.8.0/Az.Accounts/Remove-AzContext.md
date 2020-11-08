---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: d5c31519ba55babb79e3e902a01e46746c5b70f1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050968"
---
# <span data-ttu-id="87c78-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="87c78-101">Remove-AzContext</span></span>

## <span data-ttu-id="87c78-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87c78-102">SYNOPSIS</span></span>
<span data-ttu-id="87c78-103">Usuwanie kontekstu z zestawu dostępnych kontekstów</span><span class="sxs-lookup"><span data-stu-id="87c78-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="87c78-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87c78-104">SYNTAX</span></span>

### <span data-ttu-id="87c78-105">RemoveByInputObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="87c78-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87c78-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="87c78-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="87c78-107">Opis</span><span class="sxs-lookup"><span data-stu-id="87c78-107">DESCRIPTION</span></span>
<span data-ttu-id="87c78-108">Usuwanie kontekstu platformy Azure z zestawu kontekstów</span><span class="sxs-lookup"><span data-stu-id="87c78-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="87c78-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87c78-109">EXAMPLES</span></span>

### <span data-ttu-id="87c78-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="87c78-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="87c78-111">Usuwanie kontekstu o nazwie Default</span><span class="sxs-lookup"><span data-stu-id="87c78-111">Remove the context named default</span></span>

## <span data-ttu-id="87c78-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87c78-112">PARAMETERS</span></span>

### <span data-ttu-id="87c78-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87c78-113">-DefaultProfile</span></span>
<span data-ttu-id="87c78-114">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="87c78-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87c78-115">-Force</span><span class="sxs-lookup"><span data-stu-id="87c78-115">-Force</span></span>
<span data-ttu-id="87c78-116">Usuwanie kontekstu nawet w przypadku, gdy jest to ustawienie domyślne</span><span class="sxs-lookup"><span data-stu-id="87c78-116">Remove context even if it is the default</span></span>

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

### <span data-ttu-id="87c78-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="87c78-117">-InputObject</span></span>
<span data-ttu-id="87c78-118">Obiekt kontekstu, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="87c78-118">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="87c78-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="87c78-119">-Name</span></span>
<span data-ttu-id="87c78-120">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="87c78-120">The name of the context</span></span>

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

### <span data-ttu-id="87c78-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87c78-121">-PassThru</span></span>
<span data-ttu-id="87c78-122">Zwracanie usuniętego kontekstu</span><span class="sxs-lookup"><span data-stu-id="87c78-122">Return the removed context</span></span>

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

### <span data-ttu-id="87c78-123">-Zakres</span><span class="sxs-lookup"><span data-stu-id="87c78-123">-Scope</span></span>
<span data-ttu-id="87c78-124">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="87c78-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="87c78-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87c78-125">-Confirm</span></span>
<span data-ttu-id="87c78-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87c78-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87c78-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87c78-127">-WhatIf</span></span>
<span data-ttu-id="87c78-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87c78-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87c78-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="87c78-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87c78-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87c78-130">CommonParameters</span></span>
<span data-ttu-id="87c78-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87c78-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87c78-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87c78-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87c78-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87c78-133">INPUTS</span></span>

### <span data-ttu-id="87c78-134">Microsoft. Azure. Commands. profile. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="87c78-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="87c78-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87c78-135">OUTPUTS</span></span>

### <span data-ttu-id="87c78-136">Microsoft. Azure. Commands. profile. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="87c78-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="87c78-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87c78-137">NOTES</span></span>

## <span data-ttu-id="87c78-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87c78-138">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/rename-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
ms.openlocfilehash: aea1fac4450a8625eb3d31e9f951a465344a3bd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544932"
---
# <span data-ttu-id="015e8-101">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="015e8-101">Rename-AzureRmContext</span></span>

## <span data-ttu-id="015e8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="015e8-102">SYNOPSIS</span></span>
<span data-ttu-id="015e8-103">Zmienianie nazwy kontekstu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="015e8-103">Rename an Azure context.</span></span>  <span data-ttu-id="015e8-104">Domyślnie nazwy kontekstowe są nazywane przez konto użytkownika i abonament.</span><span class="sxs-lookup"><span data-stu-id="015e8-104">By default contexts are named by user account and subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="015e8-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="015e8-105">SYNTAX</span></span>

### <span data-ttu-id="015e8-106">RenameByInputObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="015e8-106">RenameByInputObject (Default)</span></span>
```
Rename-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="015e8-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="015e8-107">RenameByName</span></span>
```
Rename-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="015e8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="015e8-108">DESCRIPTION</span></span>
<span data-ttu-id="015e8-109">Zmienianie nazwy kontekstu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="015e8-109">Rename an Azure context.</span></span>  <span data-ttu-id="015e8-110">Domyślnie nazwy kontekstowe są nazywane przez konto użytkownika i abonament.</span><span class="sxs-lookup"><span data-stu-id="015e8-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="015e8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="015e8-111">EXAMPLES</span></span>

### <span data-ttu-id="015e8-112">Zmienianie nazwy kontekstu przy użyciu nazwanych parametrów</span><span class="sxs-lookup"><span data-stu-id="015e8-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzureRmContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="015e8-113">Zmień nazwę kontekstu dla user1@contoso.org subskrypcji "12345-6789-2345-3567890" na "praca".</span><span class="sxs-lookup"><span data-stu-id="015e8-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="015e8-114">Po wykonaniu tego polecenia będziesz mieć możliwość kierowania kontekstu przy użyciu funkcji "Select-AzureRmContext Work".</span><span class="sxs-lookup"><span data-stu-id="015e8-114">After this command, you will be able to target the context using 'Select-AzureRmContext Work'.</span></span>  <span data-ttu-id="015e8-115">Zwróć uwagę, że możesz przełączać się między wartościami "SourceName" przy użyciu funkcji kończenia karty.</span><span class="sxs-lookup"><span data-stu-id="015e8-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="015e8-116">Zmienianie nazwy kontekstu przy użyciu parametrów pozycyjnych</span><span class="sxs-lookup"><span data-stu-id="015e8-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzureRmContext "My context" "Work"
```

<span data-ttu-id="015e8-117">Zmień nazwę kontekstu o nazwie "mój kontekst" na "praca".</span><span class="sxs-lookup"><span data-stu-id="015e8-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="015e8-118">Po tym poleceniu będziesz mieć możliwość kierowania kontekstu przy użyciu Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="015e8-118">After this command, you will be able to target the context using Select-AzureRmContext Work</span></span>

## <span data-ttu-id="015e8-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="015e8-119">PARAMETERS</span></span>

### <span data-ttu-id="015e8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="015e8-120">-DefaultProfile</span></span>
<span data-ttu-id="015e8-121">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="015e8-121">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="015e8-122">-Force</span><span class="sxs-lookup"><span data-stu-id="015e8-122">-Force</span></span>
<span data-ttu-id="015e8-123">Zmienianie nazwy kontekstu, nawet jeśli kontekst docelowy już istnieje</span><span class="sxs-lookup"><span data-stu-id="015e8-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="015e8-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="015e8-124">-InputObject</span></span>
<span data-ttu-id="015e8-125">Obiekt kontekstu, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="015e8-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: RenameByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="015e8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="015e8-126">-PassThru</span></span>
<span data-ttu-id="015e8-127">Zwraca kontekst o zmienionej nazwie.</span><span class="sxs-lookup"><span data-stu-id="015e8-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="015e8-128">-Zakres</span><span class="sxs-lookup"><span data-stu-id="015e8-128">-Scope</span></span>
<span data-ttu-id="015e8-129">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="015e8-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="015e8-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="015e8-130">-SourceName</span></span>
<span data-ttu-id="015e8-131">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="015e8-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RenameByName
Aliases:
Accepted values: Default

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="015e8-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="015e8-132">-TargetName</span></span>
<span data-ttu-id="015e8-133">Nowa nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="015e8-133">The new name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="015e8-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="015e8-134">-Confirm</span></span>
<span data-ttu-id="015e8-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="015e8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="015e8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="015e8-136">-WhatIf</span></span>
<span data-ttu-id="015e8-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="015e8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="015e8-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="015e8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="015e8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="015e8-139">CommonParameters</span></span>
<span data-ttu-id="015e8-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="015e8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="015e8-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="015e8-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="015e8-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="015e8-142">INPUTS</span></span>

### <span data-ttu-id="015e8-143">Microsoft. Azure. Commands. profile. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="015e8-143">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>
<span data-ttu-id="015e8-144">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="015e8-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="015e8-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="015e8-145">OUTPUTS</span></span>

### <span data-ttu-id="015e8-146">Microsoft. Azure. Commands. profile. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="015e8-146">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="015e8-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="015e8-147">NOTES</span></span>

## <span data-ttu-id="015e8-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="015e8-148">RELATED LINKS</span></span>

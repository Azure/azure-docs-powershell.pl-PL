---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/rename-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
ms.openlocfilehash: 09c0faec1ab424ef1bfb10fec35dd59646e4711c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190426"
---
# <span data-ttu-id="6b1f2-101">Rename-AzContext</span><span class="sxs-lookup"><span data-stu-id="6b1f2-101">Rename-AzContext</span></span>

## <span data-ttu-id="6b1f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b1f2-102">SYNOPSIS</span></span>
<span data-ttu-id="6b1f2-103">Zmień nazwę kontekstu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6b1f2-103">Rename an Azure context.</span></span>  <span data-ttu-id="6b1f2-104">Domyślnie konteksty są nazwane według konta użytkownika i subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6b1f2-104">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="6b1f2-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6b1f2-105">SYNTAX</span></span>

### <span data-ttu-id="6b1f2-106">RenameByInputObject (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6b1f2-106">RenameByInputObject (Default)</span></span>
```
Rename-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="6b1f2-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="6b1f2-107">RenameByName</span></span>
```
Rename-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="6b1f2-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6b1f2-108">DESCRIPTION</span></span>
<span data-ttu-id="6b1f2-109">Zmień nazwę kontekstu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6b1f2-109">Rename an Azure context.</span></span>  <span data-ttu-id="6b1f2-110">Domyślnie konteksty są nazwane według konta użytkownika i subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6b1f2-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="6b1f2-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6b1f2-111">EXAMPLES</span></span>

### <span data-ttu-id="6b1f2-112">Przykład 1. Zmienianie nazwy kontekstu przy użyciu nazwanych parametrów</span><span class="sxs-lookup"><span data-stu-id="6b1f2-112">Example 1: Rename a context using named parameters</span></span>
```powershell
PS C:\> Rename-AzContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="6b1f2-113">Zmień nazwę kontekstu dla ' na subskrypcję user1@contoso.org '12345-6789-2345-3567890' na "Służbowy".</span><span class="sxs-lookup"><span data-stu-id="6b1f2-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="6b1f2-114">Po użyciu tego polecenia będzie można kierować kontekst za pomocą polecenia "Select-AzContext Work".</span><span class="sxs-lookup"><span data-stu-id="6b1f2-114">After this command, you will be able to target the context using 'Select-AzContext Work'.</span></span>  <span data-ttu-id="6b1f2-115">Wartości parametru "SourceName" można przechodzić za pomocą klawisza Tab, używając zakończenia karty.</span><span class="sxs-lookup"><span data-stu-id="6b1f2-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="6b1f2-116">Przykład 2. Zmienianie nazwy kontekstu przy użyciu parametrów pozytowych</span><span class="sxs-lookup"><span data-stu-id="6b1f2-116">Example 2: Rename a context using positional parameters</span></span>
```powershell
PS C:\> Rename-AzContext "My context" "Work"
```

<span data-ttu-id="6b1f2-117">Zmień nazwę kontekstu o nazwie "Mój kontekst" na "Praca".</span><span class="sxs-lookup"><span data-stu-id="6b1f2-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="6b1f2-118">Po użyciu tego polecenia będzie można kierować kontekst przy użyciu Select-AzContext Work</span><span class="sxs-lookup"><span data-stu-id="6b1f2-118">After this command, you will be able to target the context using Select-AzContext Work</span></span>

## <span data-ttu-id="6b1f2-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b1f2-119">PARAMETERS</span></span>

### <span data-ttu-id="6b1f2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b1f2-120">-DefaultProfile</span></span>
<span data-ttu-id="6b1f2-121">Poświadczenia, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="6b1f2-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b1f2-122">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="6b1f2-122">-Force</span></span>
<span data-ttu-id="6b1f2-123">Zmienianie nazwy kontekstu, nawet jeśli kontekst docelowy już istnieje</span><span class="sxs-lookup"><span data-stu-id="6b1f2-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="6b1f2-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b1f2-124">-InputObject</span></span>
<span data-ttu-id="6b1f2-125">Obiekt kontekstowy, który zwykle przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="6b1f2-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RenameByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b1f2-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b1f2-126">-PassThru</span></span>
<span data-ttu-id="6b1f2-127">Zwracanie kontekstu ze zmienioną nazwę.</span><span class="sxs-lookup"><span data-stu-id="6b1f2-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="6b1f2-128">— Zakres</span><span class="sxs-lookup"><span data-stu-id="6b1f2-128">-Scope</span></span>
<span data-ttu-id="6b1f2-129">Określa zakres zmian kontekstu, na przykład to, czy zmiany mają zastosowanie tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6b1f2-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="6b1f2-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="6b1f2-130">-SourceName</span></span>
<span data-ttu-id="6b1f2-131">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="6b1f2-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RenameByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b1f2-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="6b1f2-132">-TargetName</span></span>
<span data-ttu-id="6b1f2-133">Nowa nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="6b1f2-133">The new name of the context</span></span>

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

### <span data-ttu-id="6b1f2-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6b1f2-134">-Confirm</span></span>
<span data-ttu-id="6b1f2-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6b1f2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b1f2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b1f2-136">-WhatIf</span></span>
<span data-ttu-id="6b1f2-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b1f2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b1f2-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6b1f2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b1f2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b1f2-139">CommonParameters</span></span>
<span data-ttu-id="6b1f2-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b1f2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b1f2-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b1f2-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b1f2-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b1f2-142">INPUTS</span></span>

### <span data-ttu-id="6b1f2-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="6b1f2-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="6b1f2-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6b1f2-144">OUTPUTS</span></span>

### <span data-ttu-id="6b1f2-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="6b1f2-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="6b1f2-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6b1f2-146">NOTES</span></span>

## <span data-ttu-id="6b1f2-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b1f2-147">RELATED LINKS</span></span>

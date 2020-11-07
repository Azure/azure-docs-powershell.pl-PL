---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
ms.openlocfilehash: 9c9c0c3c52f610c0bb2c0198e9995cf2804b2b24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719270"
---
# <span data-ttu-id="8529b-101">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="8529b-101">Rename-AzureRmContext</span></span>

## <span data-ttu-id="8529b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8529b-102">SYNOPSIS</span></span>
<span data-ttu-id="8529b-103">Zmienianie nazwy kontekstu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8529b-103">Rename an Azure context.</span></span>  <span data-ttu-id="8529b-104">Domyślnie nazwy kontekstowe są nazywane przez konto użytkownika i abonament.</span><span class="sxs-lookup"><span data-stu-id="8529b-104">By default contexts are named by user account and subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8529b-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8529b-105">SYNTAX</span></span>

### <span data-ttu-id="8529b-106">Obiekt wejściowy (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8529b-106">Input Object (Default)</span></span>
```
Rename-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="8529b-107">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="8529b-107">Context Name</span></span>
```
Rename-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="8529b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8529b-108">DESCRIPTION</span></span>
<span data-ttu-id="8529b-109">Zmienianie nazwy kontekstu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8529b-109">Rename an Azure context.</span></span>  <span data-ttu-id="8529b-110">Domyślnie nazwy kontekstowe są nazywane przez konto użytkownika i abonament.</span><span class="sxs-lookup"><span data-stu-id="8529b-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="8529b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8529b-111">EXAMPLES</span></span>

### <span data-ttu-id="8529b-112">Zmienianie nazwy kontekstu przy użyciu nazwanych parametrów</span><span class="sxs-lookup"><span data-stu-id="8529b-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzureRmContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="8529b-113">Zmień nazwę kontekstu dla user1@contoso.org subskrypcji "12345-6789-2345-3567890" na "praca".</span><span class="sxs-lookup"><span data-stu-id="8529b-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="8529b-114">Po wykonaniu tego polecenia będziesz mieć możliwość kierowania kontekstu przy użyciu funkcji "Select-AzureRmContext Work".</span><span class="sxs-lookup"><span data-stu-id="8529b-114">After this command, you will be able to target the context using 'Select-AzureRmContext Work'.</span></span>  <span data-ttu-id="8529b-115">Zwróć uwagę, że możesz przełączać się między wartościami "SourceName" przy użyciu funkcji kończenia karty.</span><span class="sxs-lookup"><span data-stu-id="8529b-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="8529b-116">Zmienianie nazwy kontekstu przy użyciu parametrów pozycyjnych</span><span class="sxs-lookup"><span data-stu-id="8529b-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzureRmContext "My context" "Work"
```

<span data-ttu-id="8529b-117">Zmień nazwę kontekstu o nazwie "mój kontekst" na "praca".</span><span class="sxs-lookup"><span data-stu-id="8529b-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="8529b-118">Po tym poleceniu będziesz mieć możliwość kierowania kontekstu przy użyciu Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="8529b-118">After this command, you will be able to target the context using Select-AzureRmContext Work</span></span>

## <span data-ttu-id="8529b-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8529b-119">PARAMETERS</span></span>

### <span data-ttu-id="8529b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8529b-120">-DefaultProfile</span></span>
<span data-ttu-id="8529b-121">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8529b-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8529b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="8529b-122">-Force</span></span>
<span data-ttu-id="8529b-123">Zmienianie nazwy kontekstu, nawet jeśli kontekst docelowy już istnieje</span><span class="sxs-lookup"><span data-stu-id="8529b-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="8529b-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8529b-124">-InputObject</span></span>
<span data-ttu-id="8529b-125">Obiekt kontekstu, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="8529b-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Input Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8529b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8529b-126">-PassThru</span></span>
<span data-ttu-id="8529b-127">Zwraca kontekst o zmienionej nazwie.</span><span class="sxs-lookup"><span data-stu-id="8529b-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="8529b-128">-Zakres</span><span class="sxs-lookup"><span data-stu-id="8529b-128">-Scope</span></span>
<span data-ttu-id="8529b-129">Określa zakres zmian kontekstu, na przykład wheher zmiany dotyczą tylko procesu cusrrent lub wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8529b-129">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="8529b-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="8529b-130">-SourceName</span></span>
<span data-ttu-id="8529b-131">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="8529b-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: Context Name
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8529b-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="8529b-132">-TargetName</span></span>
<span data-ttu-id="8529b-133">Nowa nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="8529b-133">The new name of the context</span></span>

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

### <span data-ttu-id="8529b-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8529b-134">-Confirm</span></span>
<span data-ttu-id="8529b-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8529b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8529b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8529b-136">-WhatIf</span></span>
<span data-ttu-id="8529b-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8529b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8529b-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8529b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8529b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8529b-139">CommonParameters</span></span>
<span data-ttu-id="8529b-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8529b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8529b-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8529b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8529b-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8529b-142">INPUTS</span></span>

### <span data-ttu-id="8529b-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8529b-143">None</span></span>

## <span data-ttu-id="8529b-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8529b-144">OUTPUTS</span></span>

### <span data-ttu-id="8529b-145">Microsoft. Azure. Commands. profile. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="8529b-145">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="8529b-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8529b-146">NOTES</span></span>

## <span data-ttu-id="8529b-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8529b-147">RELATED LINKS</span></span>


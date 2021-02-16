---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 2d3506fcf0968e58a71d81fbabe56f08428af761
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176578"
---
# <span data-ttu-id="04a36-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="04a36-101">Save-AzContext</span></span>

## <span data-ttu-id="04a36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04a36-102">SYNOPSIS</span></span>
<span data-ttu-id="04a36-103">Zapisuje bieżące informacje o uwierzytelnieniu do użycia w innych sesjach programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="04a36-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="04a36-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="04a36-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04a36-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="04a36-105">DESCRIPTION</span></span>
<span data-ttu-id="04a36-106">Polecenie Save-AzContext umożliwia zapisanie bieżących informacji o uwierzytelnieniu do użycia w innych sesjach programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="04a36-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="04a36-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="04a36-107">EXAMPLES</span></span>

### <span data-ttu-id="04a36-108">Przykład 1. Zapisywanie kontekstu bieżącej sesji</span><span class="sxs-lookup"><span data-stu-id="04a36-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="04a36-109">W tym przykładzie kontekst platformy Azure bieżącej sesji jest zapisywany w dostarczonym pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="04a36-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="04a36-110">Przykład 2. Zapisywanie danego kontekstu</span><span class="sxs-lookup"><span data-stu-id="04a36-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="04a36-111">W tym przykładzie jest zapisywany kontekst platformy Azure, który jest przekazywany do polecenia cmdlet w dostarczonym pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="04a36-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="04a36-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04a36-112">PARAMETERS</span></span>

### <span data-ttu-id="04a36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04a36-113">-DefaultProfile</span></span>
<span data-ttu-id="04a36-114">Poświadczenia, dzierżawy i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="04a36-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04a36-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="04a36-115">-Force</span></span>
<span data-ttu-id="04a36-116">Zastępowanie danego pliku, jeśli istnieje</span><span class="sxs-lookup"><span data-stu-id="04a36-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="04a36-117">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="04a36-117">-Path</span></span>
<span data-ttu-id="04a36-118">Określa ścieżkę pliku, w którym mają być zapisywanie informacji uwierzytelnianych.</span><span class="sxs-lookup"><span data-stu-id="04a36-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="04a36-119">— Profil</span><span class="sxs-lookup"><span data-stu-id="04a36-119">-Profile</span></span>
<span data-ttu-id="04a36-120">Określa kontekst platformy Azure, z którego będzie odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04a36-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="04a36-121">Jeśli nie określisz kontekstu, to polecenie cmdlet będzie odczytywane z lokalnego kontekstu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="04a36-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04a36-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="04a36-122">-Confirm</span></span>
<span data-ttu-id="04a36-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="04a36-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04a36-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04a36-124">-WhatIf</span></span>
<span data-ttu-id="04a36-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04a36-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04a36-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="04a36-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04a36-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04a36-127">CommonParameters</span></span>
<span data-ttu-id="04a36-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04a36-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04a36-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04a36-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04a36-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04a36-130">INPUTS</span></span>

### <span data-ttu-id="04a36-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="04a36-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="04a36-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="04a36-132">OUTPUTS</span></span>

### <span data-ttu-id="04a36-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="04a36-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="04a36-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="04a36-134">NOTES</span></span>

## <span data-ttu-id="04a36-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04a36-135">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 2d3506fcf0968e58a71d81fbabe56f08428af761
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331465"
---
# <span data-ttu-id="0c2b2-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="0c2b2-101">Save-AzContext</span></span>

## <span data-ttu-id="0c2b2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c2b2-102">SYNOPSIS</span></span>
<span data-ttu-id="0c2b2-103">Zapisuje bieżące informacje o uwierzytelnianiu do użycia w innych sesjach programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0c2b2-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="0c2b2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c2b2-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c2b2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0c2b2-105">DESCRIPTION</span></span>
<span data-ttu-id="0c2b2-106">Polecenie cmdlet Save-AzContext zapisuje bieżące informacje o uwierzytelnianiu do użycia w innych sesjach programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0c2b2-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="0c2b2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c2b2-107">EXAMPLES</span></span>

### <span data-ttu-id="0c2b2-108">Przykład 1. zapisywanie kontekstu bieżącej sesji</span><span class="sxs-lookup"><span data-stu-id="0c2b2-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="0c2b2-109">W tym przykładzie zapisywany jest kontekst platformy Azure bieżącej sesji w udostępnionym pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="0c2b2-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="0c2b2-110">Przykład 2: zapisanie określonego kontekstu</span><span class="sxs-lookup"><span data-stu-id="0c2b2-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="0c2b2-111">W tym przykładzie zapisywany jest kontekst platformy Azure przekazany do polecenia cmdlet do dostarczonego pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="0c2b2-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="0c2b2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c2b2-112">PARAMETERS</span></span>

### <span data-ttu-id="0c2b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c2b2-113">-DefaultProfile</span></span>
<span data-ttu-id="0c2b2-114">Poświadczenia, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c2b2-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c2b2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0c2b2-115">-Force</span></span>
<span data-ttu-id="0c2b2-116">Zastąpienie danego pliku, jeśli istnieje</span><span class="sxs-lookup"><span data-stu-id="0c2b2-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="0c2b2-117">-Path</span><span class="sxs-lookup"><span data-stu-id="0c2b2-117">-Path</span></span>
<span data-ttu-id="0c2b2-118">Określa ścieżkę pliku, do którego mają zostać zapisane informacje uwierzytelniające.</span><span class="sxs-lookup"><span data-stu-id="0c2b2-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="0c2b2-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="0c2b2-119">-Profile</span></span>
<span data-ttu-id="0c2b2-120">Określa kontekst platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c2b2-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="0c2b2-121">Jeśli nie określisz kontekstu, to polecenie cmdlet odczytuje dane z lokalnego kontekstu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="0c2b2-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="0c2b2-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c2b2-122">-Confirm</span></span>
<span data-ttu-id="0c2b2-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c2b2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c2b2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c2b2-124">-WhatIf</span></span>
<span data-ttu-id="0c2b2-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c2b2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c2b2-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0c2b2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c2b2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c2b2-127">CommonParameters</span></span>
<span data-ttu-id="0c2b2-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c2b2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c2b2-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c2b2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c2b2-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c2b2-130">INPUTS</span></span>

### <span data-ttu-id="0c2b2-131">Microsoft. Azure. Commands. Common. Authentication. models. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="0c2b2-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="0c2b2-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c2b2-132">OUTPUTS</span></span>

### <span data-ttu-id="0c2b2-133">Microsoft. Azure. Commands. profile. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="0c2b2-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="0c2b2-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c2b2-134">NOTES</span></span>

## <span data-ttu-id="0c2b2-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c2b2-135">RELATED LINKS</span></span>

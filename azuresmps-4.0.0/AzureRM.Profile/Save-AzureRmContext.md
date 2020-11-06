---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: f3afbd9b96de51f754dd87dfa42ed6f71e5b3577
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522685"
---
# <span data-ttu-id="1619a-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="1619a-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="1619a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1619a-102">SYNOPSIS</span></span>
<span data-ttu-id="1619a-103">Zapisuje bieżące informacje o uwierzytelnianiu do użycia w innych sesjach programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1619a-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="1619a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1619a-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="1619a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1619a-105">DESCRIPTION</span></span>
<span data-ttu-id="1619a-106">Polecenie cmdlet Save-AzureRmContext zapisuje bieżące informacje o uwierzytelnianiu do użycia w innych sesjach programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1619a-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="1619a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1619a-107">EXAMPLES</span></span>

### <span data-ttu-id="1619a-108">Przykład 1. zapisywanie kontekstu bieżącej sesji</span><span class="sxs-lookup"><span data-stu-id="1619a-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="1619a-109">W tym przykładzie zapisywany jest kontekst platformy Azure bieżącej sesji w udostępnionym pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="1619a-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="1619a-110">Przykład 2: zapisanie określonego kontekstu</span><span class="sxs-lookup"><span data-stu-id="1619a-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="1619a-111">W tym przykładzie zapisywany jest kontekst platformy Azure przekazany do polecenia cmdlet do dostarczonego pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="1619a-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="1619a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1619a-112">PARAMETERS</span></span>

### <span data-ttu-id="1619a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1619a-113">-Force</span></span>
<span data-ttu-id="1619a-114">Zastąpienie danego pliku, jeśli istnieje</span><span class="sxs-lookup"><span data-stu-id="1619a-114">Overwrite the given file if it exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1619a-115">-Path</span><span class="sxs-lookup"><span data-stu-id="1619a-115">-Path</span></span>
<span data-ttu-id="1619a-116">Określa ścieżkę pliku, do którego mają zostać zapisane informacje uwierzytelniające.</span><span class="sxs-lookup"><span data-stu-id="1619a-116">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1619a-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="1619a-117">-Profile</span></span>
<span data-ttu-id="1619a-118">Określa kontekst platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1619a-118">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="1619a-119">Jeśli nie określisz kontekstu, to polecenie cmdlet odczytuje dane z lokalnego kontekstu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="1619a-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1619a-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1619a-120">-Confirm</span></span>
<span data-ttu-id="1619a-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1619a-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1619a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1619a-122">-WhatIf</span></span>
<span data-ttu-id="1619a-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1619a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1619a-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1619a-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="1619a-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1619a-125">INPUTS</span></span>

### <span data-ttu-id="1619a-126">Microsoft. Azure. Commands. Common. Authentication. models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="1619a-126">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>

## <span data-ttu-id="1619a-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1619a-127">OUTPUTS</span></span>

### <span data-ttu-id="1619a-128">Microsoft. Azure. Commands. profile. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="1619a-128">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="1619a-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1619a-129">NOTES</span></span>

## <span data-ttu-id="1619a-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1619a-130">RELATED LINKS</span></span>


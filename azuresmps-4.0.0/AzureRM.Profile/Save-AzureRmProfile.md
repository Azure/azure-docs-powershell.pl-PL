---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06a78584437021df570bc5ff2b6ec19e332bffd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523553"
---
# <span data-ttu-id="41899-101">Save-AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="41899-101">Save-AzureRmProfile</span></span>

## <span data-ttu-id="41899-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41899-102">SYNOPSIS</span></span>
<span data-ttu-id="41899-103">Zapisuje bieżące informacje o uwierzytelnianiu do użycia w innych sesjach programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="41899-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="41899-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41899-104">SYNTAX</span></span>

```
Save-AzureRmProfile [[-Profile] <AzureRMProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="41899-105">Opis</span><span class="sxs-lookup"><span data-stu-id="41899-105">DESCRIPTION</span></span>
<span data-ttu-id="41899-106">Polecenie cmdlet Save-AzureRmProfile zapisuje bieżące informacje o uwierzytelnianiu do użycia w innych sesjach programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="41899-106">The Save-AzureRmProfile cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="41899-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41899-107">EXAMPLES</span></span>

### <span data-ttu-id="41899-108">Przykład 1. zapisywanie bieżącego profilu sesji</span><span class="sxs-lookup"><span data-stu-id="41899-108">Example 1: Saving the current session's profile</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmProfile -Path C:\test.json
```

<span data-ttu-id="41899-109">W tym przykładzie zapisywany jest profil platformy Azure bieżącej sesji w udostępnionym pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="41899-109">This example saves the current session's Azure profile to the JSON file provided.</span></span>

### <span data-ttu-id="41899-110">Przykład 2: zapisanie określonego profilu</span><span class="sxs-lookup"><span data-stu-id="41899-110">Example 2: Saving a given profile</span></span>
```
PS C:\> Save-AzureRmProfile -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="41899-111">W tym przykładzie zapisywany jest profil platformy Azure przekazany do polecenia cmdlet do podanego pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="41899-111">This example saves the Azure profile that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="41899-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41899-112">PARAMETERS</span></span>

### <span data-ttu-id="41899-113">-Force</span><span class="sxs-lookup"><span data-stu-id="41899-113">-Force</span></span>
<span data-ttu-id="41899-114">Zastąpienie danego pliku, jeśli istnieje</span><span class="sxs-lookup"><span data-stu-id="41899-114">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="41899-115">-Path</span><span class="sxs-lookup"><span data-stu-id="41899-115">-Path</span></span>
<span data-ttu-id="41899-116">Określa ścieżkę pliku, do którego mają zostać zapisane informacje uwierzytelniające.</span><span class="sxs-lookup"><span data-stu-id="41899-116">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41899-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="41899-117">-Profile</span></span>
<span data-ttu-id="41899-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41899-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="41899-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="41899-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureRMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41899-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41899-120">-Confirm</span></span>
<span data-ttu-id="41899-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41899-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41899-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41899-122">-WhatIf</span></span>
<span data-ttu-id="41899-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41899-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41899-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="41899-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41899-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41899-125">CommonParameters</span></span>
<span data-ttu-id="41899-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41899-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41899-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41899-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41899-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41899-128">INPUTS</span></span>

## <span data-ttu-id="41899-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41899-129">OUTPUTS</span></span>

### <span data-ttu-id="41899-130">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="41899-130">PSAzureProfile</span></span>

## <span data-ttu-id="41899-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41899-131">NOTES</span></span>

## <span data-ttu-id="41899-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41899-132">RELATED LINKS</span></span>

[<span data-ttu-id="41899-133">Wybierz — AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="41899-133">Select-AzureRMProfile</span></span>]()


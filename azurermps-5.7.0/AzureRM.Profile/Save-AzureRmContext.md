---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/save-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
ms.openlocfilehash: c605921d56cb9fd70005c290d696e5f50b0d4175
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549620"
---
# <span data-ttu-id="859b2-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="859b2-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="859b2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="859b2-102">SYNOPSIS</span></span>
<span data-ttu-id="859b2-103">Zapisuje bieżące informacje o uwierzytelnianiu do użycia w innych sesjach programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="859b2-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="859b2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="859b2-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="859b2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="859b2-105">DESCRIPTION</span></span>
<span data-ttu-id="859b2-106">Polecenie cmdlet Save-AzureRmContext zapisuje bieżące informacje o uwierzytelnianiu do użycia w innych sesjach programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="859b2-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="859b2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="859b2-107">EXAMPLES</span></span>

### <span data-ttu-id="859b2-108">Przykład 1. zapisywanie kontekstu bieżącej sesji</span><span class="sxs-lookup"><span data-stu-id="859b2-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="859b2-109">W tym przykładzie zapisywany jest kontekst platformy Azure bieżącej sesji w udostępnionym pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="859b2-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="859b2-110">Przykład 2: zapisanie określonego kontekstu</span><span class="sxs-lookup"><span data-stu-id="859b2-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Connect-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="859b2-111">W tym przykładzie zapisywany jest kontekst platformy Azure przekazany do polecenia cmdlet do dostarczonego pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="859b2-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="859b2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="859b2-112">PARAMETERS</span></span>

### <span data-ttu-id="859b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="859b2-113">-DefaultProfile</span></span>
<span data-ttu-id="859b2-114">Poświadczenia, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="859b2-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="859b2-115">-Force</span></span>
<span data-ttu-id="859b2-116">Zastąpienie danego pliku, jeśli istnieje</span><span class="sxs-lookup"><span data-stu-id="859b2-116">Overwrite the given file if it exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b2-117">-Path</span><span class="sxs-lookup"><span data-stu-id="859b2-117">-Path</span></span>
<span data-ttu-id="859b2-118">Określa ścieżkę pliku, do którego mają zostać zapisane informacje uwierzytelniające.</span><span class="sxs-lookup"><span data-stu-id="859b2-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="859b2-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="859b2-119">-Profile</span></span>
<span data-ttu-id="859b2-120">Określa kontekst platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="859b2-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="859b2-121">Jeśli nie określisz kontekstu, to polecenie cmdlet odczytuje dane z lokalnego kontekstu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="859b2-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="859b2-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="859b2-122">-Confirm</span></span>
<span data-ttu-id="859b2-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="859b2-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="859b2-124">-WhatIf</span></span>
<span data-ttu-id="859b2-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="859b2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="859b2-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="859b2-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="859b2-127">CommonParameters</span></span>
<span data-ttu-id="859b2-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="859b2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="859b2-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="859b2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="859b2-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="859b2-130">INPUTS</span></span>

### <span data-ttu-id="859b2-131">Microsoft. Azure. Commands. Common. Authentication. models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="859b2-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>

## <span data-ttu-id="859b2-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="859b2-132">OUTPUTS</span></span>

### <span data-ttu-id="859b2-133">Microsoft. Azure. Commands. profile. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="859b2-133">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="859b2-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="859b2-134">NOTES</span></span>

## <span data-ttu-id="859b2-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="859b2-135">RELATED LINKS</span></span>


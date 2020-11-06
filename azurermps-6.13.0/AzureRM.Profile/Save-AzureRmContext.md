---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/save-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
ms.openlocfilehash: 451498760d85cc018b8fbade625625ec6ecc1910
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541575"
---
# <span data-ttu-id="c3930-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="c3930-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="c3930-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3930-102">SYNOPSIS</span></span>
<span data-ttu-id="c3930-103">Zapisuje bieżące informacje o uwierzytelnianiu do użycia w innych sesjach programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c3930-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3930-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3930-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3930-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c3930-105">DESCRIPTION</span></span>
<span data-ttu-id="c3930-106">Polecenie cmdlet Save-AzureRmContext zapisuje bieżące informacje o uwierzytelnianiu do użycia w innych sesjach programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c3930-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="c3930-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3930-107">EXAMPLES</span></span>

### <span data-ttu-id="c3930-108">Przykład 1. zapisywanie kontekstu bieżącej sesji</span><span class="sxs-lookup"><span data-stu-id="c3930-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="c3930-109">W tym przykładzie zapisywany jest kontekst platformy Azure bieżącej sesji w udostępnionym pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="c3930-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="c3930-110">Przykład 2: zapisanie określonego kontekstu</span><span class="sxs-lookup"><span data-stu-id="c3930-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Connect-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="c3930-111">W tym przykładzie zapisywany jest kontekst platformy Azure przekazany do polecenia cmdlet do dostarczonego pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="c3930-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="c3930-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3930-112">PARAMETERS</span></span>

### <span data-ttu-id="c3930-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3930-113">-DefaultProfile</span></span>
<span data-ttu-id="c3930-114">Poświadczenia, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3930-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3930-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c3930-115">-Force</span></span>
<span data-ttu-id="c3930-116">Zastąpienie danego pliku, jeśli istnieje</span><span class="sxs-lookup"><span data-stu-id="c3930-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="c3930-117">-Path</span><span class="sxs-lookup"><span data-stu-id="c3930-117">-Path</span></span>
<span data-ttu-id="c3930-118">Określa ścieżkę pliku, do którego mają zostać zapisane informacje uwierzytelniające.</span><span class="sxs-lookup"><span data-stu-id="c3930-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="c3930-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="c3930-119">-Profile</span></span>
<span data-ttu-id="c3930-120">Określa kontekst platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3930-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="c3930-121">Jeśli nie określisz kontekstu, to polecenie cmdlet odczytuje dane z lokalnego kontekstu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="c3930-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="c3930-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c3930-122">-Confirm</span></span>
<span data-ttu-id="c3930-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3930-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3930-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3930-124">-WhatIf</span></span>
<span data-ttu-id="c3930-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3930-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3930-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c3930-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3930-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3930-127">CommonParameters</span></span>
<span data-ttu-id="c3930-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3930-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3930-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3930-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3930-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3930-130">INPUTS</span></span>

### <span data-ttu-id="c3930-131">Microsoft. Azure. Commands. Common. Authentication. models. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="c3930-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>
<span data-ttu-id="c3930-132">Parametry: profile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c3930-132">Parameters: Profile (ByValue)</span></span>

## <span data-ttu-id="c3930-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3930-133">OUTPUTS</span></span>

### <span data-ttu-id="c3930-134">Microsoft. Azure. Commands. profile. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="c3930-134">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="c3930-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3930-135">NOTES</span></span>

## <span data-ttu-id="c3930-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3930-136">RELATED LINKS</span></span>

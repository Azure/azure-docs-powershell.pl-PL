---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
ms.openlocfilehash: 8bc129ddc1b4291ea7b3c9100a964bf5bb1dcee6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553799"
---
# <span data-ttu-id="ef034-101">Remove-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="ef034-101">Remove-AzureRmContext</span></span>

## <span data-ttu-id="ef034-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ef034-102">SYNOPSIS</span></span>
<span data-ttu-id="ef034-103">Usuwanie kontekstu z zestawu dostępnych kontekstów</span><span class="sxs-lookup"><span data-stu-id="ef034-103">Remove a context from the set of available contexts</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef034-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ef034-104">SYNTAX</span></span>

### <span data-ttu-id="ef034-105">Obiekt wejściowy (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ef034-105">Input Object (Default)</span></span>
```
Remove-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef034-106">Nazwany kontekst</span><span class="sxs-lookup"><span data-stu-id="ef034-106">Named Context</span></span>
```
Remove-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="ef034-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ef034-107">DESCRIPTION</span></span>
<span data-ttu-id="ef034-108">Usuwanie kontekstu platformy Azure z zestawu kontekstów</span><span class="sxs-lookup"><span data-stu-id="ef034-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="ef034-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ef034-109">EXAMPLES</span></span>

### <span data-ttu-id="ef034-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ef034-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmContext -Name Default
```

<span data-ttu-id="ef034-111">Usuwanie kontekstu o nazwie Default</span><span class="sxs-lookup"><span data-stu-id="ef034-111">Remove the context named default</span></span>

## <span data-ttu-id="ef034-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ef034-112">PARAMETERS</span></span>

### <span data-ttu-id="ef034-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef034-113">-DefaultProfile</span></span>
<span data-ttu-id="ef034-114">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef034-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef034-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ef034-115">-Force</span></span>
<span data-ttu-id="ef034-116">Usuń kontekst, nawet jeśli jest defualt</span><span class="sxs-lookup"><span data-stu-id="ef034-116">Remove context even if it is the defualt</span></span>

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

### <span data-ttu-id="ef034-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ef034-117">-InputObject</span></span>
<span data-ttu-id="ef034-118">Obiekt kontekstu, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="ef034-118">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="ef034-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ef034-119">-Name</span></span>
<span data-ttu-id="ef034-120">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="ef034-120">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: Named Context
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef034-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef034-121">-PassThru</span></span>
<span data-ttu-id="ef034-122">Zwracanie usuniętego kontekstu</span><span class="sxs-lookup"><span data-stu-id="ef034-122">Return the removed context</span></span>

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

### <span data-ttu-id="ef034-123">-Zakres</span><span class="sxs-lookup"><span data-stu-id="ef034-123">-Scope</span></span>
<span data-ttu-id="ef034-124">Określa zakres zmian kontekstu, na przykład wheher zmiany dotyczą tylko procesu cusrrent lub wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ef034-124">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="ef034-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ef034-125">-Confirm</span></span>
<span data-ttu-id="ef034-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef034-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef034-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef034-127">-WhatIf</span></span>
<span data-ttu-id="ef034-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef034-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef034-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ef034-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef034-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef034-130">CommonParameters</span></span>
<span data-ttu-id="ef034-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef034-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef034-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef034-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef034-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef034-133">INPUTS</span></span>

### <span data-ttu-id="ef034-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ef034-134">None</span></span>

## <span data-ttu-id="ef034-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ef034-135">OUTPUTS</span></span>

### <span data-ttu-id="ef034-136">Microsoft. Azure. Commands. profile. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="ef034-136">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="ef034-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ef034-137">NOTES</span></span>

## <span data-ttu-id="ef034-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef034-138">RELATED LINKS</span></span>


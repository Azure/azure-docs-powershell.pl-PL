---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
ms.openlocfilehash: cb232bdebacfcb65cf3570854b14c28406d22b12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549627"
---
# <span data-ttu-id="0e8e4-101">Remove-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="0e8e4-101">Remove-AzureRmContext</span></span>

## <span data-ttu-id="0e8e4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e8e4-102">SYNOPSIS</span></span>
<span data-ttu-id="0e8e4-103">Usuwanie kontekstu z zestawu dostępnych kontekstów</span><span class="sxs-lookup"><span data-stu-id="0e8e4-103">Remove a context from the set of available contexts</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e8e4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e8e4-104">SYNTAX</span></span>

### <span data-ttu-id="0e8e4-105">RemoveByInputObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0e8e4-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e8e4-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="0e8e4-106">RemoveByName</span></span>
```
Remove-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="0e8e4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0e8e4-107">DESCRIPTION</span></span>
<span data-ttu-id="0e8e4-108">Usuwanie kontekstu platformy Azure z zestawu kontekstów</span><span class="sxs-lookup"><span data-stu-id="0e8e4-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="0e8e4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e8e4-109">EXAMPLES</span></span>

### <span data-ttu-id="0e8e4-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0e8e4-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmContext -Name Default
```

<span data-ttu-id="0e8e4-111">Usuwanie kontekstu o nazwie Default</span><span class="sxs-lookup"><span data-stu-id="0e8e4-111">Remove the context named default</span></span>

## <span data-ttu-id="0e8e4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e8e4-112">PARAMETERS</span></span>

### <span data-ttu-id="0e8e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e8e4-113">-DefaultProfile</span></span>
<span data-ttu-id="0e8e4-114">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e8e4-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e8e4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0e8e4-115">-Force</span></span>
<span data-ttu-id="0e8e4-116">Usuń kontekst, nawet jeśli jest defualt</span><span class="sxs-lookup"><span data-stu-id="0e8e4-116">Remove context even if it is the defualt</span></span>

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

### <span data-ttu-id="0e8e4-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0e8e4-117">-InputObject</span></span>
<span data-ttu-id="0e8e4-118">Obiekt kontekstu, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="0e8e4-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8e4-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0e8e4-119">-Name</span></span>
<span data-ttu-id="0e8e4-120">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="0e8e4-120">The name of the context</span></span>

```yaml
Type: String
Parameter Sets: RemoveByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8e4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e8e4-121">-PassThru</span></span>
<span data-ttu-id="0e8e4-122">Zwracanie usuniętego kontekstu</span><span class="sxs-lookup"><span data-stu-id="0e8e4-122">Return the removed context</span></span>

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

### <span data-ttu-id="0e8e4-123">-Zakres</span><span class="sxs-lookup"><span data-stu-id="0e8e4-123">-Scope</span></span>
<span data-ttu-id="0e8e4-124">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0e8e4-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8e4-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0e8e4-125">-Confirm</span></span>
<span data-ttu-id="0e8e4-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e8e4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e8e4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e8e4-127">-WhatIf</span></span>
<span data-ttu-id="0e8e4-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e8e4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e8e4-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0e8e4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e8e4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e8e4-130">CommonParameters</span></span>
<span data-ttu-id="0e8e4-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e8e4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e8e4-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e8e4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e8e4-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e8e4-133">INPUTS</span></span>

### <span data-ttu-id="0e8e4-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0e8e4-134">None</span></span>

## <span data-ttu-id="0e8e4-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e8e4-135">OUTPUTS</span></span>

### <span data-ttu-id="0e8e4-136">Microsoft. Azure. Commands. profile. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="0e8e4-136">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="0e8e4-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e8e4-137">NOTES</span></span>

## <span data-ttu-id="0e8e4-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e8e4-138">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/clear-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
ms.openlocfilehash: 960e1b35a90b0bc1c490cbf194c20ac7a051e4d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525041"
---
# <span data-ttu-id="5fc59-101">Clear-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="5fc59-101">Clear-AzureRmContext</span></span>

## <span data-ttu-id="5fc59-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5fc59-102">SYNOPSIS</span></span>
<span data-ttu-id="5fc59-103">Usuwanie wszystkich poświadczeń Azure, kont i informacji o subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5fc59-103">Remove all Azure credentials, account, and subscription information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fc59-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5fc59-104">SYNTAX</span></span>

```
Clear-AzureRmContext -Scope <ContextModificationScope> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fc59-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5fc59-105">DESCRIPTION</span></span>
<span data-ttu-id="5fc59-106">Usuwanie wszystkich poświadczeń Azure, kont i informacji o subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5fc59-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="5fc59-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5fc59-107">EXAMPLES</span></span>

### <span data-ttu-id="5fc59-108">Wyczyść kontekst globalny</span><span class="sxs-lookup"><span data-stu-id="5fc59-108">Clear global context</span></span>
```
PS C:\> Clear-AzureRmContext -Scope CurrentUser
```

<span data-ttu-id="5fc59-109">Usuń wszystkie informacje dotyczące konta, abonamentu i poświadczeń dla dowolnej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5fc59-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="5fc59-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5fc59-110">PARAMETERS</span></span>

### <span data-ttu-id="5fc59-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fc59-111">-DefaultProfile</span></span>
<span data-ttu-id="5fc59-112">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5fc59-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5fc59-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5fc59-113">-Force</span></span>
<span data-ttu-id="5fc59-114">Usuwanie wszystkich użytkowników i grup z zakresu globalnego bez monitowania</span><span class="sxs-lookup"><span data-stu-id="5fc59-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="5fc59-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5fc59-115">-PassThru</span></span>
<span data-ttu-id="5fc59-116">Zwracanie wartości oznaczającej sukces lub niepowodzenie</span><span class="sxs-lookup"><span data-stu-id="5fc59-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="5fc59-117">-Zakres</span><span class="sxs-lookup"><span data-stu-id="5fc59-117">-Scope</span></span>
<span data-ttu-id="5fc59-118">Wyczyść kontekst tylko dla bieżącej sesji programu PowerShell lub dla wszystkich sesji.</span><span class="sxs-lookup"><span data-stu-id="5fc59-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fc59-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5fc59-119">-Confirm</span></span>
<span data-ttu-id="5fc59-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fc59-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fc59-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fc59-121">-WhatIf</span></span>
<span data-ttu-id="5fc59-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fc59-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fc59-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5fc59-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fc59-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fc59-124">CommonParameters</span></span>
<span data-ttu-id="5fc59-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fc59-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fc59-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fc59-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fc59-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5fc59-127">INPUTS</span></span>

### <span data-ttu-id="5fc59-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5fc59-128">None</span></span>

## <span data-ttu-id="5fc59-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5fc59-129">OUTPUTS</span></span>

### <span data-ttu-id="5fc59-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5fc59-130">System.Boolean</span></span>
<span data-ttu-id="5fc59-131">Prawda, jeśli kontekst został pomyślnie wyczyszczony, FAŁSZ w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="5fc59-131">True if the context was successfully cleared, false otherwise.</span></span>

## <span data-ttu-id="5fc59-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5fc59-132">NOTES</span></span>

## <span data-ttu-id="5fc59-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5fc59-133">RELATED LINKS</span></span>


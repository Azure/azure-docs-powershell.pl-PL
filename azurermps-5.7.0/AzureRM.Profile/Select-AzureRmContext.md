---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/select-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
ms.openlocfilehash: c002db2d04905c19c3229a45feb9e00b5dc15754
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551676"
---
# <span data-ttu-id="ee805-101">Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="ee805-101">Select-AzureRmContext</span></span>

## <span data-ttu-id="ee805-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ee805-102">SYNOPSIS</span></span>
<span data-ttu-id="ee805-103">Wybierz abonament i konto docelowe dla poleceń cmdlet środowiska Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee805-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee805-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ee805-104">SYNTAX</span></span>

### <span data-ttu-id="ee805-105">SelectByInputObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ee805-105">SelectByInputObject (Default)</span></span>
```
Select-AzureRmContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee805-106">SelectByName</span><span class="sxs-lookup"><span data-stu-id="ee805-106">SelectByName</span></span>
```
Select-AzureRmContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="ee805-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ee805-107">DESCRIPTION</span></span>
<span data-ttu-id="ee805-108">Wybierz abonament dla lokalizacji docelowej (lub konta lub dzierżawy) w poleceniach cmdlet środowiska Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ee805-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="ee805-109">Po tym poleceniu cmdlet przyszłe polecenia cmdlet będą wskazywać wybrany kontekst.</span><span class="sxs-lookup"><span data-stu-id="ee805-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="ee805-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ee805-110">EXAMPLES</span></span>

### <span data-ttu-id="ee805-111">Przykład 1. cel nazwanego kontekstu</span><span class="sxs-lookup"><span data-stu-id="ee805-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzureRmContext "Work"
```

<span data-ttu-id="ee805-112">Docelowe przyszłe polecenia cmdlet programu PowerShell środowiska Azure na koncie, dzierżawie i subskrypcji w kontekście "praca".</span><span class="sxs-lookup"><span data-stu-id="ee805-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="ee805-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee805-113">PARAMETERS</span></span>

### <span data-ttu-id="ee805-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee805-114">-DefaultProfile</span></span>
<span data-ttu-id="ee805-115">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ee805-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee805-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ee805-116">-InputObject</span></span>
<span data-ttu-id="ee805-117">Obiekt kontekstu, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="ee805-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: SelectByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee805-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ee805-118">-Name</span></span>
<span data-ttu-id="ee805-119">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="ee805-119">The name of the context</span></span>

```yaml
Type: String
Parameter Sets: SelectByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee805-120">-Zakres</span><span class="sxs-lookup"><span data-stu-id="ee805-120">-Scope</span></span>
<span data-ttu-id="ee805-121">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ee805-121">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="ee805-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ee805-122">-Confirm</span></span>
<span data-ttu-id="ee805-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee805-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee805-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee805-124">-WhatIf</span></span>
<span data-ttu-id="ee805-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee805-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee805-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ee805-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee805-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee805-127">CommonParameters</span></span>
<span data-ttu-id="ee805-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee805-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee805-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee805-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee805-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee805-130">INPUTS</span></span>

### <span data-ttu-id="ee805-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ee805-131">None</span></span>

## <span data-ttu-id="ee805-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ee805-132">OUTPUTS</span></span>

### <span data-ttu-id="ee805-133">Microsoft. Azure. Commands. profile. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="ee805-133">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="ee805-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ee805-134">NOTES</span></span>

## <span data-ttu-id="ee805-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee805-135">RELATED LINKS</span></span>


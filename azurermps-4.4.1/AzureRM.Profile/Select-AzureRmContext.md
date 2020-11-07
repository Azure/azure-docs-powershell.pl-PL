---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
ms.openlocfilehash: 5450939ba5d0dc2fb1ae6c475d51b6fc9187082c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717814"
---
# <span data-ttu-id="39f38-101">Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="39f38-101">Select-AzureRmContext</span></span>

## <span data-ttu-id="39f38-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="39f38-102">SYNOPSIS</span></span>
<span data-ttu-id="39f38-103">Wybierz abonament i konto docelowe dla poleceń cmdlet środowiska Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="39f38-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39f38-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="39f38-104">SYNTAX</span></span>

### <span data-ttu-id="39f38-105">Obiekt wejściowy (domyślny)</span><span class="sxs-lookup"><span data-stu-id="39f38-105">Input Object (Default)</span></span>
```
Select-AzureRmContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39f38-106">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="39f38-106">Context Name</span></span>
```
Select-AzureRmContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="39f38-107">Opis</span><span class="sxs-lookup"><span data-stu-id="39f38-107">DESCRIPTION</span></span>
<span data-ttu-id="39f38-108">Wybierz abonament dla lokalizacji docelowej (lub konta lub dzierżawy) w poleceniach cmdlet środowiska Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="39f38-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="39f38-109">Po tym poleceniu cmdlet przyszłe polecenia cmdlet będą wskazywać wybrany kontekst.</span><span class="sxs-lookup"><span data-stu-id="39f38-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="39f38-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="39f38-110">EXAMPLES</span></span>

### <span data-ttu-id="39f38-111">Przykład 1. cel nazwanego kontekstu</span><span class="sxs-lookup"><span data-stu-id="39f38-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzureRmContext "Work"
```

<span data-ttu-id="39f38-112">Docelowe przyszłe polecenia cmdlet programu PowerShell środowiska Azure na koncie, dzierżawie i subskrypcji w kontekście "praca".</span><span class="sxs-lookup"><span data-stu-id="39f38-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="39f38-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="39f38-113">PARAMETERS</span></span>

### <span data-ttu-id="39f38-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39f38-114">-DefaultProfile</span></span>
<span data-ttu-id="39f38-115">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="39f38-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39f38-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="39f38-116">-InputObject</span></span>
<span data-ttu-id="39f38-117">Obiekt kontekstu, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="39f38-117">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="39f38-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="39f38-118">-Name</span></span>
<span data-ttu-id="39f38-119">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="39f38-119">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: Context Name
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f38-120">-Zakres</span><span class="sxs-lookup"><span data-stu-id="39f38-120">-Scope</span></span>
<span data-ttu-id="39f38-121">Określa zakres zmian kontekstu, na przykład wheher zmiany dotyczą tylko procesu cusrrent lub wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="39f38-121">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="39f38-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="39f38-122">-Confirm</span></span>
<span data-ttu-id="39f38-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39f38-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39f38-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39f38-124">-WhatIf</span></span>
<span data-ttu-id="39f38-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39f38-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39f38-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="39f38-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39f38-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39f38-127">CommonParameters</span></span>
<span data-ttu-id="39f38-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39f38-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39f38-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39f38-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39f38-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39f38-130">INPUTS</span></span>

### <span data-ttu-id="39f38-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="39f38-131">None</span></span>

## <span data-ttu-id="39f38-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="39f38-132">OUTPUTS</span></span>

### <span data-ttu-id="39f38-133">Microsoft. Azure. Commands. profile. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="39f38-133">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="39f38-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="39f38-134">NOTES</span></span>

## <span data-ttu-id="39f38-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39f38-135">RELATED LINKS</span></span>


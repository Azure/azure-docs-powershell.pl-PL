---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/import-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
ms.openlocfilehash: 18dd703551603ed03eb36d19af04fcd3ab6938f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955025"
---
# <span data-ttu-id="ccb82-101">Import-AzContext</span><span class="sxs-lookup"><span data-stu-id="ccb82-101">Import-AzContext</span></span>

## <span data-ttu-id="ccb82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccb82-102">SYNOPSIS</span></span>
<span data-ttu-id="ccb82-103">Ładowanie informacji uwierzytelniania platformy Azure z pliku.</span><span class="sxs-lookup"><span data-stu-id="ccb82-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="ccb82-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ccb82-104">SYNTAX</span></span>

### <span data-ttu-id="ccb82-105">ProfileFrom Jednakowe (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ccb82-105">ProfileFromDisk (Default)</span></span>
```
Import-AzContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccb82-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="ccb82-106">InMemoryProfile</span></span>
```
Import-AzContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccb82-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ccb82-107">DESCRIPTION</span></span>
<span data-ttu-id="ccb82-108">Polecenie Import-AzContext cmdlet ładuje informacje o uwierzytelnianiu z pliku w celu ustawienia środowiska i kontekstu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ccb82-108">The Import-AzContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="ccb82-109">Polecenia cmdlet uruchomione w bieżącej sesji używają tych informacji do uwierzytelniania żądań do usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="ccb82-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="ccb82-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ccb82-110">EXAMPLES</span></span>

### <span data-ttu-id="ccb82-111">Przykład 1. Importowanie kontekstu z pliku AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="ccb82-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzContext -AzContext (Connect-AzAccount)

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="ccb82-112">W tym przykładzie kontekst z pliku PSAzureProfile, który jest przekazywany do polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccb82-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="ccb82-113">Przykład 2. Importowanie kontekstu z pliku JSON</span><span class="sxs-lookup"><span data-stu-id="ccb82-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzContext -Path C:\test.json

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="ccb82-114">W tym przykładzie wybiera kontekst z pliku JSON przekazywanego do polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccb82-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="ccb82-115">Ten plik JSON można utworzyć na podstawie pliku Save-AzContext.</span><span class="sxs-lookup"><span data-stu-id="ccb82-115">This JSON file can be created from Save-AzContext.</span></span>

## <span data-ttu-id="ccb82-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ccb82-116">PARAMETERS</span></span>

### <span data-ttu-id="ccb82-117">— AzureContext</span><span class="sxs-lookup"><span data-stu-id="ccb82-117">-AzureContext</span></span>
<span data-ttu-id="ccb82-118">{{Fill AzureContext Description}}</span><span class="sxs-lookup"><span data-stu-id="ccb82-118">{{Fill AzureContext Description}}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccb82-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccb82-119">-DefaultProfile</span></span>
<span data-ttu-id="ccb82-120">Poświadczenia, dzierżawy i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ccb82-120">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ccb82-121">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="ccb82-121">-Path</span></span>
<span data-ttu-id="ccb82-122">Określa ścieżkę do informacji kontekstowych zapisanych przy użyciu funkcji Zapisz-AzContext.</span><span class="sxs-lookup"><span data-stu-id="ccb82-122">Specifies the path to context information saved by using Save-AzContext.</span></span>

```yaml
Type: System.String
Parameter Sets: ProfileFromDisk
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccb82-123">— Zakres</span><span class="sxs-lookup"><span data-stu-id="ccb82-123">-Scope</span></span>
<span data-ttu-id="ccb82-124">Określa zakres zmian kontekstu, na przykład tego, czy zmiany mają zastosowanie tylko do bieżącego procesu, czy do wszystkich sesji rozpoczętych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ccb82-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="ccb82-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ccb82-125">-Confirm</span></span>
<span data-ttu-id="ccb82-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ccb82-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb82-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccb82-127">-WhatIf</span></span>
<span data-ttu-id="ccb82-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccb82-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ccb82-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ccb82-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb82-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccb82-130">CommonParameters</span></span>
<span data-ttu-id="ccb82-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccb82-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccb82-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ccb82-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccb82-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ccb82-133">INPUTS</span></span>

### <span data-ttu-id="ccb82-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="ccb82-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

### <span data-ttu-id="ccb82-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ccb82-135">System.String</span></span>

## <span data-ttu-id="ccb82-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ccb82-136">OUTPUTS</span></span>

### <span data-ttu-id="ccb82-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="ccb82-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="ccb82-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ccb82-138">NOTES</span></span>

## <span data-ttu-id="ccb82-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ccb82-139">RELATED LINKS</span></span>

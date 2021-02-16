---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/import-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
ms.openlocfilehash: 40d5cef72a8a1f345ac7f6389bacfb75257ccab4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190466"
---
# <span data-ttu-id="bdde1-101">Import-AzContext</span><span class="sxs-lookup"><span data-stu-id="bdde1-101">Import-AzContext</span></span>

## <span data-ttu-id="bdde1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdde1-102">SYNOPSIS</span></span>
<span data-ttu-id="bdde1-103">Ładowanie informacji uwierzytelniania platformy Azure z pliku.</span><span class="sxs-lookup"><span data-stu-id="bdde1-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="bdde1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bdde1-104">SYNTAX</span></span>

### <span data-ttu-id="bdde1-105">ProfileFrom Jednakowe (domyślne)</span><span class="sxs-lookup"><span data-stu-id="bdde1-105">ProfileFromDisk (Default)</span></span>
```
Import-AzContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdde1-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="bdde1-106">InMemoryProfile</span></span>
```
Import-AzContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdde1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="bdde1-107">DESCRIPTION</span></span>
<span data-ttu-id="bdde1-108">Polecenie Import-AzContext ładuje informacje o uwierzytelnianiu z pliku w celu ustawienia środowiska i kontekstu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bdde1-108">The Import-AzContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="bdde1-109">Polecenia cmdlet uruchomione w bieżącej sesji używają tych informacji do uwierzytelniania żądań do usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="bdde1-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="bdde1-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bdde1-110">EXAMPLES</span></span>

### <span data-ttu-id="bdde1-111">Przykład 1. Importowanie kontekstu z pliku AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="bdde1-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzContext -AzContext (Connect-AzAccount)

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="bdde1-112">W tym przykładzie kontekst z pliku PSAzureProfile, który jest przekazywany do polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdde1-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="bdde1-113">Przykład 2. Importowanie kontekstu z pliku JSON</span><span class="sxs-lookup"><span data-stu-id="bdde1-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzContext -Path C:\test.json

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="bdde1-114">W tym przykładzie wybiera kontekst z pliku JSON przekazywanego do polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdde1-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="bdde1-115">Ten plik JSON można utworzyć na podstawie pliku Save-AzContext.</span><span class="sxs-lookup"><span data-stu-id="bdde1-115">This JSON file can be created from Save-AzContext.</span></span>

## <span data-ttu-id="bdde1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdde1-116">PARAMETERS</span></span>

### <span data-ttu-id="bdde1-117">— AzureContext</span><span class="sxs-lookup"><span data-stu-id="bdde1-117">-AzureContext</span></span>
<span data-ttu-id="bdde1-118">{{Fill AzureContext Description}}</span><span class="sxs-lookup"><span data-stu-id="bdde1-118">{{Fill AzureContext Description}}</span></span>

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

### <span data-ttu-id="bdde1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdde1-119">-DefaultProfile</span></span>
<span data-ttu-id="bdde1-120">Poświadczenia, dzierżawy i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="bdde1-120">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdde1-121">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="bdde1-121">-Path</span></span>
<span data-ttu-id="bdde1-122">Określa ścieżkę do informacji kontekstowych zapisanych przy użyciu funkcji Zapisz-AzContext.</span><span class="sxs-lookup"><span data-stu-id="bdde1-122">Specifies the path to context information saved by using Save-AzContext.</span></span>

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

### <span data-ttu-id="bdde1-123">— Zakres</span><span class="sxs-lookup"><span data-stu-id="bdde1-123">-Scope</span></span>
<span data-ttu-id="bdde1-124">Określa zakres zmian kontekstu, na przykład tego, czy zmiany mają zastosowanie tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bdde1-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="bdde1-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bdde1-125">-Confirm</span></span>
<span data-ttu-id="bdde1-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bdde1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdde1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdde1-127">-WhatIf</span></span>
<span data-ttu-id="bdde1-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdde1-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bdde1-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bdde1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdde1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdde1-130">CommonParameters</span></span>
<span data-ttu-id="bdde1-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdde1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdde1-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdde1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdde1-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdde1-133">INPUTS</span></span>

### <span data-ttu-id="bdde1-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="bdde1-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

### <span data-ttu-id="bdde1-135">System.String</span><span class="sxs-lookup"><span data-stu-id="bdde1-135">System.String</span></span>

## <span data-ttu-id="bdde1-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bdde1-136">OUTPUTS</span></span>

### <span data-ttu-id="bdde1-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="bdde1-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="bdde1-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bdde1-138">NOTES</span></span>

## <span data-ttu-id="bdde1-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdde1-139">RELATED LINKS</span></span>

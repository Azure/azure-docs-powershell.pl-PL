---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/import-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
ms.openlocfilehash: 145c5f65b00da7f143b04d526b8bcd959d323d12
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707212"
---
# <span data-ttu-id="5033b-101">Import-AzContext</span><span class="sxs-lookup"><span data-stu-id="5033b-101">Import-AzContext</span></span>

## <span data-ttu-id="5033b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5033b-102">SYNOPSIS</span></span>
<span data-ttu-id="5033b-103">Ładuje informacje o uwierzytelnianiu platformy Azure z pliku.</span><span class="sxs-lookup"><span data-stu-id="5033b-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="5033b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5033b-104">SYNTAX</span></span>

### <span data-ttu-id="5033b-105">ProfileFromDisk (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5033b-105">ProfileFromDisk (Default)</span></span>
```
Import-AzContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5033b-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="5033b-106">InMemoryProfile</span></span>
```
Import-AzContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5033b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5033b-107">DESCRIPTION</span></span>
<span data-ttu-id="5033b-108">Polecenie cmdlet Import-AzContext ładuje informacje uwierzytelniające z pliku w celu ustawienia środowiska i kontekstu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5033b-108">The Import-AzContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="5033b-109">Polecenia cmdlet uruchomione w bieżącej sesji używają tych informacji do uwierzytelniania żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="5033b-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="5033b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5033b-110">EXAMPLES</span></span>

### <span data-ttu-id="5033b-111">Przykład 1: Importowanie kontekstu z AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="5033b-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzContext -AzContext (Connect-AzAccount)

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="5033b-112">W tym przykładzie zaimportowano kontekst z PSAzureProfile, który przekazano do polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5033b-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="5033b-113">Przykład 2: Importowanie kontekstu z pliku JSON</span><span class="sxs-lookup"><span data-stu-id="5033b-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzContext -Path C:\test.json

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="5033b-114">W tym przykładzie wybrano kontekst z pliku JSON przekazanego do polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5033b-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="5033b-115">Ten plik JSON można utworzyć w usłudze Save-AzContext.</span><span class="sxs-lookup"><span data-stu-id="5033b-115">This JSON file can be created from Save-AzContext.</span></span>

## <span data-ttu-id="5033b-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5033b-116">PARAMETERS</span></span>

### <span data-ttu-id="5033b-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="5033b-117">-AzureContext</span></span>
<span data-ttu-id="5033b-118">{{Fill AzureContext Description}}</span><span class="sxs-lookup"><span data-stu-id="5033b-118">{{Fill AzureContext Description}}</span></span>

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

### <span data-ttu-id="5033b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5033b-119">-DefaultProfile</span></span>
<span data-ttu-id="5033b-120">Poświadczenia, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5033b-120">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5033b-121">-Path</span><span class="sxs-lookup"><span data-stu-id="5033b-121">-Path</span></span>
<span data-ttu-id="5033b-122">Określa ścieżkę do informacji kontekstowych zapisanych przy użyciu polecenia Save-AzContext.</span><span class="sxs-lookup"><span data-stu-id="5033b-122">Specifies the path to context information saved by using Save-AzContext.</span></span>

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

### <span data-ttu-id="5033b-123">-Zakres</span><span class="sxs-lookup"><span data-stu-id="5033b-123">-Scope</span></span>
<span data-ttu-id="5033b-124">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5033b-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="5033b-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5033b-125">-Confirm</span></span>
<span data-ttu-id="5033b-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5033b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5033b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5033b-127">-WhatIf</span></span>
<span data-ttu-id="5033b-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5033b-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5033b-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5033b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5033b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5033b-130">CommonParameters</span></span>
<span data-ttu-id="5033b-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5033b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5033b-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5033b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5033b-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5033b-133">INPUTS</span></span>

### <span data-ttu-id="5033b-134">Microsoft. Azure. Commands. Common. Authentication. models. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="5033b-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

### <span data-ttu-id="5033b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5033b-135">System.String</span></span>

## <span data-ttu-id="5033b-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5033b-136">OUTPUTS</span></span>

### <span data-ttu-id="5033b-137">Microsoft. Azure. Commands. profile. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="5033b-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="5033b-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5033b-138">NOTES</span></span>

## <span data-ttu-id="5033b-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5033b-139">RELATED LINKS</span></span>

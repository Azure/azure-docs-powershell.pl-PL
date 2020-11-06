---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
ms.openlocfilehash: bb1f34a27d9f1ad5d8e851cd280751c25ebf25c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546111"
---
# <span data-ttu-id="4a52c-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="4a52c-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="4a52c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a52c-102">SYNOPSIS</span></span>
<span data-ttu-id="4a52c-103">Ładuje informacje o uwierzytelnianiu platformy Azure z pliku.</span><span class="sxs-lookup"><span data-stu-id="4a52c-103">Loads Azure authentication information from a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a52c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a52c-104">SYNTAX</span></span>

### <span data-ttu-id="4a52c-105">ProfileFromDisk (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4a52c-105">ProfileFromDisk (Default)</span></span>
```
Import-AzureRmContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a52c-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="4a52c-106">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a52c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4a52c-107">DESCRIPTION</span></span>
<span data-ttu-id="4a52c-108">Polecenie cmdlet Import-AzureRmContext ładuje informacje uwierzytelniające z pliku w celu ustawienia środowiska i kontekstu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4a52c-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="4a52c-109">Polecenia cmdlet uruchomione w bieżącej sesji używają tych informacji do uwierzytelniania żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="4a52c-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="4a52c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a52c-110">EXAMPLES</span></span>

### <span data-ttu-id="4a52c-111">Przykład 1: Importowanie kontekstu z AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="4a52c-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="4a52c-112">W tym przykładzie zaimportowano kontekst z PSAzureProfile, który przekazano do polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a52c-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="4a52c-113">Przykład 2: Importowanie kontekstu z pliku JSON</span><span class="sxs-lookup"><span data-stu-id="4a52c-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="4a52c-114">W tym przykładzie wybrano kontekst z pliku JSON przekazanego do polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a52c-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="4a52c-115">Ten plik JSON można utworzyć w usłudze Save-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="4a52c-115">This JSON file can be created from Save-AzureRmContext.</span></span>

## <span data-ttu-id="4a52c-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a52c-116">PARAMETERS</span></span>

### <span data-ttu-id="4a52c-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="4a52c-117">-AzureContext</span></span>
<span data-ttu-id="4a52c-118">Określa kontekst platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a52c-118">Specifies the Azure context from which this cmdlet reads.</span></span> <span data-ttu-id="4a52c-119">Jeśli nie określisz kontekstu, to polecenie cmdlet odczytuje dane z lokalnego kontekstu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="4a52c-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="4a52c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a52c-120">-DefaultProfile</span></span>
<span data-ttu-id="4a52c-121">Poświadczenia, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4a52c-121">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a52c-122">-Path</span><span class="sxs-lookup"><span data-stu-id="4a52c-122">-Path</span></span>
<span data-ttu-id="4a52c-123">Określa ścieżkę do informacji kontekstowych zapisanych przy użyciu polecenia Save-AzureRMContext.</span><span class="sxs-lookup"><span data-stu-id="4a52c-123">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

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

### <span data-ttu-id="4a52c-124">-Zakres</span><span class="sxs-lookup"><span data-stu-id="4a52c-124">-Scope</span></span>
<span data-ttu-id="4a52c-125">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4a52c-125">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="4a52c-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4a52c-126">-Confirm</span></span>
<span data-ttu-id="4a52c-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a52c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a52c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a52c-128">-WhatIf</span></span>
<span data-ttu-id="4a52c-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a52c-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a52c-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4a52c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a52c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a52c-131">CommonParameters</span></span>
<span data-ttu-id="4a52c-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a52c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a52c-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a52c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a52c-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a52c-134">INPUTS</span></span>

### <span data-ttu-id="4a52c-135">Microsoft. Azure. Commands. Common. Authentication. models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="4a52c-135">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>
<span data-ttu-id="4a52c-136">Zawiera zestaw poświadczeń, kont i subskrypcji, które są używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a52c-136">Contains the set of credentials, accounts, and subscriptions that are used to communicate with Azure.</span></span>

## <span data-ttu-id="4a52c-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a52c-137">OUTPUTS</span></span>

### <span data-ttu-id="4a52c-138">Microsoft. Azure. Commands. profile. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="4a52c-138">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>
<span data-ttu-id="4a52c-139">Zawiera zestaw poświadczeń, kont i subskrypcji, których można użyć do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a52c-139">Contains the set of credentials, accounts, and subscriptions that can be used to communicate with Azure.</span></span>

## <span data-ttu-id="4a52c-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a52c-140">NOTES</span></span>

## <span data-ttu-id="4a52c-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a52c-141">RELATED LINKS</span></span>


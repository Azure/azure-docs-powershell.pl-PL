---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46efba5e2ab9a5c51172264b343b0f4f2b508065
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522682"
---
# <span data-ttu-id="d55bd-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="d55bd-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="d55bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d55bd-102">SYNOPSIS</span></span>
<span data-ttu-id="d55bd-103">Ładuje informacje o uwierzytelnianiu platformy Azure z pliku.</span><span class="sxs-lookup"><span data-stu-id="d55bd-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="d55bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d55bd-104">SYNTAX</span></span>

### <span data-ttu-id="d55bd-105">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="d55bd-105">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d55bd-106">ProfileFromDisk</span><span class="sxs-lookup"><span data-stu-id="d55bd-106">ProfileFromDisk</span></span>
```
Import-AzureRmContext [-Path] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="d55bd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d55bd-107">DESCRIPTION</span></span>
<span data-ttu-id="d55bd-108">Polecenie cmdlet Import-AzureRmContext ładuje informacje uwierzytelniające z pliku w celu ustawienia środowiska i kontekstu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d55bd-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="d55bd-109">Polecenia cmdlet uruchomione w bieżącej sesji używają tych informacji do uwierzytelniania żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="d55bd-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="d55bd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d55bd-110">EXAMPLES</span></span>

### <span data-ttu-id="d55bd-111">Przykład 1: Importowanie kontekstu z AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="d55bd-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="d55bd-112">W tym przykładzie zaimportowano kontekst z PSAzureProfile, który przekazano do polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d55bd-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="d55bd-113">Przykład 2: Importowanie kontekstu z pliku JSON</span><span class="sxs-lookup"><span data-stu-id="d55bd-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="d55bd-114">W tym przykładzie wybrano kontekst z pliku JSON przekazanego do polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d55bd-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span>
<span data-ttu-id="d55bd-115">Ten plik JSON można utworzyć na podstawie elementu importu-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="d55bd-115">This JSON file can be created from Import-AzureRmContext.</span></span>

## <span data-ttu-id="d55bd-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d55bd-116">PARAMETERS</span></span>

### <span data-ttu-id="d55bd-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="d55bd-117">-AzureContext</span></span>
<span data-ttu-id="d55bd-118">Określa kontekst platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d55bd-118">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="d55bd-119">Jeśli nie określisz kontekstu, to polecenie cmdlet odczytuje dane z lokalnego kontekstu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="d55bd-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d55bd-120">-Path</span><span class="sxs-lookup"><span data-stu-id="d55bd-120">-Path</span></span>
<span data-ttu-id="d55bd-121">Określa ścieżkę do informacji kontekstowych zapisanych przy użyciu polecenia Save-AzureRMContext.</span><span class="sxs-lookup"><span data-stu-id="d55bd-121">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d55bd-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d55bd-122">-Confirm</span></span>
<span data-ttu-id="d55bd-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d55bd-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d55bd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d55bd-124">-WhatIf</span></span>
<span data-ttu-id="d55bd-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d55bd-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d55bd-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d55bd-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="d55bd-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d55bd-127">INPUTS</span></span>

### <span data-ttu-id="d55bd-128">Microsoft. Azure. Commands. Common. Authentication. models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="d55bd-128">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>
<span data-ttu-id="d55bd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d55bd-129">System.String</span></span>

## <span data-ttu-id="d55bd-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d55bd-130">OUTPUTS</span></span>

### <span data-ttu-id="d55bd-131">Microsoft. Azure. Commands. profile. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="d55bd-131">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="d55bd-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d55bd-132">NOTES</span></span>

## <span data-ttu-id="d55bd-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d55bd-133">RELATED LINKS</span></span>


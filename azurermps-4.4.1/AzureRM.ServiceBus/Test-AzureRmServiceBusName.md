---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: 892177efebb3a62e40f79b80b1ac67c488e048d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718695"
---
# <span data-ttu-id="d8ef6-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="d8ef6-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="d8ef6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8ef6-102">SYNOPSIS</span></span>
<span data-ttu-id="d8ef6-103">Sprawdza dostępność danej nazwy obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="d8ef6-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8ef6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8ef6-104">SYNTAX</span></span>

```
Test-AzureRmServiceBusName [-Namespace] <String>
```

## <span data-ttu-id="d8ef6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d8ef6-105">DESCRIPTION</span></span>
<span data-ttu-id="d8ef6-106">Polecenie cmdlet **test-AzureRmServiceBusName** sprawdza dostępność nazwy przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="d8ef6-106">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="d8ef6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8ef6-107">EXAMPLES</span></span>

### <span data-ttu-id="d8ef6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d8ef6-108">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace TestingtheAvailability
```

### <span data-ttu-id="d8ef6-109">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d8ef6-109">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace Testi
```

### <span data-ttu-id="d8ef6-110">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d8ef6-110">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace Test123
```

<span data-ttu-id="d8ef6-111">Zwraca stan dostępności nazwy przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="d8ef6-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="d8ef6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8ef6-112">PARAMETERS</span></span>

### <span data-ttu-id="d8ef6-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d8ef6-113">-Namespace</span></span>
<span data-ttu-id="d8ef6-114">Nazwa przestrzeni nazw ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="d8ef6-114">ServiceBus Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```
### <span data-ttu-id="d8ef6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8ef6-115">CommonParameters</span></span>
<span data-ttu-id="d8ef6-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8ef6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8ef6-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8ef6-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8ef6-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8ef6-118">INPUTS</span></span>

### <span data-ttu-id="d8ef6-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d8ef6-119">-Namespace</span></span>
 <span data-ttu-id="d8ef6-120">System. String</span><span class="sxs-lookup"><span data-stu-id="d8ef6-120">System.String</span></span>

## <span data-ttu-id="d8ef6-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8ef6-121">OUTPUTS</span></span>

### <span data-ttu-id="d8ef6-122">[Microsoft. Azure. Commands. ServiceBus. modele. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]</span><span class="sxs-lookup"><span data-stu-id="d8ef6-122">[Microsoft.Azure.Commands.ServiceBus.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="d8ef6-123">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d8ef6-123">Example 1</span></span>
<span data-ttu-id="d8ef6-124">Komunikat o przyczynach NameAvailable</span><span class="sxs-lookup"><span data-stu-id="d8ef6-124">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="d8ef6-125">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d8ef6-125">Example 2</span></span>
<span data-ttu-id="d8ef6-126">Komunikat o przyczynach NameAvailable</span><span class="sxs-lookup"><span data-stu-id="d8ef6-126">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="d8ef6-127">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d8ef6-127">Example 3</span></span>
<span data-ttu-id="d8ef6-128">Komunikat o przyczynach NameAvailable</span><span class="sxs-lookup"><span data-stu-id="d8ef6-128">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="d8ef6-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8ef6-129">NOTES</span></span>

## <span data-ttu-id="d8ef6-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8ef6-130">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: adf7c4b7f8d80e16b49d9d55b742a55279232a07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548024"
---
# <span data-ttu-id="648f2-101">Test-AzureRmRelayName</span><span class="sxs-lookup"><span data-stu-id="648f2-101">Test-AzureRmRelayName</span></span>

## <span data-ttu-id="648f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="648f2-102">SYNOPSIS</span></span>
<span data-ttu-id="648f2-103">Sprawdza dostępność danej nazwy obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="648f2-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="648f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="648f2-104">SYNTAX</span></span>

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="648f2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="648f2-105">DESCRIPTION</span></span>
<span data-ttu-id="648f2-106">Polecenie cmdlet **test-AzureRmRelayName** sprawdza dostępność nazwy przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="648f2-106">The **Test-AzureRmRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="648f2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="648f2-107">EXAMPLES</span></span>

### <span data-ttu-id="648f2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="648f2-108">Example 1</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability
```

### <span data-ttu-id="648f2-109">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="648f2-109">Example 2</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Testi
```

### <span data-ttu-id="648f2-110">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="648f2-110">Example 3</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Test123
```

<span data-ttu-id="648f2-111">Zwraca stan dostępności nazwy przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="648f2-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="648f2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="648f2-112">PARAMETERS</span></span>

### <span data-ttu-id="648f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="648f2-113">-DefaultProfile</span></span>
<span data-ttu-id="648f2-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="648f2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="648f2-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="648f2-115">-Namespace</span></span>
<span data-ttu-id="648f2-116">Nazwa obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="648f2-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="648f2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="648f2-117">CommonParameters</span></span>
<span data-ttu-id="648f2-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="648f2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="648f2-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="648f2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="648f2-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="648f2-120">INPUTS</span></span>

### <span data-ttu-id="648f2-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="648f2-121">-Namespace</span></span>
 <span data-ttu-id="648f2-122">System. String</span><span class="sxs-lookup"><span data-stu-id="648f2-122">System.String</span></span>

## <span data-ttu-id="648f2-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="648f2-123">OUTPUTS</span></span>

### <span data-ttu-id="648f2-124">[Microsoft. Azure. Commands. Relay. models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="648f2-124">[Microsoft.Azure.Commands.Relay.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="648f2-125">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="648f2-125">Example 1</span></span>
<span data-ttu-id="648f2-126">Komunikat o przyczynach NameAvailable</span><span class="sxs-lookup"><span data-stu-id="648f2-126">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="648f2-127">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="648f2-127">Example 2</span></span>
<span data-ttu-id="648f2-128">Komunikat o przyczynach NameAvailable</span><span class="sxs-lookup"><span data-stu-id="648f2-128">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="648f2-129">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="648f2-129">Example 3</span></span>
<span data-ttu-id="648f2-130">Komunikat o przyczynach NameAvailable</span><span class="sxs-lookup"><span data-stu-id="648f2-130">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="648f2-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="648f2-131">NOTES</span></span>

## <span data-ttu-id="648f2-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="648f2-132">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: 396243e366f6a21e2ac94d105473b348c6a8198d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550239"
---
# <span data-ttu-id="cd63c-101">Test-AzureRmRelayName</span><span class="sxs-lookup"><span data-stu-id="cd63c-101">Test-AzureRmRelayName</span></span>

## <span data-ttu-id="cd63c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd63c-102">SYNOPSIS</span></span>
<span data-ttu-id="cd63c-103">Sprawdza dostępność danej nazwy obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="cd63c-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd63c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd63c-104">SYNTAX</span></span>

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd63c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cd63c-105">DESCRIPTION</span></span>
<span data-ttu-id="cd63c-106">Polecenie cmdlet **test-AzureRmRelayName** sprawdza dostępność nazwy przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="cd63c-106">The **Test-AzureRmRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="cd63c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd63c-107">EXAMPLES</span></span>

### <span data-ttu-id="cd63c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cd63c-108">Example 1</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="cd63c-109">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cd63c-109">Example 2</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="cd63c-110">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="cd63c-110">Example 3</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="cd63c-111">Zwraca stan dostępności nazwy przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="cd63c-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="cd63c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd63c-112">PARAMETERS</span></span>

### <span data-ttu-id="cd63c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd63c-113">-DefaultProfile</span></span>
<span data-ttu-id="cd63c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd63c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd63c-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cd63c-115">-Namespace</span></span>
<span data-ttu-id="cd63c-116">Nazwa obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="cd63c-116">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd63c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd63c-117">CommonParameters</span></span>
<span data-ttu-id="cd63c-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd63c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cd63c-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd63c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd63c-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd63c-120">INPUTS</span></span>

### <span data-ttu-id="cd63c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="cd63c-121">System.String</span></span>


## <span data-ttu-id="cd63c-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd63c-122">OUTPUTS</span></span>

### <span data-ttu-id="cd63c-123">Microsoft. Azure. Commands. Relay. modele. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="cd63c-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>


## <span data-ttu-id="cd63c-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd63c-124">NOTES</span></span>

## <span data-ttu-id="cd63c-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd63c-125">RELATED LINKS</span></span>

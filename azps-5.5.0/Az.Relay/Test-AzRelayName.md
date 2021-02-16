---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: 45c3e0a4271a5eb2527ff25b5858a3f5aa35dc0a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242642"
---
# <span data-ttu-id="d3e5a-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="d3e5a-101">Test-AzRelayName</span></span>

## <span data-ttu-id="d3e5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3e5a-102">SYNOPSIS</span></span>
<span data-ttu-id="d3e5a-103">Sprawdza dostępność danej nazwy NameSpace.</span><span class="sxs-lookup"><span data-stu-id="d3e5a-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="d3e5a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d3e5a-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3e5a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d3e5a-105">DESCRIPTION</span></span>
<span data-ttu-id="d3e5a-106">Polecenie **cmdlet Test-AzRelayName** — sprawdzanie dostępności nazwy NameSpace</span><span class="sxs-lookup"><span data-stu-id="d3e5a-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="d3e5a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d3e5a-107">EXAMPLES</span></span>

### <span data-ttu-id="d3e5a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d3e5a-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="d3e5a-109">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d3e5a-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="d3e5a-110">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d3e5a-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="d3e5a-111">Zwraca stan dostępności nazwy przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="d3e5a-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="d3e5a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3e5a-112">PARAMETERS</span></span>

### <span data-ttu-id="d3e5a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3e5a-113">-DefaultProfile</span></span>
<span data-ttu-id="d3e5a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3e5a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3e5a-115">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="d3e5a-115">-Namespace</span></span>
<span data-ttu-id="d3e5a-116">Nazwa przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="d3e5a-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="d3e5a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3e5a-117">CommonParameters</span></span>
<span data-ttu-id="d3e5a-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3e5a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3e5a-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3e5a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3e5a-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3e5a-120">INPUTS</span></span>

### <span data-ttu-id="d3e5a-121">System.String</span><span class="sxs-lookup"><span data-stu-id="d3e5a-121">System.String</span></span>

## <span data-ttu-id="d3e5a-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d3e5a-122">OUTPUTS</span></span>

### <span data-ttu-id="d3e5a-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="d3e5a-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="d3e5a-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d3e5a-124">NOTES</span></span>

## <span data-ttu-id="d3e5a-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3e5a-125">RELATED LINKS</span></span>

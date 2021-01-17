---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: 45c3e0a4271a5eb2527ff25b5858a3f5aa35dc0a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378016"
---
# <span data-ttu-id="58794-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="58794-101">Test-AzRelayName</span></span>

## <span data-ttu-id="58794-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58794-102">SYNOPSIS</span></span>
<span data-ttu-id="58794-103">Sprawdza dostępność danej nazwy obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="58794-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="58794-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58794-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58794-105">Opis</span><span class="sxs-lookup"><span data-stu-id="58794-105">DESCRIPTION</span></span>
<span data-ttu-id="58794-106">Polecenie cmdlet **test-AzRelayName** sprawdza dostępność nazwy przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="58794-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="58794-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58794-107">EXAMPLES</span></span>

### <span data-ttu-id="58794-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="58794-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="58794-109">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="58794-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="58794-110">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="58794-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="58794-111">Zwraca stan dostępności nazwy przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="58794-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="58794-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58794-112">PARAMETERS</span></span>

### <span data-ttu-id="58794-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58794-113">-DefaultProfile</span></span>
<span data-ttu-id="58794-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="58794-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58794-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="58794-115">-Namespace</span></span>
<span data-ttu-id="58794-116">Nazwa obszaru nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="58794-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="58794-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58794-117">CommonParameters</span></span>
<span data-ttu-id="58794-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58794-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58794-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58794-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58794-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58794-120">INPUTS</span></span>

### <span data-ttu-id="58794-121">System. String</span><span class="sxs-lookup"><span data-stu-id="58794-121">System.String</span></span>

## <span data-ttu-id="58794-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58794-122">OUTPUTS</span></span>

### <span data-ttu-id="58794-123">Microsoft. Azure. Commands. Relay. modele. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="58794-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="58794-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58794-124">NOTES</span></span>

## <span data-ttu-id="58794-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58794-125">RELATED LINKS</span></span>

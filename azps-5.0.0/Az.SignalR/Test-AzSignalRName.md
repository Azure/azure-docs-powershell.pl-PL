---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: b00a408df2fe1705309152a02484d3b18ea41e9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317545"
---
# <span data-ttu-id="9f305-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="9f305-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="9f305-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9f305-102">SYNOPSIS</span></span>
<span data-ttu-id="9f305-103">Sprawdź dostępność nazwy.</span><span class="sxs-lookup"><span data-stu-id="9f305-103">Check the availability of a name.</span></span> <span data-ttu-id="9f305-104">Alias: test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="9f305-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="9f305-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9f305-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f305-106">Opis</span><span class="sxs-lookup"><span data-stu-id="9f305-106">DESCRIPTION</span></span>
<span data-ttu-id="9f305-107">Sprawdź dostępność nazwy.</span><span class="sxs-lookup"><span data-stu-id="9f305-107">Check the availability of a name.</span></span> <span data-ttu-id="9f305-108">Alias: test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="9f305-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="9f305-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9f305-109">EXAMPLES</span></span>

### <span data-ttu-id="9f305-110">Sprawdź istniejące imię i nazwisko.</span><span class="sxs-lookup"><span data-stu-id="9f305-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="9f305-111">Sprawdzanie nazwy nieistniejącej.</span><span class="sxs-lookup"><span data-stu-id="9f305-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="9f305-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9f305-112">PARAMETERS</span></span>

### <span data-ttu-id="9f305-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f305-113">-DefaultProfile</span></span>
<span data-ttu-id="9f305-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9f305-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f305-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9f305-115">-Location</span></span>
<span data-ttu-id="9f305-116">Lokalizacja usługi sygnalizacji.</span><span class="sxs-lookup"><span data-stu-id="9f305-116">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f305-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9f305-117">-Name</span></span>
<span data-ttu-id="9f305-118">Nazwa usługi sygnalizującego.</span><span class="sxs-lookup"><span data-stu-id="9f305-118">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f305-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f305-119">CommonParameters</span></span>
<span data-ttu-id="9f305-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f305-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f305-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f305-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f305-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f305-122">INPUTS</span></span>

### <span data-ttu-id="9f305-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9f305-123">System.String</span></span>

## <span data-ttu-id="9f305-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9f305-124">OUTPUTS</span></span>

### <span data-ttu-id="9f305-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9f305-125">System.Boolean</span></span>

## <span data-ttu-id="9f305-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9f305-126">NOTES</span></span>

## <span data-ttu-id="9f305-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9f305-127">RELATED LINKS</span></span>

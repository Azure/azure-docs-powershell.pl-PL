---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclustername
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
ms.openlocfilehash: c6b2f462ac66ab48b50e7555a3b5bf7c844aae3a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050081"
---
# <span data-ttu-id="df863-101">Test-AzKustoClusterName</span><span class="sxs-lookup"><span data-stu-id="df863-101">Test-AzKustoClusterName</span></span>

## <span data-ttu-id="df863-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df863-102">SYNOPSIS</span></span>
<span data-ttu-id="df863-103">Sprawdź, czy podana nazwa klastra Kusto jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="df863-103">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="df863-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df863-104">SYNTAX</span></span>

```
Test-AzKustoClusterName -Location <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df863-105">Opis</span><span class="sxs-lookup"><span data-stu-id="df863-105">DESCRIPTION</span></span>
<span data-ttu-id="df863-106">Sprawdź, czy podana nazwa klastra Kusto jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="df863-106">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="df863-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df863-107">EXAMPLES</span></span>

### <span data-ttu-id="df863-108">Przykład 1 — Sprawdź dostępność nazwy klastra usługi Kusto, która jest w użyciu</span><span class="sxs-lookup"><span data-stu-id="df863-108">Example 1 - Check the availability of a Kusto cluster name which is in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
False                   mykustocluster      Name 'mykustocluster' with type Engine is already taken. Please specify a different name
```

<span data-ttu-id="df863-109">Powyższe polecenie zwraca informację o tym, czy klaster usługi Kusto o nazwie "mykustocluster" istnieje w regionie "centralny stan".</span><span class="sxs-lookup"><span data-stu-id="df863-109">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

### <span data-ttu-id="df863-110">Przykład 2 — Sprawdzanie dostępności nazwy klastra Kusto, która nie jest używana</span><span class="sxs-lookup"><span data-stu-id="df863-110">Example 2 - Check the availability of a Kusto cluster name which is not in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
 True                   mykustocluster
```

<span data-ttu-id="df863-111">Powyższe polecenie zwraca informację o tym, czy klaster usługi Kusto o nazwie "mykustocluster" istnieje w regionie "centralny stan".</span><span class="sxs-lookup"><span data-stu-id="df863-111">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

## <span data-ttu-id="df863-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df863-112">PARAMETERS</span></span>

### <span data-ttu-id="df863-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df863-113">-DefaultProfile</span></span>
<span data-ttu-id="df863-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df863-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df863-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="df863-115">-Location</span></span>
<span data-ttu-id="df863-116">Lokalizacja, w której ma zostać sprawdzona.</span><span class="sxs-lookup"><span data-stu-id="df863-116">The location where to check.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df863-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="df863-117">-Name</span></span>
<span data-ttu-id="df863-118">Nazwa określonego klastra.</span><span class="sxs-lookup"><span data-stu-id="df863-118">Name of a specific cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df863-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df863-119">CommonParameters</span></span>
<span data-ttu-id="df863-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df863-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df863-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df863-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df863-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df863-122">INPUTS</span></span>

### <span data-ttu-id="df863-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="df863-123">None</span></span>

## <span data-ttu-id="df863-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df863-124">OUTPUTS</span></span>

### <span data-ttu-id="df863-125">Microsoft. Azure. Commands. Kusto. models. PSKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="df863-125">Microsoft.Azure.Commands.Kusto.Models.PSKustoClusterNameAvailability</span></span>

## <span data-ttu-id="df863-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df863-126">NOTES</span></span>

## <span data-ttu-id="df863-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df863-127">RELATED LINKS</span></span>

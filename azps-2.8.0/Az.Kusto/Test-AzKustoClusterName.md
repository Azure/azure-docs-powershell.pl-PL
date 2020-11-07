---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclustername
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
ms.openlocfilehash: 9a3d8397914317d733c8da47e7d095e1acb541e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705070"
---
# <span data-ttu-id="0c2fe-101">Test-AzKustoClusterName</span><span class="sxs-lookup"><span data-stu-id="0c2fe-101">Test-AzKustoClusterName</span></span>

## <span data-ttu-id="0c2fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c2fe-102">SYNOPSIS</span></span>
<span data-ttu-id="0c2fe-103">Sprawdź, czy podana nazwa klastra Kusto jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="0c2fe-103">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="0c2fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c2fe-104">SYNTAX</span></span>

```
Test-AzKustoClusterName -Location <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c2fe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0c2fe-105">DESCRIPTION</span></span>
<span data-ttu-id="0c2fe-106">Sprawdź, czy podana nazwa klastra Kusto jest dostępna.</span><span class="sxs-lookup"><span data-stu-id="0c2fe-106">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="0c2fe-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c2fe-107">EXAMPLES</span></span>

### <span data-ttu-id="0c2fe-108">Przykład 1 — Sprawdź dostępność nazwy klastra usługi Kusto, która jest w użyciu</span><span class="sxs-lookup"><span data-stu-id="0c2fe-108">Example 1 - Check the availability of a Kusto cluster name which is in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
False                   mykustocluster      Name 'mykustocluster' with type Engine is already taken. Please specify a different name
```

<span data-ttu-id="0c2fe-109">Powyższe polecenie zwraca informację o tym, czy klaster usługi Kusto o nazwie "mykustocluster" istnieje w regionie "centralny stan".</span><span class="sxs-lookup"><span data-stu-id="0c2fe-109">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

### <span data-ttu-id="0c2fe-110">Przykład 2 — Sprawdzanie dostępności nazwy klastra Kusto, która nie jest używana</span><span class="sxs-lookup"><span data-stu-id="0c2fe-110">Example 2 - Check the availability of a Kusto cluster name which is not in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
 True                   mykustocluster
```

<span data-ttu-id="0c2fe-111">Powyższe polecenie zwraca informację o tym, czy klaster usługi Kusto o nazwie "mykustocluster" istnieje w regionie "centralny stan".</span><span class="sxs-lookup"><span data-stu-id="0c2fe-111">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

## <span data-ttu-id="0c2fe-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c2fe-112">PARAMETERS</span></span>

### <span data-ttu-id="0c2fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c2fe-113">-DefaultProfile</span></span>
<span data-ttu-id="0c2fe-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c2fe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c2fe-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0c2fe-115">-Location</span></span>
<span data-ttu-id="0c2fe-116">Lokalizacja, w której ma zostać sprawdzona.</span><span class="sxs-lookup"><span data-stu-id="0c2fe-116">The location where to check.</span></span>

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

### <span data-ttu-id="0c2fe-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0c2fe-117">-Name</span></span>
<span data-ttu-id="0c2fe-118">Nazwa określonego klastra.</span><span class="sxs-lookup"><span data-stu-id="0c2fe-118">Name of a specific cluster.</span></span>

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

### <span data-ttu-id="0c2fe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c2fe-119">CommonParameters</span></span>
<span data-ttu-id="0c2fe-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c2fe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c2fe-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c2fe-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c2fe-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c2fe-122">INPUTS</span></span>

### <span data-ttu-id="0c2fe-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0c2fe-123">None</span></span>

## <span data-ttu-id="0c2fe-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c2fe-124">OUTPUTS</span></span>

### <span data-ttu-id="0c2fe-125">Microsoft. Azure. Commands. Kusto. models. PSKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="0c2fe-125">Microsoft.Azure.Commands.Kusto.Models.PSKustoClusterNameAvailability</span></span>

## <span data-ttu-id="0c2fe-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c2fe-126">NOTES</span></span>

## <span data-ttu-id="0c2fe-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c2fe-127">RELATED LINKS</span></span>

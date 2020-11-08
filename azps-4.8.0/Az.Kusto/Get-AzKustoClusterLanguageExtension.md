---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: f33d644e9726d09f9f2314e74a6b5fb80b788952
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064439"
---
# <span data-ttu-id="51dc7-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="51dc7-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="51dc7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="51dc7-103">Zwraca listę rozszerzeń języków, które mogą być uruchamiane w ramach zapytań programu Keyword.</span><span class="sxs-lookup"><span data-stu-id="51dc7-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="51dc7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51dc7-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="51dc7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="51dc7-105">DESCRIPTION</span></span>
<span data-ttu-id="51dc7-106">Zwraca listę rozszerzeń języków, które mogą być uruchamiane w ramach zapytań programu Keyword.</span><span class="sxs-lookup"><span data-stu-id="51dc7-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="51dc7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51dc7-107">EXAMPLES</span></span>

### <span data-ttu-id="51dc7-108">Przykład 1: Lista wszystkich rozszerzeń językowych ustawionych dla klastra</span><span class="sxs-lookup"><span data-stu-id="51dc7-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="51dc7-109">Powyższe polecenie zwraca listę rozszerzeń języków, które mogą być uruchamiane w ramach zapytań programu Keyword.</span><span class="sxs-lookup"><span data-stu-id="51dc7-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="51dc7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51dc7-110">PARAMETERS</span></span>

### <span data-ttu-id="51dc7-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="51dc7-111">-ClusterName</span></span>
<span data-ttu-id="51dc7-112">Nazwa klastra usługi Kusto.</span><span class="sxs-lookup"><span data-stu-id="51dc7-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="51dc7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51dc7-113">-DefaultProfile</span></span>
<span data-ttu-id="51dc7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="51dc7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51dc7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51dc7-115">-ResourceGroupName</span></span>
<span data-ttu-id="51dc7-116">Nazwa grupy zasobów zawierającej klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="51dc7-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="51dc7-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="51dc7-117">-SubscriptionId</span></span>
<span data-ttu-id="51dc7-118">Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="51dc7-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="51dc7-119">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="51dc7-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51dc7-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="51dc7-120">-Confirm</span></span>
<span data-ttu-id="51dc7-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51dc7-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51dc7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51dc7-122">-WhatIf</span></span>
<span data-ttu-id="51dc7-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51dc7-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51dc7-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="51dc7-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51dc7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51dc7-125">CommonParameters</span></span>
<span data-ttu-id="51dc7-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51dc7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51dc7-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51dc7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51dc7-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51dc7-128">INPUTS</span></span>

## <span data-ttu-id="51dc7-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51dc7-129">OUTPUTS</span></span>

### <span data-ttu-id="51dc7-130">Microsoft. Azure. PowerShell. polecenia. Kusto. models. Api20200614. ILanguageExtension</span><span class="sxs-lookup"><span data-stu-id="51dc7-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension</span></span>

## <span data-ttu-id="51dc7-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51dc7-131">NOTES</span></span>

<span data-ttu-id="51dc7-132">PISUJE</span><span class="sxs-lookup"><span data-stu-id="51dc7-132">ALIASES</span></span>

## <span data-ttu-id="51dc7-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51dc7-133">RELATED LINKS</span></span>


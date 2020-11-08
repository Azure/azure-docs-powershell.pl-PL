---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: 9c18597da52900794e5f891fb06385249c173a0b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050098"
---
# <span data-ttu-id="326a7-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="326a7-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="326a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="326a7-102">SYNOPSIS</span></span>
<span data-ttu-id="326a7-103">Tworzy nowy klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="326a7-103">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="326a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="326a7-104">SYNTAX</span></span>

```
New-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-Tier <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="326a7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="326a7-105">DESCRIPTION</span></span>
<span data-ttu-id="326a7-106">Tworzy nowy klaster Kusto.</span><span class="sxs-lookup"><span data-stu-id="326a7-106">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="326a7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="326a7-107">EXAMPLES</span></span>

### <span data-ttu-id="326a7-108">Przykład 1-Tworzenie nowego klastra Kusto</span><span class="sxs-lookup"><span data-stu-id="326a7-108">Example 1 - Create a new Kusto cluster</span></span>

```
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster -Location 'Central US' -Sku D13_v2 -Capacity 10

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 10
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="326a7-109">Powyższe polecenie tworzy nowy klaster Kusto o nazwie "mykustocluster" w grupie zasobów "testrg".</span><span class="sxs-lookup"><span data-stu-id="326a7-109">The above command creates a new Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="326a7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="326a7-110">PARAMETERS</span></span>

### <span data-ttu-id="326a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="326a7-111">-DefaultProfile</span></span>
<span data-ttu-id="326a7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="326a7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="326a7-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="326a7-113">-Location</span></span>
<span data-ttu-id="326a7-114">Obszar platformy Azure, w którym ma zostać utworzony klaster.</span><span class="sxs-lookup"><span data-stu-id="326a7-114">Azure region where the cluster should be created.</span></span>

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

### <span data-ttu-id="326a7-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="326a7-115">-Name</span></span>
<span data-ttu-id="326a7-116">Nazwa klastra do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="326a7-116">Name of the cluster to be created.</span></span>

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

### <span data-ttu-id="326a7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="326a7-117">-ResourceGroupName</span></span>
<span data-ttu-id="326a7-118">Nazwa grupy zasobów, w której ma zostać utworzony klaster.</span><span class="sxs-lookup"><span data-stu-id="326a7-118">Name of resource group under which you want to create the cluster.</span></span>

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

### <span data-ttu-id="326a7-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="326a7-119">-Sku</span></span>
<span data-ttu-id="326a7-120">Nazwa jednostki SKU użytej do utworzenia klastra</span><span class="sxs-lookup"><span data-stu-id="326a7-120">Name of the Sku used to create the cluster</span></span>

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

### <span data-ttu-id="326a7-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="326a7-121">-Tag</span></span>
<span data-ttu-id="326a7-122">Ciąg znaków, który jest ciągiem znaczników skojarzonych z tym klastrem</span><span class="sxs-lookup"><span data-stu-id="326a7-122">A string,string dictionary of tags associated with this cluster</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="326a7-123">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="326a7-123">-Tier</span></span>
<span data-ttu-id="326a7-124">Nazwa warstwy użytej do utworzenia klastra</span><span class="sxs-lookup"><span data-stu-id="326a7-124">Name of the Tier used to create the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="326a7-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="326a7-125">-Confirm</span></span>
<span data-ttu-id="326a7-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="326a7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="326a7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="326a7-127">-WhatIf</span></span>
<span data-ttu-id="326a7-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="326a7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="326a7-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="326a7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="326a7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="326a7-130">CommonParameters</span></span>
<span data-ttu-id="326a7-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="326a7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="326a7-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="326a7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="326a7-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="326a7-133">INPUTS</span></span>

### <span data-ttu-id="326a7-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="326a7-134">None</span></span>

## <span data-ttu-id="326a7-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="326a7-135">OUTPUTS</span></span>

### <span data-ttu-id="326a7-136">Microsoft. Azure. Commands. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="326a7-136">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="326a7-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="326a7-137">NOTES</span></span>

## <span data-ttu-id="326a7-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="326a7-138">RELATED LINKS</span></span>

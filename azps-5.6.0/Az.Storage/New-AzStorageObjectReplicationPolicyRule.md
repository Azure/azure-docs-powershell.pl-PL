---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: 8338f13829ebc3feff4c5a81fdfb3bd13934d90d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002442"
---
# <span data-ttu-id="6fcd5-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="6fcd5-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="6fcd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fcd5-102">SYNOPSIS</span></span>
<span data-ttu-id="6fcd5-103">Tworzy regułę zasad replikacji obiektów.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="6fcd5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6fcd5-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fcd5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6fcd5-105">DESCRIPTION</span></span>
<span data-ttu-id="6fcd5-106">Polecenie **cmdlet Get-AzStorageObjectReplicationPolicy** tworzy regułę zasad replikacji obiektów, która będzie używana w Set-AzStorageObjectReplicationPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="6fcd5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6fcd5-107">EXAMPLES</span></span>

### <span data-ttu-id="6fcd5-108">Przykład 1. Tworzenie reguły zasad replikacji obiektu tylko przy użyciu konta źródłowego i docelowego oraz wyświetlanie jego właściwości</span><span class="sxs-lookup"><span data-stu-id="6fcd5-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="6fcd5-109">To polecenie tworzy regułę zasad replikacji obiektów tylko z kontem źródłowym i docelowym oraz wyświetla jej właściwości.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="6fcd5-110">Przykład 2. Tworzenie reguły zasad replikacji obiektu ze wszystkimi właściwościami i wyświetlanie jej właściwości</span><span class="sxs-lookup"><span data-stu-id="6fcd5-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="6fcd5-111">To polecenie reguły zasad replikacji obiektu ze wszystkimi właściwościami i pokazanie jej właściwości.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="6fcd5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fcd5-112">PARAMETERS</span></span>

### <span data-ttu-id="6fcd5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fcd5-113">-DefaultProfile</span></span>
<span data-ttu-id="6fcd5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fcd5-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="6fcd5-115">-DestinationContainer</span></span>
<span data-ttu-id="6fcd5-116">Nazwa kontenera docelowego, do którego chcesz zreplikować dane.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-116">The Destination Container name to replicate to.</span></span>

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

### <span data-ttu-id="6fcd5-117">— MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="6fcd5-117">-MinCreationTime</span></span>
<span data-ttu-id="6fcd5-118">Obiekty blob utworzone po upływie tego czasu zostaną zreplikowane do miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-118">Blobs created after the time will be replicated to the destination..</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fcd5-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="6fcd5-119">-PrefixMatch</span></span>
<span data-ttu-id="6fcd5-120">Filtruje wyniki w celu replikowania tylko obiektów blob, których nazwy zaczynają się od określonego prefiksu.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fcd5-121">-RuleId</span><span class="sxs-lookup"><span data-stu-id="6fcd5-121">-RuleId</span></span>
<span data-ttu-id="6fcd5-122">Identyfikator reguły replikacji obiektu.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-122">Object Replication Rule Id.</span></span>

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

### <span data-ttu-id="6fcd5-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="6fcd5-123">-SourceContainer</span></span>
<span data-ttu-id="6fcd5-124">Nazwa kontenera źródłowego, z których ma być replikowana.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-124">The Source Container name to replicate from.</span></span>

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

### <span data-ttu-id="6fcd5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fcd5-125">CommonParameters</span></span>
<span data-ttu-id="6fcd5-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fcd5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fcd5-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fcd5-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fcd5-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fcd5-128">INPUTS</span></span>

### <span data-ttu-id="6fcd5-129">Brak</span><span class="sxs-lookup"><span data-stu-id="6fcd5-129">None</span></span>

## <span data-ttu-id="6fcd5-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fcd5-130">OUTPUTS</span></span>

### <span data-ttu-id="6fcd5-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="6fcd5-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="6fcd5-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6fcd5-132">NOTES</span></span>

## <span data-ttu-id="6fcd5-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fcd5-133">RELATED LINKS</span></span>

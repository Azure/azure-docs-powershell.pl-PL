---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: c8d41300250e41548cf949248b02c819b7da497f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190842"
---
# <span data-ttu-id="a1a6f-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a1a6f-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="a1a6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1a6f-102">SYNOPSIS</span></span>
<span data-ttu-id="a1a6f-103">Tworzy regułę zasad replikacji obiektów.</span><span class="sxs-lookup"><span data-stu-id="a1a6f-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="a1a6f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a1a6f-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1a6f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a1a6f-105">DESCRIPTION</span></span>
<span data-ttu-id="a1a6f-106">Polecenie **cmdlet Get-AzStorageObjectReplicationPolicy** tworzy regułę zasad replikacji obiektów, która będzie używana w Set-AzStorageObjectReplicationPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1a6f-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="a1a6f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a1a6f-107">EXAMPLES</span></span>

### <span data-ttu-id="a1a6f-108">Przykład 1. Tworzenie reguły zasad replikacji obiektu tylko z kontem źródłowym i docelowym oraz wyświetlanie jej właściwości</span><span class="sxs-lookup"><span data-stu-id="a1a6f-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="a1a6f-109">To polecenie tworzy regułę zasad replikacji obiektów tylko z kontem źródłowym i docelowym oraz wyświetla jej właściwości.</span><span class="sxs-lookup"><span data-stu-id="a1a6f-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="a1a6f-110">Przykład 2. Tworzenie reguły zasad replikacji obiektu ze wszystkimi właściwościami i wyświetlanie jej właściwości</span><span class="sxs-lookup"><span data-stu-id="a1a6f-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="a1a6f-111">To polecenie reguły zasad replikacji obiektu ze wszystkimi właściwościami i wyświetlanie jej właściwości.</span><span class="sxs-lookup"><span data-stu-id="a1a6f-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="a1a6f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1a6f-112">PARAMETERS</span></span>

### <span data-ttu-id="a1a6f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1a6f-113">-DefaultProfile</span></span>
<span data-ttu-id="a1a6f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1a6f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1a6f-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="a1a6f-115">-DestinationContainer</span></span>
<span data-ttu-id="a1a6f-116">Nazwa kontenera docelowego, do którego ma być replikowana.</span><span class="sxs-lookup"><span data-stu-id="a1a6f-116">The Destination Container name to replicate to.</span></span>

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

### <span data-ttu-id="a1a6f-117">— MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="a1a6f-117">-MinCreationTime</span></span>
<span data-ttu-id="a1a6f-118">Obiekty blob utworzone po upływie tego czasu zostaną zreplikowane do miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="a1a6f-118">Blobs created after the time will be replicated to the destination..</span></span>

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

### <span data-ttu-id="a1a6f-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="a1a6f-119">-PrefixMatch</span></span>
<span data-ttu-id="a1a6f-120">Filtruje wyniki w celu replikowania tylko obiektów blob, których nazwy zaczynają się od określonego prefiksu.</span><span class="sxs-lookup"><span data-stu-id="a1a6f-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

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

### <span data-ttu-id="a1a6f-121">-RuleId</span><span class="sxs-lookup"><span data-stu-id="a1a6f-121">-RuleId</span></span>
<span data-ttu-id="a1a6f-122">Identyfikator reguły replikacji obiektu.</span><span class="sxs-lookup"><span data-stu-id="a1a6f-122">Object Replication Rule Id.</span></span>

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

### <span data-ttu-id="a1a6f-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="a1a6f-123">-SourceContainer</span></span>
<span data-ttu-id="a1a6f-124">Nazwa kontenera źródłowego, z których ma być replikowana.</span><span class="sxs-lookup"><span data-stu-id="a1a6f-124">The Source Container name to replicate from.</span></span>

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

### <span data-ttu-id="a1a6f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1a6f-125">CommonParameters</span></span>
<span data-ttu-id="a1a6f-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1a6f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1a6f-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1a6f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1a6f-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1a6f-128">INPUTS</span></span>

### <span data-ttu-id="a1a6f-129">Brak</span><span class="sxs-lookup"><span data-stu-id="a1a6f-129">None</span></span>

## <span data-ttu-id="a1a6f-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1a6f-130">OUTPUTS</span></span>

### <span data-ttu-id="a1a6f-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a1a6f-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="a1a6f-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a1a6f-132">NOTES</span></span>

## <span data-ttu-id="a1a6f-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1a6f-133">RELATED LINKS</span></span>

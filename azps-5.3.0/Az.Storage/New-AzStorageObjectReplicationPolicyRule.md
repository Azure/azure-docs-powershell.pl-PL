---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: c8d41300250e41548cf949248b02c819b7da497f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491333"
---
# <span data-ttu-id="b0bc1-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="b0bc1-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="b0bc1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b0bc1-102">SYNOPSIS</span></span>
<span data-ttu-id="b0bc1-103">Tworzenie reguły zasad replikacji obiektów.</span><span class="sxs-lookup"><span data-stu-id="b0bc1-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="b0bc1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b0bc1-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0bc1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b0bc1-105">DESCRIPTION</span></span>
<span data-ttu-id="b0bc1-106">Polecenie cmdlet **Get-AzStorageObjectReplicationPolicy** umożliwia utworzenie reguły zasad replikacji obiektów, która będzie używana w Set-AzStorageObjectReplicationPolicy polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0bc1-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="b0bc1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b0bc1-107">EXAMPLES</span></span>

### <span data-ttu-id="b0bc1-108">Przykład 1: Tworzenie reguły replikacji obiektów tylko dla konta źródłowego i docelowego oraz wyświetlanie jego właściwości</span><span class="sxs-lookup"><span data-stu-id="b0bc1-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="b0bc1-109">To polecenie tworzy regułę replikacji obiektów z tylko kontem źródłowym i docelowym oraz wyświetla jego właściwości.</span><span class="sxs-lookup"><span data-stu-id="b0bc1-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="b0bc1-110">Przykład 2: Tworzenie reguły replikacji obiektów ze wszystkimi właściwościami i wyświetlanie jej właściwości</span><span class="sxs-lookup"><span data-stu-id="b0bc1-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="b0bc1-111">To polecenie ma regułę zasad replikacji obiektu ze wszystkimi właściwościami i przedstawia jej właściwości.</span><span class="sxs-lookup"><span data-stu-id="b0bc1-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="b0bc1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b0bc1-112">PARAMETERS</span></span>

### <span data-ttu-id="b0bc1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0bc1-113">-DefaultProfile</span></span>
<span data-ttu-id="b0bc1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0bc1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0bc1-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="b0bc1-115">-DestinationContainer</span></span>
<span data-ttu-id="b0bc1-116">Nazwa kontenera docelowego, na który mają być replikowane dane.</span><span class="sxs-lookup"><span data-stu-id="b0bc1-116">The Destination Container name to replicate to.</span></span>

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

### <span data-ttu-id="b0bc1-117">-MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="b0bc1-117">-MinCreationTime</span></span>
<span data-ttu-id="b0bc1-118">Obiekty blob utworzone po upływie tego czasu będą replikowane do miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="b0bc1-118">Blobs created after the time will be replicated to the destination..</span></span>

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

### <span data-ttu-id="b0bc1-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="b0bc1-119">-PrefixMatch</span></span>
<span data-ttu-id="b0bc1-120">Filtruje wyniki, aby zreplikować tylko obiekty blob, których nazwy zaczynają się od określonego prefiksu.</span><span class="sxs-lookup"><span data-stu-id="b0bc1-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

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

### <span data-ttu-id="b0bc1-121">-RuleId</span><span class="sxs-lookup"><span data-stu-id="b0bc1-121">-RuleId</span></span>
<span data-ttu-id="b0bc1-122">Identyfikator reguły replikacji obiektów.</span><span class="sxs-lookup"><span data-stu-id="b0bc1-122">Object Replication Rule Id.</span></span>

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

### <span data-ttu-id="b0bc1-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="b0bc1-123">-SourceContainer</span></span>
<span data-ttu-id="b0bc1-124">Źródłowa nazwa kontenera, z którego mają być replikowane dane.</span><span class="sxs-lookup"><span data-stu-id="b0bc1-124">The Source Container name to replicate from.</span></span>

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

### <span data-ttu-id="b0bc1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0bc1-125">CommonParameters</span></span>
<span data-ttu-id="b0bc1-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0bc1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0bc1-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0bc1-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0bc1-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0bc1-128">INPUTS</span></span>

### <span data-ttu-id="b0bc1-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b0bc1-129">None</span></span>

## <span data-ttu-id="b0bc1-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b0bc1-130">OUTPUTS</span></span>

### <span data-ttu-id="b0bc1-131">Microsoft. Azure. Commands. Management. Storage. models. PSObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="b0bc1-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="b0bc1-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b0bc1-132">NOTES</span></span>

## <span data-ttu-id="b0bc1-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0bc1-133">RELATED LINKS</span></span>

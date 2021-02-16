---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 6785eac6df5568f4b26e6de61ac0f4bfd8061259
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201322"
---
# <span data-ttu-id="21074-101">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="21074-101">Get-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="21074-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21074-102">SYNOPSIS</span></span>
<span data-ttu-id="21074-103">Pobiera lub wyświetla zasady replikacji obiektów konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="21074-103">Gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="21074-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="21074-104">SYNTAX</span></span>

### <span data-ttu-id="21074-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="21074-105">AccountName (Default)</span></span>
```
Get-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21074-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="21074-106">AccountObject</span></span>
```
Get-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21074-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="21074-107">DESCRIPTION</span></span>
<span data-ttu-id="21074-108">Polecenie **cmdlet Get-AzStorageObjectReplicationPolicy** pobiera lub wyświetla zasady replikacji obiektów konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="21074-108">The **Get-AzStorageObjectReplicationPolicy** cmdlet gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="21074-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="21074-109">EXAMPLES</span></span>

### <span data-ttu-id="21074-110">Przykład 1. Pobierz zasady replikacji obiektu z określonym identyfikatorem zasad i pokaż jego reguły.</span><span class="sxs-lookup"><span data-stu-id="21074-110">Example 1: Get an object replication policy with specific policy Id and show its rules.</span></span>
```
PS C:\> $policy = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" -PolicyId 56bfa11c-81ef-4f8d-b307-5e5386e16fba

PS C:\> $policy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]

PS C:\> $policy.Rules

RuleId                               SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------                               --------------- -------------------- ------------------- -----------------------
d3d39a01-8d92-40e5-849f-e56209ae5cf5 src1            dest1                {}                                         
2407de9a-3301-4656-858f-359d185565e0 src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="21074-111">To polecenie pobiera zasady replikacji obiektów z określonym identyfikatorem zasad i wyświetla jego reguły.</span><span class="sxs-lookup"><span data-stu-id="21074-111">This command gets an object replication policy with specific policy Id and show its rules.</span></span>

### <span data-ttu-id="21074-112">Przykład 2.Lista zasad replikacji obiektów z konta magazynu</span><span class="sxs-lookup"><span data-stu-id="21074-112">Example 2:List object replication policy from a Storage account</span></span>
```
PS C:\> $policies = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" 

PS C:\> $policies

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysrcaccount1   mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
myresourcegroup   mydestaccount      68434c7a-20d0-4282-b75c-43b5a243435e             mysrcaccount2   mydestaccount      [d3d39a01-8d92-40e5-849f-e56209ae5cf5,...]
```

<span data-ttu-id="21074-113">To polecenie zawiera listę zasad replikacji obiektów z konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="21074-113">This command lists object replication policy from a Storage account.</span></span>

## <span data-ttu-id="21074-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21074-114">PARAMETERS</span></span>

### <span data-ttu-id="21074-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21074-115">-DefaultProfile</span></span>
<span data-ttu-id="21074-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="21074-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21074-117">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="21074-117">-PolicyId</span></span>
<span data-ttu-id="21074-118">Identyfikator zasad replikacji obiektów.</span><span class="sxs-lookup"><span data-stu-id="21074-118">Object Replication Policy Id.</span></span>

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

### <span data-ttu-id="21074-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21074-119">-ResourceGroupName</span></span>
<span data-ttu-id="21074-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="21074-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21074-121">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="21074-121">-StorageAccount</span></span>
<span data-ttu-id="21074-122">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="21074-122">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21074-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="21074-123">-StorageAccountName</span></span>
<span data-ttu-id="21074-124">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="21074-124">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21074-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21074-125">CommonParameters</span></span>
<span data-ttu-id="21074-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21074-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21074-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21074-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21074-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21074-128">INPUTS</span></span>

### <span data-ttu-id="21074-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="21074-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="21074-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21074-130">OUTPUTS</span></span>

### <span data-ttu-id="21074-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="21074-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="21074-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="21074-132">NOTES</span></span>

## <span data-ttu-id="21074-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21074-133">RELATED LINKS</span></span>

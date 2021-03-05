---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: 65bce04c3df14a6b9dc4397d47577d0642746c45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976186"
---
# <span data-ttu-id="6433b-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="6433b-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="6433b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6433b-102">SYNOPSIS</span></span>
<span data-ttu-id="6433b-103">Dodaje akcję do obiektu wejściowego Grupa akcji ManagementPolicy lub tworzy obiekt grupy akcji ManagementPolicy wraz z akcją.</span><span class="sxs-lookup"><span data-stu-id="6433b-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="6433b-104">Ten obiekt może być używany w programie New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="6433b-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="6433b-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6433b-105">SYNTAX</span></span>

### <span data-ttu-id="6433b-106">BaseBlob (domyślne)</span><span class="sxs-lookup"><span data-stu-id="6433b-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6433b-107">Migawka</span><span class="sxs-lookup"><span data-stu-id="6433b-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6433b-108">BlobVersion</span><span class="sxs-lookup"><span data-stu-id="6433b-108">BlobVersion</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BlobVersionAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6433b-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="6433b-109">DESCRIPTION</span></span>
<span data-ttu-id="6433b-110">Polecenie cmdlet **Add-AzStorageAccountManagementPolicyAction** dodaje akcję do obiektu wejściowego grupa akcji ManagementPolicy lub tworzy z akcją obiekt grupy akcji ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="6433b-110">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="6433b-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6433b-111">EXAMPLES</span></span>

### <span data-ttu-id="6433b-112">Przykład 1. Tworzy obiekt grupy akcji ManagementPolicy z 4 akcjami, a następnie dodaje go do reguły zasad zarządzania i ustawia na konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="6433b-112">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action
PS C:\>$action 

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 30
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 50
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 100
Snapshot.TierToCool.DaysAfterCreationGreaterThan        : 
Snapshot.TierToArchive.DaysAfterCreationGreaterThan     : 
Snapshot.Delete.DaysAfterCreationGreaterThan            : 100
Version.TierToCool.DaysAfterCreationGreaterThan         : 
Version.TierToArchive.DaysAfterCreationGreaterThan      : 
Version.Delete.DaysAfterCreationGreaterThan             : 

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="6433b-113">Pierwsze polecenie umożliwia utworzenie obiektu grupy akcji ManagementPolicy, a następujące 3 polecenia dodają do obiektu 3 akcje.</span><span class="sxs-lookup"><span data-stu-id="6433b-113">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="6433b-114">Następnie dodaj ją do reguły zasad zarządzania i ustaw jako konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="6433b-114">Then add it to a management policy rule and set to a Storage account.</span></span>

### <span data-ttu-id="6433b-115">Przykład 2. Tworzy obiekt grupy akcji ManagementPolicy z 6 akcjami w wersji migawki i obiektu blob, a następnie dodaj go do reguły zasad zarządzania i ustaw na konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="6433b-115">Example 2: Creates a ManagementPolicy Action Group object with 6 actions on snapshot and blob version, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction  -SnapshotAction Delete -daysAfterCreationGreaterThan 40
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -SnapshotAction TierToArchive -daysAfterCreationGreaterThan 50
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -SnapshotAction TierToCool -daysAfterCreationGreaterThan 60
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction Delete -daysAfterCreationGreaterThan 70
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction TierToArchive -daysAfterCreationGreaterThan 80
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction TierToCool -daysAfterCreationGreaterThan 90
PS C:\> $action

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 
Snapshot.TierToCool.DaysAfterCreationGreaterThan        : 60
Snapshot.TierToArchive.DaysAfterCreationGreaterThan     : 50
Snapshot.Delete.DaysAfterCreationGreaterThan            : 40
Version.TierToCool.DaysAfterCreationGreaterThan         : 90
Version.TierToArchive.DaysAfterCreationGreaterThan      : 80
Version.Delete.DaysAfterCreationGreaterThan             : 70

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="6433b-116">Pierwsze polecenie tworzy obiekt grupy akcji ManagementPolicy, a następujące 5 poleceń dodaje do obiektu 5 akcji w wersji migawki i obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="6433b-116">The first command create a ManagementPolicy Action Group object, the following 5 commands add 5 actions on snapshot and blob version to the object.</span></span> <span data-ttu-id="6433b-117">Następnie dodaj ją do reguły zasad zarządzania i ustaw jako konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="6433b-117">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="6433b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6433b-118">PARAMETERS</span></span>

### <span data-ttu-id="6433b-119">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="6433b-119">-BaseBlobAction</span></span>
<span data-ttu-id="6433b-120">Akcja zasad zarządzania dla bazy danych Baseblob.</span><span class="sxs-lookup"><span data-stu-id="6433b-120">The management policy action for baseblob.</span></span>

```yaml
Type: System.String
Parameter Sets: BaseBlob
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6433b-121">-BlobVersionAction</span><span class="sxs-lookup"><span data-stu-id="6433b-121">-BlobVersionAction</span></span>
<span data-ttu-id="6433b-122">Akcja zasad zarządzania dla wersji obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="6433b-122">The management policy action for blob version.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobVersion
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6433b-123">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="6433b-123">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="6433b-124">Wartość całkowita wskazująca wiek w dniach po utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="6433b-124">Integer value indicating the age in days after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Snapshot, BlobVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6433b-125">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="6433b-125">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="6433b-126">Wartość całkowita wskazująca wiek w dniach po ostatniej modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="6433b-126">Integer value indicating the age in days after last modification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: BaseBlob
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6433b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6433b-127">-DefaultProfile</span></span>
<span data-ttu-id="6433b-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6433b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6433b-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6433b-129">-InputObject</span></span>
<span data-ttu-id="6433b-130">Jeśli obiekt akcji ManagementPolicy zostanie wejściowy, ustawi akcję na obiekt akcji wprowadzania.</span><span class="sxs-lookup"><span data-stu-id="6433b-130">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="6433b-131">Jeśli nie zostanie on wejściowy, utworzy nowy obiekt akcji.</span><span class="sxs-lookup"><span data-stu-id="6433b-131">If not input, will create a new action object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6433b-132">-SnapshotAction</span><span class="sxs-lookup"><span data-stu-id="6433b-132">-SnapshotAction</span></span>
<span data-ttu-id="6433b-133">Akcja zasad zarządzania migawki.</span><span class="sxs-lookup"><span data-stu-id="6433b-133">The management policy action for snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: Snapshot
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6433b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6433b-134">CommonParameters</span></span>
<span data-ttu-id="6433b-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6433b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6433b-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6433b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6433b-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6433b-137">INPUTS</span></span>

### <span data-ttu-id="6433b-138">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="6433b-138">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="6433b-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6433b-139">OUTPUTS</span></span>

### <span data-ttu-id="6433b-140">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="6433b-140">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="6433b-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6433b-141">NOTES</span></span>

## <span data-ttu-id="6433b-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6433b-142">RELATED LINKS</span></span>

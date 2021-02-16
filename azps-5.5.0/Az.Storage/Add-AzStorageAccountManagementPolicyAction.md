---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: ed876765e3b5eb9d306847958772d9205758f5d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176659"
---
# <span data-ttu-id="3a95a-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="3a95a-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="3a95a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a95a-102">SYNOPSIS</span></span>
<span data-ttu-id="3a95a-103">Dodaje akcję do obiektu wejściowego Grupa akcji ManagementPolicy lub tworzy obiekt grupy akcji ManagementPolicy wraz z akcją.</span><span class="sxs-lookup"><span data-stu-id="3a95a-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="3a95a-104">Ten obiekt może być używany w programie New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="3a95a-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="3a95a-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3a95a-105">SYNTAX</span></span>

### <span data-ttu-id="3a95a-106">BaseBlob (domyślne)</span><span class="sxs-lookup"><span data-stu-id="3a95a-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a95a-107">Migawka</span><span class="sxs-lookup"><span data-stu-id="3a95a-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a95a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3a95a-108">DESCRIPTION</span></span>
<span data-ttu-id="3a95a-109">Polecenie cmdlet **Add-AzStorageAccountManagementPolicyAction** dodaje akcję do obiektu wejściowego grupa akcji ManagementPolicy lub tworzy obiekt grupy akcji ManagementPolicy wraz z akcją.</span><span class="sxs-lookup"><span data-stu-id="3a95a-109">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="3a95a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3a95a-110">EXAMPLES</span></span>

### <span data-ttu-id="3a95a-111">Przykład 1. Tworzy obiekt grupy akcji ManagementPolicy z 4 akcjami, a następnie dodaje go do reguły zasad zarządzania i ustawia na konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="3a95a-111">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action
PS C:\>$action 

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 30
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 50
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 100
Snapshot.Delete.DaysAfterCreationGreaterThan            : 100

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="3a95a-112">Pierwsze polecenie tworzy obiekt grupa akcji ManagementPolicy, a następujące 3 polecenia dodają do obiektu 3 akcje.</span><span class="sxs-lookup"><span data-stu-id="3a95a-112">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="3a95a-113">Następnie dodaj ją do reguły zasad zarządzania i ustaw jako konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="3a95a-113">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="3a95a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a95a-114">PARAMETERS</span></span>

### <span data-ttu-id="3a95a-115">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="3a95a-115">-BaseBlobAction</span></span>
<span data-ttu-id="3a95a-116">Akcja zasad zarządzania dla bazy danych Baseblob.</span><span class="sxs-lookup"><span data-stu-id="3a95a-116">The management policy action for baseblob.</span></span>

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

### <span data-ttu-id="3a95a-117">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="3a95a-117">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="3a95a-118">Wartość całkowita wskazująca wiek w dniach po utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="3a95a-118">Integer value indicating the age in days after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Snapshot
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a95a-119">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="3a95a-119">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="3a95a-120">Wartość całkowita wskazująca wiek w dniach po ostatniej modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="3a95a-120">Integer value indicating the age in days after last modification.</span></span>

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

### <span data-ttu-id="3a95a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a95a-121">-DefaultProfile</span></span>
<span data-ttu-id="3a95a-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a95a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a95a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a95a-123">-InputObject</span></span>
<span data-ttu-id="3a95a-124">Jeśli obiekt akcji ManagementPolicy zostanie wejściowy, ustawi akcję na obiekt akcji wprowadzania.</span><span class="sxs-lookup"><span data-stu-id="3a95a-124">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="3a95a-125">Jeśli nie zostanie on wejściowy, utworzy nowy obiekt akcji.</span><span class="sxs-lookup"><span data-stu-id="3a95a-125">If not input, will create a new action object.</span></span>

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

### <span data-ttu-id="3a95a-126">-SnapshotAction</span><span class="sxs-lookup"><span data-stu-id="3a95a-126">-SnapshotAction</span></span>
<span data-ttu-id="3a95a-127">Akcja zasad zarządzania migawki.</span><span class="sxs-lookup"><span data-stu-id="3a95a-127">The management policy action for snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: Snapshot
Aliases:
Accepted values: Delete

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a95a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a95a-128">CommonParameters</span></span>
<span data-ttu-id="3a95a-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a95a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a95a-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a95a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a95a-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a95a-131">INPUTS</span></span>

### <span data-ttu-id="3a95a-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="3a95a-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="3a95a-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a95a-133">OUTPUTS</span></span>

### <span data-ttu-id="3a95a-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="3a95a-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="3a95a-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3a95a-135">NOTES</span></span>

## <span data-ttu-id="3a95a-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a95a-136">RELATED LINKS</span></span>

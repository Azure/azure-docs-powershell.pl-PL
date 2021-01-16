---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: ed876765e3b5eb9d306847958772d9205758f5d6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374171"
---
# <span data-ttu-id="d60dc-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="d60dc-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="d60dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d60dc-102">SYNOPSIS</span></span>
<span data-ttu-id="d60dc-103">Umożliwia dodanie akcji do obiektu grupy akcji ManagementPolicy lub utworzenie obiektu grupy akcji ManagementPolicy z akcją.</span><span class="sxs-lookup"><span data-stu-id="d60dc-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="d60dc-104">Obiekt może być wykorzystywany w nowych — AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="d60dc-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="d60dc-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d60dc-105">SYNTAX</span></span>

### <span data-ttu-id="d60dc-106">BaseBlob (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d60dc-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d60dc-107">Zdjęcie</span><span class="sxs-lookup"><span data-stu-id="d60dc-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d60dc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d60dc-108">DESCRIPTION</span></span>
<span data-ttu-id="d60dc-109">Polecenie cmdlet **Add-AzStorageAccountManagementPolicyAction** umożliwia dodanie akcji do obiektu grupy akcji ManagementPolicy lub utworzenie obiektu grupy akcji ManagementPolicy z akcją.</span><span class="sxs-lookup"><span data-stu-id="d60dc-109">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="d60dc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d60dc-110">EXAMPLES</span></span>

### <span data-ttu-id="d60dc-111">Przykład 1: utworzenie obiektu grupy akcji ManagementPolicy z czterema akcjami, a następnie dodanie go do reguły zasad zarządzania i ustawieniem konta magazynu</span><span class="sxs-lookup"><span data-stu-id="d60dc-111">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
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

<span data-ttu-id="d60dc-112">Pierwsze polecenie Tworzenie obiektu grupy akcji ManagementPolicy, następujące 3 polecenia dodają 3 akcje do obiektu.</span><span class="sxs-lookup"><span data-stu-id="d60dc-112">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="d60dc-113">Następnie dodaj ją do reguły zasad zarządzania i Ustaw konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="d60dc-113">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="d60dc-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d60dc-114">PARAMETERS</span></span>

### <span data-ttu-id="d60dc-115">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="d60dc-115">-BaseBlobAction</span></span>
<span data-ttu-id="d60dc-116">Akcja zasady zarządzania dla baseblob.</span><span class="sxs-lookup"><span data-stu-id="d60dc-116">The management policy action for baseblob.</span></span>

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

### <span data-ttu-id="d60dc-117">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="d60dc-117">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="d60dc-118">Wartość całkowita określająca wiek w dniach od daty utworzenia.</span><span class="sxs-lookup"><span data-stu-id="d60dc-118">Integer value indicating the age in days after creation.</span></span>

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

### <span data-ttu-id="d60dc-119">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="d60dc-119">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="d60dc-120">Wartość całkowita oznaczająca wiek w dniach od ostatniej modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="d60dc-120">Integer value indicating the age in days after last modification.</span></span>

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

### <span data-ttu-id="d60dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d60dc-121">-DefaultProfile</span></span>
<span data-ttu-id="d60dc-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d60dc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d60dc-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d60dc-123">-InputObject</span></span>
<span data-ttu-id="d60dc-124">Jeśli wprowadzasz obiekt akcji ManagementPolicy, ustawisz akcję na obiekt akcja wejściowa.</span><span class="sxs-lookup"><span data-stu-id="d60dc-124">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="d60dc-125">Jeśli nie jest to dane, utworzy nowy obiekt Action.</span><span class="sxs-lookup"><span data-stu-id="d60dc-125">If not input, will create a new action object.</span></span>

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

### <span data-ttu-id="d60dc-126">-SnapshotAction</span><span class="sxs-lookup"><span data-stu-id="d60dc-126">-SnapshotAction</span></span>
<span data-ttu-id="d60dc-127">Akcja zasady zarządzania dla migawki.</span><span class="sxs-lookup"><span data-stu-id="d60dc-127">The management policy action for snapshot.</span></span>

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

### <span data-ttu-id="d60dc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d60dc-128">CommonParameters</span></span>
<span data-ttu-id="d60dc-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d60dc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d60dc-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d60dc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d60dc-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d60dc-131">INPUTS</span></span>

### <span data-ttu-id="d60dc-132">Microsoft. Azure. Commands. Management. Storage. models. PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="d60dc-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="d60dc-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d60dc-133">OUTPUTS</span></span>

### <span data-ttu-id="d60dc-134">Microsoft. Azure. Commands. Management. Storage. models. PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="d60dc-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="d60dc-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d60dc-135">NOTES</span></span>

## <span data-ttu-id="d60dc-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d60dc-136">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
ms.openlocfilehash: c2a20d19676cff15ff26792a81bfc09242c5e4c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195747"
---
# <span data-ttu-id="8693c-101">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="8693c-101">New-AzStorageAccountManagementPolicyRule</span></span>

## <span data-ttu-id="8693c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8693c-102">SYNOPSIS</span></span>
<span data-ttu-id="8693c-103">Tworzy obiekt reguły ManagementPolicy, którego można używać w politykę Set-AzStorageAccountManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="8693c-103">Creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="8693c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8693c-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyRule [-Name] <String> [-Disabled] -Action <PSManagementPolicyActionGroup>
 [-Filter <PSManagementPolicyRuleFilter>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8693c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8693c-105">DESCRIPTION</span></span>
<span data-ttu-id="8693c-106">Polecenie cmdlet **New-AzStorageAccountManagementPolicyRule** tworzy obiekt reguły ManagementPolicy, który może być używany w programie Set-AzStorageAccountManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="8693c-106">The **New-AzStorageAccountManagementPolicyRule** cmdlet creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="8693c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8693c-107">EXAMPLES</span></span>

### <span data-ttu-id="8693c-108">Przykład 1. Tworzy obiekt reguły ManagementPolicy, a następnie jest ustawiany jako konto magazynu</span><span class="sxs-lookup"><span data-stu-id="8693c-108">Example 1: Creates a ManagementPolicy rule object, then set to a Storage Account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2

PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name rule1 -Action $action -Filter $filter
PS C:\>$rule

Enabled    : True
Name       : rule1
Definition : {
                 "Actions":  {
                                 "BaseBlob":  {
                                                  "TierToCool":  {
                                                                     "DaysAfterModificationGreaterThan":  30
                                                                 },
                                                  "TierToArchive":  {
                                                                        "DaysAfterModificationGreaterThan":  50
                                                                    },
                                                  "Delete":  {
                                                                 "DaysAfterModificationGreaterThan":  100
                                                             }
                                              },
                                 "Snapshot":  {
                                                  "Delete":  {
                                                                 "DaysAfterCreationGreaterThan":  100
                                                             }
                                              }
                             },
                 "Filters":  {
                                 "PrefixMatch":  [
                                                     "blobprefix1",
                                                     "blobprefix2"
                                                 ],
                                 "BlobTypes":  [
                                                   "blockBlob"
                                               ]
                             }
             }

PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="8693c-109">To polecenie umożliwia utworzenie obiektu reguły ManagementPolicy z obiektem grupy akcji ManagementPolicy zawierającym 4 akcje, obiektem filtru reguły ManagementPolicy, a następnie ustawieniem dla reguły konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="8693c-109">This command create a ManagementPolicy rule object, with a ManagementPolicy action group object contains 4 actions, a ManagementPolicy rule filter object, then set the rule to a Storage Account.</span></span>

## <span data-ttu-id="8693c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8693c-110">PARAMETERS</span></span>

### <span data-ttu-id="8693c-111">— Akcja</span><span class="sxs-lookup"><span data-stu-id="8693c-111">-Action</span></span>
<span data-ttu-id="8693c-112">Obiekt definiujący zestaw akcji.</span><span class="sxs-lookup"><span data-stu-id="8693c-112">An object that defines the action set.</span></span>
<span data-ttu-id="8693c-113">Uzyskiwanie obiektu za pomocą polecenia cmdlet Add-AzureStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="8693c-113">Get the Object with cmdlet Add-AzureStorageAccountManagementPolicyAction</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8693c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8693c-114">-DefaultProfile</span></span>
<span data-ttu-id="8693c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8693c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8693c-116">— Wyłączone</span><span class="sxs-lookup"><span data-stu-id="8693c-116">-Disabled</span></span>
<span data-ttu-id="8693c-117">Reguła zostanie wyłączona, jeśli ją ustawisz.</span><span class="sxs-lookup"><span data-stu-id="8693c-117">The rule is disabled if set it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8693c-118">— Filtr</span><span class="sxs-lookup"><span data-stu-id="8693c-118">-Filter</span></span>
<span data-ttu-id="8693c-119">Obiekt definiujący zestaw filtrów.</span><span class="sxs-lookup"><span data-stu-id="8693c-119">An object that defines the filter set.</span></span>
<span data-ttu-id="8693c-120">Uzyskiwanie obiektu za pomocą polecenia cmdlet New-AzureStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="8693c-120">Get the Object with cmdlet New-AzureStorageAccountManagementPolicyFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8693c-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8693c-121">-Name</span></span>
<span data-ttu-id="8693c-122">Nazwa reguły może zawierać dowolną kombinację znaków alfanumerycznych.</span><span class="sxs-lookup"><span data-stu-id="8693c-122">A rule name can contain any combination of alpha numeric characters.</span></span>
<span data-ttu-id="8693c-123">W nazwie reguły jest zróżnicowa wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="8693c-123">Rule name is case-sensitive.</span></span>
<span data-ttu-id="8693c-124">Musi być unikatowy w ramach zasad.</span><span class="sxs-lookup"><span data-stu-id="8693c-124">It must be unique within a policy.</span></span>

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

### <span data-ttu-id="8693c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8693c-125">CommonParameters</span></span>
<span data-ttu-id="8693c-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8693c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8693c-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8693c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8693c-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8693c-128">INPUTS</span></span>

### <span data-ttu-id="8693c-129">Brak</span><span class="sxs-lookup"><span data-stu-id="8693c-129">None</span></span>

## <span data-ttu-id="8693c-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8693c-130">OUTPUTS</span></span>

### <span data-ttu-id="8693c-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="8693c-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span></span>

## <span data-ttu-id="8693c-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8693c-132">NOTES</span></span>

## <span data-ttu-id="8693c-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8693c-133">RELATED LINKS</span></span>

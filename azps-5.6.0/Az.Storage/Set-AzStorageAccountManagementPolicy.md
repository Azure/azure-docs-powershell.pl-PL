---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/set-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: cc91184374575b25f34669d7e22c80b620d34ced
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976170"
---
# <span data-ttu-id="65354-101">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="65354-101">Set-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="65354-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65354-102">SYNOPSIS</span></span>
<span data-ttu-id="65354-103">Tworzy lub modyfikuje zasady zarządzania konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="65354-103">Creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="65354-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="65354-104">SYNTAX</span></span>

### <span data-ttu-id="65354-105">AccountNamePolicyRule (domyślna)</span><span class="sxs-lookup"><span data-stu-id="65354-105">AccountNamePolicyRule (Default)</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Rule <PSManagementPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65354-106">AccountNamePolicyObject</span><span class="sxs-lookup"><span data-stu-id="65354-106">AccountNamePolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Policy <PSManagementPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65354-107">AccountObjectPolicyRule</span><span class="sxs-lookup"><span data-stu-id="65354-107">AccountObjectPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65354-108">AccountObjectPolicyObject</span><span class="sxs-lookup"><span data-stu-id="65354-108">AccountObjectPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65354-109">AccountResourceIdPolicyRule</span><span class="sxs-lookup"><span data-stu-id="65354-109">AccountResourceIdPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65354-110">AccountResourceIdPolicyObject</span><span class="sxs-lookup"><span data-stu-id="65354-110">AccountResourceIdPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65354-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="65354-111">DESCRIPTION</span></span>
<span data-ttu-id="65354-112">Polecenie **cmdlet Set-AzStorageAccountManagementPolicy** tworzy lub modyfikuje zasady zarządzania konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="65354-112">The **Set-AzStorageAccountManagementPolicy** cmdlet creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="65354-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="65354-113">EXAMPLES</span></span>

### <span data-ttu-id="65354-114">Przykład 1. Tworzenie lub aktualizowanie zasad zarządzania konta magazynu za pomocą obiektów reguł ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="65354-114">Example 1: Create or update the management policy of a Storage account with ManagementPolicy rule objects.</span></span>
```
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -SnapshotAction Delete -daysAfterCreationGreaterThan 100
PS C:\>$filter1 = New-AzStorageAccountManagementPolicyFilter -PrefixMatch ab,cd 
PS C:\>$rule1 = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action1 -Filter $filter1

PS C:\>$action2 = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100
PS C:\>$action2 = Add-AzStorageAccountManagementPolicyAction -InputObject $action2 -BlobVersionAction Delete -daysAfterCreationGreaterThan 100
PS C:\>$filter2 = New-AzStorageAccountManagementPolicyFilter -BlobType appendBlob,blockBlob
PS C:\>$rule2 = New-AzStorageAccountManagementPolicyRule -Name Test2 -Action $action2 -Filter $filter2

PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule1,$rule2


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 2/19/2021 10:13:00 AM
Rules              : [
                         {
                             "Enabled":  true,
                             "Name":  "Test",
                             "Definition":  {
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
                                                                                            },
                                                                                 "TierToCool":  null,
                                                                                 "TierToArchive":  null
                                                                             },
                                                                "Version":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  [
                                                                                    "ab",
                                                                                    "cd"
                                                                                ],
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         },
                         {
                             "Enabled":  true,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  null,
                                                                "Snapshot":  {
                                                                                 "Delete":  {
                                                                                                "DaysAfterCreationGreaterThan":  100
                                                                                            },
                                                                                 "TierToCool":  null,
                                                                                 "TierToArchive":  null
                                                                             },
                                                                "Version":  {
                                                                                "Delete":  {
                                                                                               "DaysAfterCreationGreaterThan":  100
                                                                                           },
                                                                                "TierToCool":  null,
                                                                                "TierToArchive":  null
                                                                            }
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "appendBlob",
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="65354-115">To polecenie najpierw tworzy 2 obiekty reguły ManagementPolicy, a następnie tworzy lub aktualizuje zasady zarządzania konta magazynu za pomocą obiektów reguły 2 ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="65354-115">This command first create 2 ManagementPolicy rule objects, then creates or updates the management policy of a Storage account with the 2 ManagementPolicy rule objects.</span></span>

### <span data-ttu-id="65354-116">Przykład 2. Tworzenie lub aktualizowanie zasad zarządzania konta magazynu przy użyciu zasad formatu Json.</span><span class="sxs-lookup"><span data-stu-id="65354-116">Example 2: Create or update the management policy of a Storage account with a Json format policy.</span></span>
```
PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Policy (@{
    Rules=(@{
        Enabled=$true;
        Name="Test";
        Definition=(@{
            Actions=(@{
                BaseBlob=(@{
                    TierToCool=@{DaysAfterModificationGreaterThan=30};
                    TierToArchive=@{DaysAfterModificationGreaterThan=50};
                    Delete=@{DaysAfterModificationGreaterThan=100};
                });
                Snapshot=(@{
                    Delete=@{DaysAfterCreationGreaterThan=100};
                    TierToArchive=@{DaysAfterCreationGreaterThan=50};
                    TierToCool=@{DaysAfterCreationGreaterThan=60};
                });
                Version=(@{
                    Delete=@{DaysAfterCreationGreaterThan=100};
                    TierToArchive=@{DaysAfterCreationGreaterThan=50};
                    TierToCool=@{DaysAfterCreationGreaterThan=60};
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob");
                PrefixMatch=@("prefix1","prefix2");
            })
        })
    },
    @{
        Enabled=$false;
        Name="Test2";
        Definition=(@{
            Actions=(@{
                Version=(@{
                    Delete=@{DaysAfterCreationGreaterThan=100};
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob","appendBlob");
            })
        })
    })
})


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 2/19/2021 10:16:32 AM
Rules              : [
                         {
                             "Enabled":  true,
                             "Name":  "Test",
                             "Definition":  {
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
                                                                                            },
                                                                                 "TierToCool":  {
                                                                                                    "DaysAfterCreationGreaterThan":  60
                                                                                                },
                                                                                 "TierToArchive":  {
                                                                                                       "DaysAfterCreationGreaterThan":  50
                                                                                                   }
                                                                             },
                                                                "Version":  {
                                                                                "Delete":  {
                                                                                               "DaysAfterCreationGreaterThan":  100
                                                                                           },
                                                                                "TierToCool":  {
                                                                                                   "DaysAfterCreationGreaterThan":  60
                                                                                               },
                                                                                "TierToArchive":  {
                                                                                                      "DaysAfterCreationGreaterThan":  50
                                                                                                  }
                                                                            }
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  [
                                                                                    "prefix1",
                                                                                    "prefix2"
                                                                                ],
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         },
                         {
                             "Enabled":  false,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  null,
                                                                "Snapshot":  null,
                                                                "Version":  {
                                                                                "Delete":  {
                                                                                               "DaysAfterCreationGreaterThan":  100
                                                                                           },
                                                                                "TierToCool":  null,
                                                                                "TierToArchive":  null
                                                                            }
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob",
                                                                                  "appendBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="65354-117">To polecenie tworzy lub aktualizuje zasady zarządzania konta magazynu przy użyciu zasad formatu json.</span><span class="sxs-lookup"><span data-stu-id="65354-117">This command creates or updates the management policy of a Storage account with a json format policy.</span></span>

### <span data-ttu-id="65354-118">Przykład 3. Pobierz zasady zarządzania z konta magazynu, a następnie ustaw je na inne konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="65354-118">Example 3: Get the management policy from a Storage account, then set it to another Storage account.</span></span>
```
PS C:\>$outputPolicy = Get-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" | Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup2" -AccountName "mystorageaccount2"
```

<span data-ttu-id="65354-119">To polecenie najpierw pobiera zasady zarządzania z konta magazynu, a następnie ustawia je na inne konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="65354-119">This command first gets the management policy from a Storage account, then set it to another Storage account.</span></span>

## <span data-ttu-id="65354-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65354-120">PARAMETERS</span></span>

### <span data-ttu-id="65354-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65354-121">-DefaultProfile</span></span>
<span data-ttu-id="65354-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="65354-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65354-123">— Zasady</span><span class="sxs-lookup"><span data-stu-id="65354-123">-Policy</span></span>
<span data-ttu-id="65354-124">Obiekt zasad zarządzania do ustawienia</span><span class="sxs-lookup"><span data-stu-id="65354-124">Management Policy Object to Set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy
Parameter Sets: AccountNamePolicyObject, AccountObjectPolicyObject, AccountResourceIdPolicyObject
Aliases: ManagementPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65354-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65354-125">-ResourceGroupName</span></span>
<span data-ttu-id="65354-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="65354-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNamePolicyRule, AccountNamePolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65354-127">— reguła</span><span class="sxs-lookup"><span data-stu-id="65354-127">-Rule</span></span>
<span data-ttu-id="65354-128">Reguły zasad zarządzania.</span><span class="sxs-lookup"><span data-stu-id="65354-128">The Management Policy rules.</span></span> <span data-ttu-id="65354-129">Pobierz obiekt za pomocą New-AzStorageAccountManagementPolicyRule cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65354-129">Get the object with New-AzStorageAccountManagementPolicyRule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule[]
Parameter Sets: AccountNamePolicyRule, AccountObjectPolicyRule, AccountResourceIdPolicyRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65354-130">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="65354-130">-StorageAccount</span></span>
<span data-ttu-id="65354-131">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="65354-131">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObjectPolicyRule, AccountObjectPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65354-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="65354-132">-StorageAccountName</span></span>
<span data-ttu-id="65354-133">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="65354-133">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNamePolicyRule, AccountNamePolicyObject
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65354-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="65354-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="65354-135">Identyfikator zasobu konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="65354-135">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceIdPolicyRule, AccountResourceIdPolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65354-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65354-136">-Confirm</span></span>
<span data-ttu-id="65354-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="65354-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65354-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65354-138">-WhatIf</span></span>
<span data-ttu-id="65354-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65354-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65354-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="65354-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65354-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65354-141">CommonParameters</span></span>
<span data-ttu-id="65354-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65354-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65354-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65354-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65354-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65354-144">INPUTS</span></span>

### <span data-ttu-id="65354-145">System.String</span><span class="sxs-lookup"><span data-stu-id="65354-145">System.String</span></span>

## <span data-ttu-id="65354-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65354-146">OUTPUTS</span></span>

### <span data-ttu-id="65354-147">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="65354-147">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy</span></span>

## <span data-ttu-id="65354-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="65354-148">NOTES</span></span>

## <span data-ttu-id="65354-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65354-149">RELATED LINKS</span></span>

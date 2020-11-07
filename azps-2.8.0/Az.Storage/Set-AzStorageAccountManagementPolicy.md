---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/set-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: 6a5b97ca21ca08ba51a96528e5652e80d71aef07
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888282"
---
# <span data-ttu-id="ff233-101">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ff233-101">Set-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="ff233-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ff233-102">SYNOPSIS</span></span>
<span data-ttu-id="ff233-103">Tworzy lub modyfikuje zasady zarządzania konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="ff233-103">Creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="ff233-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ff233-104">SYNTAX</span></span>

### <span data-ttu-id="ff233-105">AccountNamePolicyRule (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ff233-105">AccountNamePolicyRule (Default)</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Rule <PSManagementPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff233-106">AccountNamePolicyObject</span><span class="sxs-lookup"><span data-stu-id="ff233-106">AccountNamePolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Policy <PSManagementPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff233-107">AccountObjectPolicyRule</span><span class="sxs-lookup"><span data-stu-id="ff233-107">AccountObjectPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff233-108">AccountObjectPolicyObject</span><span class="sxs-lookup"><span data-stu-id="ff233-108">AccountObjectPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff233-109">AccountResourceIdPolicyRule</span><span class="sxs-lookup"><span data-stu-id="ff233-109">AccountResourceIdPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff233-110">AccountResourceIdPolicyObject</span><span class="sxs-lookup"><span data-stu-id="ff233-110">AccountResourceIdPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff233-111">Opis</span><span class="sxs-lookup"><span data-stu-id="ff233-111">DESCRIPTION</span></span>
<span data-ttu-id="ff233-112">Polecenie cmdlet **Set-AzStorageAccountManagementPolicy** służy do tworzenia lub modyfikowania zasad zarządzania konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="ff233-112">The **Set-AzStorageAccountManagementPolicy** cmdlet creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="ff233-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ff233-113">EXAMPLES</span></span>

### <span data-ttu-id="ff233-114">Przykład 1: Tworzenie lub aktualizowanie zasad zarządzania konta magazynu za pomocą obiektów reguł ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="ff233-114">Example 1: Create or update the management policy of a Storage account with ManagementPolicy rule objects.</span></span>
```
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -SnapshotAction Delete -daysAfterCreationGreaterThan 100
PS C:\>$filter1 = New-AzStorageAccountManagementPolicyFilter -PrefixMatch ab,cd 
PS C:\>$rule1 = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action1 -Filter $filter1

PS C:\>$action2 = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$filter2 = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule2 = New-AzStorageAccountManagementPolicyRule -Name Test2 -Action $action2 -Filter $filter2

PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule1,$rule2


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 10:29:29 AM
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
                             "Enabled":  true,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  null,
                                                                                 "TierToArchive":  null,
                                                                                 "Delete":  {
                                                                                                "DaysAfterModificationGreaterThan":  100
                                                                                            }
                                                                             },
                                                                "Snapshot":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="ff233-115">To polecenie najpierw tworzy 2 ManagementPolicy obiekty reguły, a następnie tworzy lub aktualizuje zasady zarządzania konta magazynu przy użyciu obiektów reguł 2 ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="ff233-115">This command first create 2 ManagementPolicy rule objects, then creates or updates the management policy of a Storage account with the 2 ManagementPolicy rule objects.</span></span>

### <span data-ttu-id="ff233-116">Przykład 2: Tworzenie lub aktualizowanie zasad zarządzania konta magazynu przy użyciu zasad formatu notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="ff233-116">Example 2: Create or update the management policy of a Storage account with a Json format policy.</span></span>
```
PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Policy (@{
    Rules=(@{
        Enabled="true";
        Name="Test";
        Definition=(@{
            Actions=(@{
                BaseBlob=(@{
                    TierToCool=30;
                    TierToArchive=50;
                    Delete=100;
                });
                Snapshot=(@{
                    Delete=100
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob");
                PrefixMatch=@("prefix1","prefix2");
            })
        })
    },
    @{
        Enabled="false";
        Name="Test2";
        Definition=(@{
            Actions=(@{
                BaseBlob=(@{
                    TierToCool=80;
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob");
            })
        })
    })
})


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 10:24:55 AM
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
                             "Enabled":  true,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  {
                                                                                                    "DaysAfterModificationGreaterThan":  80
                                                                                                },
                                                                                 "TierToArchive":  null,
                                                                                 "Delete":  null
                                                                             },
                                                                "Snapshot":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="ff233-117">To polecenie umożliwia utworzenie lub zaktualizowanie zasad zarządzania konta magazynu przy użyciu zasad formatu notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="ff233-117">This command creates or updates the management policy of a Storage account with a json format policy.</span></span>

### <span data-ttu-id="ff233-118">Przykład 3: Uzyskaj zasady zarządzania z konta magazynu, a następnie ustaw je na inne konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="ff233-118">Example 3: Get the management policy from a Storage account, then set it to another Storage account.</span></span>
```
PS C:\>$outputPolicy = Get-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" | Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup2" -AccountName "mystorageaccount2"
```

<span data-ttu-id="ff233-119">To polecenie po raz pierwszy pobiera zasady zarządzania z konta magazynu, a następnie ustawia je na inne konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="ff233-119">This command first gets the management policy from a Storage account, then set it to another Storage account.</span></span>

## <span data-ttu-id="ff233-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ff233-120">PARAMETERS</span></span>

### <span data-ttu-id="ff233-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff233-121">-DefaultProfile</span></span>
<span data-ttu-id="ff233-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ff233-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff233-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="ff233-123">-Policy</span></span>
<span data-ttu-id="ff233-124">Obiekt zasad zarządzania do ustawienia</span><span class="sxs-lookup"><span data-stu-id="ff233-124">Management Policy Object to Set</span></span>

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

### <span data-ttu-id="ff233-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff233-125">-ResourceGroupName</span></span>
<span data-ttu-id="ff233-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ff233-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="ff233-127">— Reguła</span><span class="sxs-lookup"><span data-stu-id="ff233-127">-Rule</span></span>
<span data-ttu-id="ff233-128">Reguły zasad zarządzania.</span><span class="sxs-lookup"><span data-stu-id="ff233-128">The Management Policy rules.</span></span> <span data-ttu-id="ff233-129">Pobierz obiekt za pomocą polecenia cmdlet New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="ff233-129">Get the object with New-AzStorageAccountManagementPolicyRule cmdlet.</span></span>

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

### <span data-ttu-id="ff233-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff233-130">-StorageAccount</span></span>
<span data-ttu-id="ff233-131">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="ff233-131">Storage account object</span></span>

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

### <span data-ttu-id="ff233-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ff233-132">-StorageAccountName</span></span>
<span data-ttu-id="ff233-133">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ff233-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="ff233-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="ff233-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="ff233-135">Identyfikator zasobu konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ff233-135">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="ff233-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ff233-136">-Confirm</span></span>
<span data-ttu-id="ff233-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff233-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff233-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff233-138">-WhatIf</span></span>
<span data-ttu-id="ff233-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff233-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff233-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ff233-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff233-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff233-141">CommonParameters</span></span>
<span data-ttu-id="ff233-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff233-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff233-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff233-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff233-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff233-144">INPUTS</span></span>

### <span data-ttu-id="ff233-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ff233-145">System.String</span></span>

## <span data-ttu-id="ff233-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ff233-146">OUTPUTS</span></span>

### <span data-ttu-id="ff233-147">Microsoft. Azure. Commands. Management. Storage. models. PSManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ff233-147">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy</span></span>

## <span data-ttu-id="ff233-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ff233-148">NOTES</span></span>

## <span data-ttu-id="ff233-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff233-149">RELATED LINKS</span></span>

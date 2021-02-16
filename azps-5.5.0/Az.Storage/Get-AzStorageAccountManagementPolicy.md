---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: b27d6e8bec4dda2ba87a0b38a9b37a8d4739ae00
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201338"
---
# <span data-ttu-id="32f59-101">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="32f59-101">Get-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="32f59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32f59-102">SYNOPSIS</span></span>
<span data-ttu-id="32f59-103">Pobiera zasady zarządzania konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="32f59-103">Gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="32f59-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="32f59-104">SYNTAX</span></span>

### <span data-ttu-id="32f59-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="32f59-105">AccountName (Default)</span></span>
```
Get-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32f59-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="32f59-106">AccountResourceId</span></span>
```
Get-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32f59-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="32f59-107">AccountObject</span></span>
```
Get-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32f59-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="32f59-108">DESCRIPTION</span></span>
<span data-ttu-id="32f59-109">Polecenie **cmdlet Get-AzStorageAccountManagementPolicy** pobiera zasady zarządzania konta magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="32f59-109">The **Get-AzStorageAccountManagementPolicy** cmdlet gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="32f59-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="32f59-110">EXAMPLES</span></span>

### <span data-ttu-id="32f59-111">Przykład 1. Uzyskiwanie zasad zarządzania konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="32f59-111">Example 1: Get the management policy of a Storage account.</span></span>
```
PS C:\>Get-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 7:04:05 AM
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

<span data-ttu-id="32f59-112">To polecenie pobiera zasady zarządzania konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="32f59-112">This command gets the management policy of a Storage account.</span></span>

## <span data-ttu-id="32f59-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32f59-113">PARAMETERS</span></span>

### <span data-ttu-id="32f59-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32f59-114">-DefaultProfile</span></span>
<span data-ttu-id="32f59-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="32f59-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32f59-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32f59-116">-ResourceGroupName</span></span>
<span data-ttu-id="32f59-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="32f59-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="32f59-118">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="32f59-118">-StorageAccount</span></span>
<span data-ttu-id="32f59-119">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="32f59-119">Storage account object</span></span>

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

### <span data-ttu-id="32f59-120">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="32f59-120">-StorageAccountName</span></span>
<span data-ttu-id="32f59-121">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="32f59-121">Storage Account Name.</span></span>

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

### <span data-ttu-id="32f59-122">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="32f59-122">-StorageAccountResourceId</span></span>
<span data-ttu-id="32f59-123">Identyfikator zasobu konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="32f59-123">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32f59-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32f59-124">CommonParameters</span></span>
<span data-ttu-id="32f59-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32f59-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32f59-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32f59-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32f59-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32f59-127">INPUTS</span></span>

### <span data-ttu-id="32f59-128">System.String</span><span class="sxs-lookup"><span data-stu-id="32f59-128">System.String</span></span>

## <span data-ttu-id="32f59-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="32f59-129">OUTPUTS</span></span>

### <span data-ttu-id="32f59-130">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="32f59-130">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="32f59-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="32f59-131">NOTES</span></span>

## <span data-ttu-id="32f59-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32f59-132">RELATED LINKS</span></span>

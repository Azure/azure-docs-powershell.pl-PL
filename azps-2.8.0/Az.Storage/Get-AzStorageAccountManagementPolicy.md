---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: 21736c7cb49d6544b9fc0a9c17a9b2a339767297
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887197"
---
# <span data-ttu-id="6fb6e-101">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6fb6e-101">Get-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="6fb6e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6fb6e-102">SYNOPSIS</span></span>
<span data-ttu-id="6fb6e-103">Pobiera zasady zarządzania konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6fb6e-103">Gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="6fb6e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6fb6e-104">SYNTAX</span></span>

### <span data-ttu-id="6fb6e-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="6fb6e-105">AccountName (Default)</span></span>
```
Get-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fb6e-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="6fb6e-106">AccountResourceId</span></span>
```
Get-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fb6e-107">AccountName</span><span class="sxs-lookup"><span data-stu-id="6fb6e-107">AccountObject</span></span>
```
Get-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fb6e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6fb6e-108">DESCRIPTION</span></span>
<span data-ttu-id="6fb6e-109">Polecenie cmdlet **Get-AzStorageAccountManagementPolicy** pobiera zasady zarządzania konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6fb6e-109">The **Get-AzStorageAccountManagementPolicy** cmdlet gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="6fb6e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6fb6e-110">EXAMPLES</span></span>

### <span data-ttu-id="6fb6e-111">Przykład 1: uzyskiwanie zasad zarządzania konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6fb6e-111">Example 1: Get the management policy of a Storage account.</span></span>
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

<span data-ttu-id="6fb6e-112">To polecenie pobiera zasady zarządzania konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6fb6e-112">This command gets the management policy of a Storage account.</span></span>

## <span data-ttu-id="6fb6e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6fb6e-113">PARAMETERS</span></span>

### <span data-ttu-id="6fb6e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fb6e-114">-DefaultProfile</span></span>
<span data-ttu-id="6fb6e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fb6e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fb6e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fb6e-116">-ResourceGroupName</span></span>
<span data-ttu-id="6fb6e-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6fb6e-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="6fb6e-118">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6fb6e-118">-StorageAccount</span></span>
<span data-ttu-id="6fb6e-119">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="6fb6e-119">Storage account object</span></span>

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

### <span data-ttu-id="6fb6e-120">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6fb6e-120">-StorageAccountName</span></span>
<span data-ttu-id="6fb6e-121">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6fb6e-121">Storage Account Name.</span></span>

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

### <span data-ttu-id="6fb6e-122">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="6fb6e-122">-StorageAccountResourceId</span></span>
<span data-ttu-id="6fb6e-123">Identyfikator zasobu konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6fb6e-123">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="6fb6e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fb6e-124">CommonParameters</span></span>
<span data-ttu-id="6fb6e-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fb6e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fb6e-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fb6e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fb6e-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fb6e-127">INPUTS</span></span>

### <span data-ttu-id="6fb6e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6fb6e-128">System.String</span></span>

## <span data-ttu-id="6fb6e-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6fb6e-129">OUTPUTS</span></span>

### <span data-ttu-id="6fb6e-130">Microsoft. Azure. Management. Storage. MODELES. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6fb6e-130">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="6fb6e-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6fb6e-131">NOTES</span></span>

## <span data-ttu-id="6fb6e-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fb6e-132">RELATED LINKS</span></span>

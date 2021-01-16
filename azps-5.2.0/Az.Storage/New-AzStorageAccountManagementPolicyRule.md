---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
ms.openlocfilehash: c2a20d19676cff15ff26792a81bfc09242c5e4c2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349486"
---
# <span data-ttu-id="cc415-101">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="cc415-101">New-AzStorageAccountManagementPolicyRule</span></span>

## <span data-ttu-id="cc415-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc415-102">SYNOPSIS</span></span>
<span data-ttu-id="cc415-103">Tworzy obiekt reguły ManagementPolicy, który można użyć w programie Set-AzStorageAccountManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="cc415-103">Creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="cc415-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc415-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyRule [-Name] <String> [-Disabled] -Action <PSManagementPolicyActionGroup>
 [-Filter <PSManagementPolicyRuleFilter>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc415-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cc415-105">DESCRIPTION</span></span>
<span data-ttu-id="cc415-106">Polecenie cmdlet **New-AzStorageAccountManagementPolicyRule** tworzy obiekt reguły ManagementPolicy, którego można użyć w parametrze Set-AzStorageAccountManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="cc415-106">The **New-AzStorageAccountManagementPolicyRule** cmdlet creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="cc415-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc415-107">EXAMPLES</span></span>

### <span data-ttu-id="cc415-108">Przykład 1: utworzenie obiektu reguły ManagementPolicy, a następnie ustawienie konta magazynu</span><span class="sxs-lookup"><span data-stu-id="cc415-108">Example 1: Creates a ManagementPolicy rule object, then set to a Storage Account</span></span>
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

<span data-ttu-id="cc415-109">To polecenie tworzy obiekt reguły ManagementPolicy, a obiekt grupy akcji ManagementPolicy zawiera 4 akcje, obiekt filtr reguły ManagementPolicy, a następnie ustawienie reguły na konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="cc415-109">This command create a ManagementPolicy rule object, with a ManagementPolicy action group object contains 4 actions, a ManagementPolicy rule filter object, then set the rule to a Storage Account.</span></span>

## <span data-ttu-id="cc415-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc415-110">PARAMETERS</span></span>

### <span data-ttu-id="cc415-111">-Action</span><span class="sxs-lookup"><span data-stu-id="cc415-111">-Action</span></span>
<span data-ttu-id="cc415-112">Obiekt definiujący zestaw akcji.</span><span class="sxs-lookup"><span data-stu-id="cc415-112">An object that defines the action set.</span></span>
<span data-ttu-id="cc415-113">Uzyskiwanie obiektu za pomocą polecenia cmdlet Add-AzureStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="cc415-113">Get the Object with cmdlet Add-AzureStorageAccountManagementPolicyAction</span></span>

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

### <span data-ttu-id="cc415-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc415-114">-DefaultProfile</span></span>
<span data-ttu-id="cc415-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc415-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc415-116">-Wyłączone</span><span class="sxs-lookup"><span data-stu-id="cc415-116">-Disabled</span></span>
<span data-ttu-id="cc415-117">Reguła jest wyłączona, jeśli ją ustawiono.</span><span class="sxs-lookup"><span data-stu-id="cc415-117">The rule is disabled if set it.</span></span>

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

### <span data-ttu-id="cc415-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="cc415-118">-Filter</span></span>
<span data-ttu-id="cc415-119">Obiekt definiujący zestaw filtrów.</span><span class="sxs-lookup"><span data-stu-id="cc415-119">An object that defines the filter set.</span></span>
<span data-ttu-id="cc415-120">Uzyskiwanie obiektu za pomocą polecenia cmdlet New-AzureStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="cc415-120">Get the Object with cmdlet New-AzureStorageAccountManagementPolicyFilter</span></span>

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

### <span data-ttu-id="cc415-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cc415-121">-Name</span></span>
<span data-ttu-id="cc415-122">Nazwa reguły może zawierać dowolną kombinację cyfr alfanumerycznych.</span><span class="sxs-lookup"><span data-stu-id="cc415-122">A rule name can contain any combination of alpha numeric characters.</span></span>
<span data-ttu-id="cc415-123">W nazwie reguły jest uwzględniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="cc415-123">Rule name is case-sensitive.</span></span>
<span data-ttu-id="cc415-124">Musi być unikatowa w obrębie zasad.</span><span class="sxs-lookup"><span data-stu-id="cc415-124">It must be unique within a policy.</span></span>

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

### <span data-ttu-id="cc415-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc415-125">CommonParameters</span></span>
<span data-ttu-id="cc415-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc415-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc415-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc415-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc415-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc415-128">INPUTS</span></span>

### <span data-ttu-id="cc415-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cc415-129">None</span></span>

## <span data-ttu-id="cc415-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc415-130">OUTPUTS</span></span>

### <span data-ttu-id="cc415-131">Microsoft. Azure. Commands. Management. Storage. models. PSManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="cc415-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span></span>

## <span data-ttu-id="cc415-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc415-132">NOTES</span></span>

## <span data-ttu-id="cc415-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc415-133">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 40a2420803197b21bb9f0f8d20b771482b4e694b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002634"
---
# <span data-ttu-id="3f3f3-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="3f3f3-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="3f3f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f3f3-102">SYNOPSIS</span></span>
<span data-ttu-id="3f3f3-103">Tworzy obiekt filtru reguły ManagementPolicy, którego można używać w rrrr-azstorageaccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="3f3f3-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="3f3f3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3f3f3-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-BlobType <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f3f3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3f3f3-105">DESCRIPTION</span></span>
<span data-ttu-id="3f3f3-106">Polecenie cmdlet **New-AzStorageAccountManagementPolicyFilter** tworzy obiekt filtru reguły ManagementPolicy, którego można używać w programie New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="3f3f3-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="3f3f3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3f3f3-107">EXAMPLES</span></span>

### <span data-ttu-id="3f3f3-108">Przykład 1. Tworzy obiekt filtru reguły ManagementPolicy, a następnie dodaje go do reguły zasad zarządzania i ustawia na konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="3f3f3-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2 -BlobType appendBlob,blockBlob
PS C:\>$filter 

PrefixMatch                BlobTypes  
-----------                ---------  
{blobprefix1, blobprefix2} {appendBlob, blockBlob}

PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="3f3f3-109">To polecenie umożliwia utworzenie obiektu filtru reguł zasad zarządzania.</span><span class="sxs-lookup"><span data-stu-id="3f3f3-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="3f3f3-110">Następnie dodaj ją do reguły zasad zarządzania i ustaw jako konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="3f3f3-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="3f3f3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f3f3-111">PARAMETERS</span></span>

### <span data-ttu-id="3f3f3-112">-BlobType</span><span class="sxs-lookup"><span data-stu-id="3f3f3-112">-BlobType</span></span>
<span data-ttu-id="3f3f3-113">Tablica ciągów dla typów obiektów blob, które mają być zgodne.</span><span class="sxs-lookup"><span data-stu-id="3f3f3-113">An array of strings for blobtypes to be match.</span></span> <span data-ttu-id="3f3f3-114">Obecnie blockBlob obsługuje wszystkie akcje związane z usuwaniem i warstwami.</span><span class="sxs-lookup"><span data-stu-id="3f3f3-114">Currently blockBlob supports all tiering and delete actions.</span></span> <span data-ttu-id="3f3f3-115">W przypadku do dołączaniaBlob są obsługiwane tylko akcje usuwania.</span><span class="sxs-lookup"><span data-stu-id="3f3f3-115">Only delete actions are supported for appendBlob.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: blockBlob, appendBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f3f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f3f3-116">-DefaultProfile</span></span>
<span data-ttu-id="3f3f3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3f3f3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f3f3-118">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="3f3f3-118">-PrefixMatch</span></span>
<span data-ttu-id="3f3f3-119">Tablica ciągów prefiksów, które mają być zgodne.</span><span class="sxs-lookup"><span data-stu-id="3f3f3-119">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="3f3f3-120">Ciąg prefiksu musi zaczynać się od nazwy kontenera.</span><span class="sxs-lookup"><span data-stu-id="3f3f3-120">A prefix string must start with a container name.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f3f3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f3f3-121">CommonParameters</span></span>
<span data-ttu-id="3f3f3-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f3f3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f3f3-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f3f3-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f3f3-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f3f3-124">INPUTS</span></span>

### <span data-ttu-id="3f3f3-125">Brak</span><span class="sxs-lookup"><span data-stu-id="3f3f3-125">None</span></span>

## <span data-ttu-id="3f3f3-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f3f3-126">OUTPUTS</span></span>

### <span data-ttu-id="3f3f3-127">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span><span class="sxs-lookup"><span data-stu-id="3f3f3-127">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="3f3f3-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3f3f3-128">NOTES</span></span>

## <span data-ttu-id="3f3f3-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f3f3-129">RELATED LINKS</span></span>

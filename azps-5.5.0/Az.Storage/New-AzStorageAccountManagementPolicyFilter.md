---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 48ae8b87671e52abe4d109025048fe1e4aeca117
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198483"
---
# <span data-ttu-id="882dc-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="882dc-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="882dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="882dc-102">SYNOPSIS</span></span>
<span data-ttu-id="882dc-103">Tworzy obiekt filtru reguły ManagementPolicy, którego można używać w rrrr-azstorageaccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="882dc-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="882dc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="882dc-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="882dc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="882dc-105">DESCRIPTION</span></span>
<span data-ttu-id="882dc-106">Polecenie cmdlet **New-AzStorageAccountManagementPolicyFilter** tworzy obiekt filtru reguły ManagementPolicy, którego można używać w programie New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="882dc-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="882dc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="882dc-107">EXAMPLES</span></span>

### <span data-ttu-id="882dc-108">Przykład 1. Tworzy obiekt filtru reguły ManagementPolicy, a następnie dodaje go do reguły zasad zarządzania i ustawia na konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="882dc-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2
PS C:\>$filter 

PrefixMatch                BlobTypes  
-----------                ---------  
{blobprefix1, blobprefix2} {blockBlob}

PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="882dc-109">To polecenie umożliwia utworzenie obiektu filtru reguł zasad zarządzania.</span><span class="sxs-lookup"><span data-stu-id="882dc-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="882dc-110">Następnie dodaj ją do reguły zasad zarządzania i ustaw jako konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="882dc-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="882dc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="882dc-111">PARAMETERS</span></span>

### <span data-ttu-id="882dc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="882dc-112">-DefaultProfile</span></span>
<span data-ttu-id="882dc-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="882dc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="882dc-114">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="882dc-114">-PrefixMatch</span></span>
<span data-ttu-id="882dc-115">Tablica ciągów prefiksów, które mają być zgodne.</span><span class="sxs-lookup"><span data-stu-id="882dc-115">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="882dc-116">Ciąg prefiksu musi zaczynać się od nazwy kontenera.</span><span class="sxs-lookup"><span data-stu-id="882dc-116">A prefix string must start with a container name.</span></span>

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

### <span data-ttu-id="882dc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="882dc-117">CommonParameters</span></span>
<span data-ttu-id="882dc-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="882dc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="882dc-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="882dc-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="882dc-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="882dc-120">INPUTS</span></span>

### <span data-ttu-id="882dc-121">Brak</span><span class="sxs-lookup"><span data-stu-id="882dc-121">None</span></span>

## <span data-ttu-id="882dc-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="882dc-122">OUTPUTS</span></span>

### <span data-ttu-id="882dc-123">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span><span class="sxs-lookup"><span data-stu-id="882dc-123">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="882dc-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="882dc-124">NOTES</span></span>

## <span data-ttu-id="882dc-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="882dc-125">RELATED LINKS</span></span>

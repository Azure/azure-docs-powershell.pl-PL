---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
ms.openlocfilehash: 344bba00d610b5e23b2af5bce8476185e8bee377
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969313"
---
# <span data-ttu-id="e7a41-101">Get-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="e7a41-101">Get-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="e7a41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7a41-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a41-103">Pobierz zestawy szyfrowania dysku lub wybierz je z listy.</span><span class="sxs-lookup"><span data-stu-id="e7a41-103">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="e7a41-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e7a41-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7a41-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e7a41-105">DESCRIPTION</span></span>
<span data-ttu-id="e7a41-106">Pobierz zestawy szyfrowania dysku lub wybierz je z listy.</span><span class="sxs-lookup"><span data-stu-id="e7a41-106">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="e7a41-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e7a41-107">EXAMPLES</span></span>

### <span data-ttu-id="e7a41-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e7a41-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet -ResourceGroupName rg1 -Name enc1;

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="e7a41-109">Uzyskaj zestaw szyfrowania dysku "enc1"</span><span class="sxs-lookup"><span data-stu-id="e7a41-109">Get disk encryption set 'enc1'</span></span>

### <span data-ttu-id="e7a41-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e7a41-110">Example 2</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc2
Name              : enc2
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="e7a41-111">Pobierz wszystkie zestawy szyfrowania dysku w grupie zasobów "rg1".</span><span class="sxs-lookup"><span data-stu-id="e7a41-111">Get all disk encryption sets in resource group 'rg1'.</span></span>

### <span data-ttu-id="e7a41-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e7a41-112">Example 3</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet -ResourceGroupName rg1

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc2
Name              : enc2
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg2
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc3
Name              : enc3
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="e7a41-113">Uzyskaj wszystkie zestawy szyfrowania dysku w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e7a41-113">Get all disk encryption sets in subscription.</span></span>

## <span data-ttu-id="e7a41-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7a41-114">PARAMETERS</span></span>

### <span data-ttu-id="e7a41-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a41-115">-DefaultProfile</span></span>
<span data-ttu-id="e7a41-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7a41-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7a41-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e7a41-117">-Name</span></span>
<span data-ttu-id="e7a41-118">Nazwa zestawu szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="e7a41-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a41-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7a41-119">-ResourceGroupName</span></span>
<span data-ttu-id="e7a41-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e7a41-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a41-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a41-121">CommonParameters</span></span>
<span data-ttu-id="e7a41-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7a41-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a41-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7a41-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a41-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7a41-124">INPUTS</span></span>

### <span data-ttu-id="e7a41-125">System.String</span><span class="sxs-lookup"><span data-stu-id="e7a41-125">System.String</span></span>

## <span data-ttu-id="e7a41-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7a41-126">OUTPUTS</span></span>

### <span data-ttu-id="e7a41-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="e7a41-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="e7a41-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e7a41-128">NOTES</span></span>

## <span data-ttu-id="e7a41-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7a41-129">RELATED LINKS</span></span>

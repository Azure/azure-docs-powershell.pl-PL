---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
ms.openlocfilehash: 7d2b23c08f7ce910daf87f7cebbea844d5bda6f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181723"
---
# <span data-ttu-id="9a531-101">Get-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="9a531-101">Get-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="9a531-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a531-102">SYNOPSIS</span></span>
<span data-ttu-id="9a531-103">Pobierz lub z listy zestawów szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="9a531-103">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="9a531-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9a531-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a531-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9a531-105">DESCRIPTION</span></span>
<span data-ttu-id="9a531-106">Pobierz lub z listy zestawów szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="9a531-106">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="9a531-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9a531-107">EXAMPLES</span></span>

### <span data-ttu-id="9a531-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9a531-108">Example 1</span></span>
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

<span data-ttu-id="9a531-109">Uzyskaj zestaw szyfrowania dysku "enc1"</span><span class="sxs-lookup"><span data-stu-id="9a531-109">Get disk encryption set 'enc1'</span></span>

### <span data-ttu-id="9a531-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9a531-110">Example 2</span></span>
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

<span data-ttu-id="9a531-111">Pobierz wszystkie zestawy szyfrowania dysku w grupie zasobów "rg1".</span><span class="sxs-lookup"><span data-stu-id="9a531-111">Get all disk encryption sets in resource group 'rg1'.</span></span>

### <span data-ttu-id="9a531-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9a531-112">Example 3</span></span>
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

<span data-ttu-id="9a531-113">Uzyskaj wszystkie zestawy szyfrowania dysku w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9a531-113">Get all disk encryption sets in subscription.</span></span>

## <span data-ttu-id="9a531-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a531-114">PARAMETERS</span></span>

### <span data-ttu-id="9a531-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a531-115">-DefaultProfile</span></span>
<span data-ttu-id="9a531-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9a531-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a531-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9a531-117">-Name</span></span>
<span data-ttu-id="9a531-118">Nazwa zestawu szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="9a531-118">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="9a531-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a531-119">-ResourceGroupName</span></span>
<span data-ttu-id="9a531-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9a531-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9a531-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a531-121">CommonParameters</span></span>
<span data-ttu-id="9a531-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a531-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a531-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a531-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a531-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a531-124">INPUTS</span></span>

### <span data-ttu-id="9a531-125">System.String</span><span class="sxs-lookup"><span data-stu-id="9a531-125">System.String</span></span>

## <span data-ttu-id="9a531-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a531-126">OUTPUTS</span></span>

### <span data-ttu-id="9a531-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="9a531-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="9a531-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9a531-128">NOTES</span></span>

## <span data-ttu-id="9a531-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a531-129">RELATED LINKS</span></span>

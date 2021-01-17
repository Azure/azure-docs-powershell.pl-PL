---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
ms.openlocfilehash: 7d2b23c08f7ce910daf87f7cebbea844d5bda6f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332797"
---
# <span data-ttu-id="4ba6f-101">Get-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="4ba6f-101">Get-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="4ba6f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ba6f-102">SYNOPSIS</span></span>
<span data-ttu-id="4ba6f-103">Uzyskiwanie lub wyświetlanie zestawów szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="4ba6f-103">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="4ba6f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ba6f-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ba6f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4ba6f-105">DESCRIPTION</span></span>
<span data-ttu-id="4ba6f-106">Uzyskiwanie lub wyświetlanie zestawów szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="4ba6f-106">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="4ba6f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ba6f-107">EXAMPLES</span></span>

### <span data-ttu-id="4ba6f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4ba6f-108">Example 1</span></span>
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

<span data-ttu-id="4ba6f-109">Pobierz zestaw szyfrowanie dysków enc1 '</span><span class="sxs-lookup"><span data-stu-id="4ba6f-109">Get disk encryption set 'enc1'</span></span>

### <span data-ttu-id="4ba6f-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4ba6f-110">Example 2</span></span>
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

<span data-ttu-id="4ba6f-111">Pobierz wszystkie zestawy szyfrowania dysków w grupie zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="4ba6f-111">Get all disk encryption sets in resource group 'rg1'.</span></span>

### <span data-ttu-id="4ba6f-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="4ba6f-112">Example 3</span></span>
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

<span data-ttu-id="4ba6f-113">Pobierz wszystkie zestawy szyfrowania dysków w abonament.</span><span class="sxs-lookup"><span data-stu-id="4ba6f-113">Get all disk encryption sets in subscription.</span></span>

## <span data-ttu-id="4ba6f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ba6f-114">PARAMETERS</span></span>

### <span data-ttu-id="4ba6f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ba6f-115">-DefaultProfile</span></span>
<span data-ttu-id="4ba6f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ba6f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ba6f-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4ba6f-117">-Name</span></span>
<span data-ttu-id="4ba6f-118">Nazwa zestawu szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="4ba6f-118">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="4ba6f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ba6f-119">-ResourceGroupName</span></span>
<span data-ttu-id="4ba6f-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ba6f-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4ba6f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ba6f-121">CommonParameters</span></span>
<span data-ttu-id="4ba6f-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ba6f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ba6f-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ba6f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ba6f-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ba6f-124">INPUTS</span></span>

### <span data-ttu-id="4ba6f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4ba6f-125">System.String</span></span>

## <span data-ttu-id="4ba6f-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ba6f-126">OUTPUTS</span></span>

### <span data-ttu-id="4ba6f-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="4ba6f-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="4ba6f-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ba6f-128">NOTES</span></span>

## <span data-ttu-id="4ba6f-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ba6f-129">RELATED LINKS</span></span>

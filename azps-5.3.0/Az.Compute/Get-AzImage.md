---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzImage.md
ms.openlocfilehash: 4d1de6553a07cf58fdc109dc5703e37392a27a02
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504133"
---
# <span data-ttu-id="f5b63-101">Get-AzImage</span><span class="sxs-lookup"><span data-stu-id="f5b63-101">Get-AzImage</span></span>

## <span data-ttu-id="f5b63-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5b63-102">SYNOPSIS</span></span>
<span data-ttu-id="f5b63-103">Pobiera właściwości obrazu.</span><span class="sxs-lookup"><span data-stu-id="f5b63-103">Gets the properties of an image.</span></span>

## <span data-ttu-id="f5b63-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5b63-104">SYNTAX</span></span>

```
Get-AzImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5b63-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f5b63-105">DESCRIPTION</span></span>
<span data-ttu-id="f5b63-106">Polecenie cmdlet **Get-AzImage** pobiera właściwości obrazu.</span><span class="sxs-lookup"><span data-stu-id="f5b63-106">The **Get-AzImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="f5b63-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5b63-107">EXAMPLES</span></span>

### <span data-ttu-id="f5b63-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f5b63-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="f5b63-109">To polecenie pobiera właściwości obrazu o nazwie "Image01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f5b63-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="f5b63-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f5b63-110">Example 2</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01'

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="f5b63-111">To polecenie pobiera właściwości wszystkich obrazów w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f5b63-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="f5b63-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f5b63-112">Example 3</span></span>
```
PS C:\> Get-AzImage

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup02
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup02/prov
                       iders/Microsoft.Compute/images/Image03
Name                 : Image03
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="f5b63-113">To polecenie pobiera właściwości wszystkich obrazów w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f5b63-113">This command gets the properties of all images under the subscription.</span></span>

### <span data-ttu-id="f5b63-114">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="f5b63-114">Example 4</span></span>
```
PS C:\> Get-AzImage -Name "Image*"

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image01
Name                 : Image01
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup01
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/prov
                       iders/Microsoft.Compute/images/Image02
Name                 : Image02
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}

ResourceGroupName    : ResourceGroup02
SourceVirtualMachine : Microsoft.Azure.Management.Compute.Models.SubResource
StorageProfile       : Microsoft.Azure.Management.Compute.Models.ImageStorageProfile
ProvisioningState    : Succeeded
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup02/prov
                       iders/Microsoft.Compute/images/Image03
Name                 : Image03
Type                 : Microsoft.Compute/images
Location             : eastus2
Tags                 : {}
```

<span data-ttu-id="f5b63-115">To polecenie pobiera właściwości wszystkich obrazów w ramach subskrypcji rozpoczynającej się od "Image".</span><span class="sxs-lookup"><span data-stu-id="f5b63-115">This command gets the properties of all images under the subscription that start with "Image".</span></span>

## <span data-ttu-id="f5b63-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5b63-116">PARAMETERS</span></span>

### <span data-ttu-id="f5b63-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5b63-117">-DefaultProfile</span></span>
<span data-ttu-id="f5b63-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5b63-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5b63-119">-Expand</span><span class="sxs-lookup"><span data-stu-id="f5b63-119">-Expand</span></span>
<span data-ttu-id="f5b63-120">Określa zapytanie rozwijające wyrażenie.</span><span class="sxs-lookup"><span data-stu-id="f5b63-120">Specifies the expand expression query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5b63-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="f5b63-121">-ImageName</span></span>
<span data-ttu-id="f5b63-122">Określa nazwę obrazu.</span><span class="sxs-lookup"><span data-stu-id="f5b63-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f5b63-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5b63-123">-ResourceGroupName</span></span>
<span data-ttu-id="f5b63-124">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f5b63-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f5b63-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5b63-125">CommonParameters</span></span>
<span data-ttu-id="f5b63-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5b63-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5b63-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5b63-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5b63-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5b63-128">INPUTS</span></span>

### <span data-ttu-id="f5b63-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f5b63-129">System.String</span></span>

## <span data-ttu-id="f5b63-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5b63-130">OUTPUTS</span></span>

### <span data-ttu-id="f5b63-131">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSImage</span><span class="sxs-lookup"><span data-stu-id="f5b63-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="f5b63-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5b63-132">NOTES</span></span>

## <span data-ttu-id="f5b63-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5b63-133">RELATED LINKS</span></span>

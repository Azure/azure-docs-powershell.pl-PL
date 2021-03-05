---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
ms.openlocfilehash: 430c0d09c56aa4fb57399c97714dc70cb19dd500
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980890"
---
# <span data-ttu-id="7872c-101">New-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="7872c-101">New-AzDiskAccess</span></span>

## <span data-ttu-id="7872c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7872c-102">SYNOPSIS</span></span>
<span data-ttu-id="7872c-103">Tworzy zasób dostępu do dysku</span><span class="sxs-lookup"><span data-stu-id="7872c-103">Creates a Disk Access resource</span></span>

## <span data-ttu-id="7872c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7872c-104">SYNTAX</span></span>

```
New-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7872c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7872c-105">DESCRIPTION</span></span>
<span data-ttu-id="7872c-106">Polecenie **cmdlet New-AzAccess** tworzy zasób dostępu do dysku</span><span class="sxs-lookup"><span data-stu-id="7872c-106">The **New-AzDiskAccess** cmdlet creates a Disk Access resource</span></span>

## <span data-ttu-id="7872c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7872c-107">EXAMPLES</span></span>

### <span data-ttu-id="7872c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7872c-108">Example 1</span></span>
```
PS C:\> New-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" -Location "NorthCentralUS"
```

<span data-ttu-id="7872c-109">To polecenie spowoduje utworzenie dostępu do dysku o podanych właściwościach.</span><span class="sxs-lookup"><span data-stu-id="7872c-109">This command will create a Disk Access with given properties.</span></span> 

## <span data-ttu-id="7872c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7872c-110">PARAMETERS</span></span>

### <span data-ttu-id="7872c-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7872c-111">-AsJob</span></span>
<span data-ttu-id="7872c-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7872c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7872c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7872c-113">-DefaultProfile</span></span>
<span data-ttu-id="7872c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7872c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7872c-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7872c-115">-Location</span></span>
<span data-ttu-id="7872c-116">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="7872c-116">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7872c-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7872c-117">-Name</span></span>
<span data-ttu-id="7872c-118">Określa nazwę dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="7872c-118">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7872c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7872c-119">-ResourceGroupName</span></span>
<span data-ttu-id="7872c-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7872c-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7872c-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7872c-121">-Confirm</span></span>
<span data-ttu-id="7872c-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7872c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7872c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7872c-123">-WhatIf</span></span>
<span data-ttu-id="7872c-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7872c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7872c-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7872c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7872c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7872c-126">CommonParameters</span></span>
<span data-ttu-id="7872c-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7872c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7872c-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7872c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7872c-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7872c-129">INPUTS</span></span>

### <span data-ttu-id="7872c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7872c-130">System.String</span></span>

## <span data-ttu-id="7872c-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7872c-131">OUTPUTS</span></span>

### <span data-ttu-id="7872c-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="7872c-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="7872c-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7872c-133">NOTES</span></span>

## <span data-ttu-id="7872c-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7872c-134">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGallery.md
ms.openlocfilehash: 2ea4bc3d1e3e6c88ec615feda97c12891030c9c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706349"
---
# <span data-ttu-id="404ea-101">New-AzGallery</span><span class="sxs-lookup"><span data-stu-id="404ea-101">New-AzGallery</span></span>

## <span data-ttu-id="404ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="404ea-102">SYNOPSIS</span></span>
<span data-ttu-id="404ea-103">Tworzenie galerii.</span><span class="sxs-lookup"><span data-stu-id="404ea-103">Create a gallery.</span></span>

## <span data-ttu-id="404ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="404ea-104">SYNTAX</span></span>

```
New-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Location] <String>
 [-Description <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="404ea-105">Opis</span><span class="sxs-lookup"><span data-stu-id="404ea-105">DESCRIPTION</span></span>
<span data-ttu-id="404ea-106">Tworzenie galerii.</span><span class="sxs-lookup"><span data-stu-id="404ea-106">Create a gallery.</span></span>

## <span data-ttu-id="404ea-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="404ea-107">EXAMPLES</span></span>

### <span data-ttu-id="404ea-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="404ea-108">Example 1</span></span>
```powershell
PS C:\> New-AzGallery -ResourceGroupName $rgname -Name $galleryName -Location $location -Description $galleryDescription
```

<span data-ttu-id="404ea-109">Tworzenie galerii.</span><span class="sxs-lookup"><span data-stu-id="404ea-109">Create a gallery.</span></span>

## <span data-ttu-id="404ea-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="404ea-110">PARAMETERS</span></span>

### <span data-ttu-id="404ea-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="404ea-111">-AsJob</span></span>
<span data-ttu-id="404ea-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="404ea-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="404ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="404ea-113">-DefaultProfile</span></span>
<span data-ttu-id="404ea-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="404ea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="404ea-115">— Opis</span><span class="sxs-lookup"><span data-stu-id="404ea-115">-Description</span></span>
<span data-ttu-id="404ea-116">Opis zasobu galerii.</span><span class="sxs-lookup"><span data-stu-id="404ea-116">The description of the gallery resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404ea-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="404ea-117">-Location</span></span>
<span data-ttu-id="404ea-118">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="404ea-118">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404ea-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="404ea-119">-Name</span></span>
<span data-ttu-id="404ea-120">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="404ea-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404ea-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="404ea-121">-ResourceGroupName</span></span>
<span data-ttu-id="404ea-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="404ea-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="404ea-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="404ea-123">-Tag</span></span>
<span data-ttu-id="404ea-124">Znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="404ea-124">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404ea-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="404ea-125">-Confirm</span></span>
<span data-ttu-id="404ea-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="404ea-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="404ea-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="404ea-127">-WhatIf</span></span>
<span data-ttu-id="404ea-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="404ea-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="404ea-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="404ea-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="404ea-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="404ea-130">CommonParameters</span></span>
<span data-ttu-id="404ea-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="404ea-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="404ea-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="404ea-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="404ea-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="404ea-133">INPUTS</span></span>

### <span data-ttu-id="404ea-134">System. String</span><span class="sxs-lookup"><span data-stu-id="404ea-134">System.String</span></span>

### <span data-ttu-id="404ea-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="404ea-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="404ea-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="404ea-136">OUTPUTS</span></span>

### <span data-ttu-id="404ea-137">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGallery</span><span class="sxs-lookup"><span data-stu-id="404ea-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="404ea-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="404ea-138">NOTES</span></span>

## <span data-ttu-id="404ea-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="404ea-139">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
ms.openlocfilehash: 414a732dd80850a31a87f88d3dfdbf091cb4a6a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223254"
---
# <span data-ttu-id="7f23c-101">Remove-AzPeering</span><span class="sxs-lookup"><span data-stu-id="7f23c-101">Remove-AzPeering</span></span>

## <span data-ttu-id="7f23c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f23c-102">SYNOPSIS</span></span>
<span data-ttu-id="7f23c-103">Usuwanie lub usuwanie komunikacji równorzędnej.</span><span class="sxs-lookup"><span data-stu-id="7f23c-103">Delete or remove a peering.</span></span> <span data-ttu-id="7f23c-104">Spowoduje to usunięcie wszystkich zasobów podrzędnych lub alertów dotyczących zasobu.</span><span class="sxs-lookup"><span data-stu-id="7f23c-104">This will delete all child resources or alerting on the resource.</span></span>

## <span data-ttu-id="7f23c-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f23c-105">SYNTAX</span></span>

### <span data-ttu-id="7f23c-106">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7f23c-106">ByName (Default)</span></span>
```
Remove-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f23c-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="7f23c-107">InputObject</span></span>
```
Remove-AzPeering [-InputObject] <PSPeering> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f23c-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7f23c-108">ByResourceId</span></span>
```
Remove-AzPeering -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f23c-109">Opis</span><span class="sxs-lookup"><span data-stu-id="7f23c-109">DESCRIPTION</span></span>
<span data-ttu-id="7f23c-110">Perminently usunąć zasób równorzędny.</span><span class="sxs-lookup"><span data-stu-id="7f23c-110">Perminently delete a peering resource.</span></span>

## <span data-ttu-id="7f23c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f23c-111">EXAMPLES</span></span>

### <span data-ttu-id="7f23c-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7f23c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeering -ResourceId $resourceId
```

<span data-ttu-id="7f23c-113">Usuwanie komunikacji równorzędnej według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="7f23c-113">Remove a peering by resource id.</span></span>

## <span data-ttu-id="7f23c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f23c-114">PARAMETERS</span></span>

### <span data-ttu-id="7f23c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f23c-115">-AsJob</span></span>
<span data-ttu-id="7f23c-116">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="7f23c-116">Run in the background.</span></span>

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

### <span data-ttu-id="7f23c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f23c-117">-DefaultProfile</span></span>
<span data-ttu-id="7f23c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f23c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f23c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7f23c-119">-Force</span></span>
<span data-ttu-id="7f23c-120">Wymuszanie ukończenia operacji</span><span class="sxs-lookup"><span data-stu-id="7f23c-120">Force the operation to complete</span></span>

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

### <span data-ttu-id="7f23c-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7f23c-121">-InputObject</span></span>
<span data-ttu-id="7f23c-122">Użyj Get-AzPeering, aby pobrać ten obiekt.</span><span class="sxs-lookup"><span data-stu-id="7f23c-122">Use Get-AzPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f23c-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7f23c-123">-Name</span></span>
<span data-ttu-id="7f23c-124">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="7f23c-124">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f23c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f23c-125">-PassThru</span></span>
<span data-ttu-id="7f23c-126">Zwraca wartość PRAWDA, jeśli została ukończona</span><span class="sxs-lookup"><span data-stu-id="7f23c-126">Return true if complete</span></span>

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

### <span data-ttu-id="7f23c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f23c-127">-ResourceGroupName</span></span>
<span data-ttu-id="7f23c-128">Tworzenie lub używanie istniejącej nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7f23c-128">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f23c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f23c-129">-ResourceId</span></span>
<span data-ttu-id="7f23c-130">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="7f23c-130">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f23c-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f23c-131">-Confirm</span></span>
<span data-ttu-id="7f23c-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f23c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f23c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f23c-133">-WhatIf</span></span>
<span data-ttu-id="7f23c-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f23c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f23c-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7f23c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f23c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f23c-136">CommonParameters</span></span>
<span data-ttu-id="7f23c-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f23c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f23c-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f23c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f23c-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f23c-139">INPUTS</span></span>

### <span data-ttu-id="7f23c-140">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeering</span><span class="sxs-lookup"><span data-stu-id="7f23c-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="7f23c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7f23c-141">System.String</span></span>

## <span data-ttu-id="7f23c-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f23c-142">OUTPUTS</span></span>

### <span data-ttu-id="7f23c-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7f23c-143">System.Boolean</span></span>

## <span data-ttu-id="7f23c-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f23c-144">NOTES</span></span>

## <span data-ttu-id="7f23c-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f23c-145">RELATED LINKS</span></span>

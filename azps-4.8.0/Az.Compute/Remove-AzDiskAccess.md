---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
ms.openlocfilehash: 4b67364f0d079c7cd5fbbdd89b1a84b4dc6fee0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064269"
---
# <span data-ttu-id="2c3f0-101">Remove-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="2c3f0-101">Remove-AzDiskAccess</span></span>

## <span data-ttu-id="2c3f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c3f0-102">SYNOPSIS</span></span>
<span data-ttu-id="2c3f0-103">Usuwa zasób dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="2c3f0-103">Removes a disk access resource.</span></span>

## <span data-ttu-id="2c3f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c3f0-104">SYNTAX</span></span>

### <span data-ttu-id="2c3f0-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2c3f0-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c3f0-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c3f0-106">ResourceIDParameterSet</span></span>
```
Remove-AzDiskAccess [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c3f0-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c3f0-107">InputObjectParameterSet</span></span>
```
Remove-AzDiskAccess [-InputObject] <PSDiskAccess> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c3f0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2c3f0-108">DESCRIPTION</span></span>
<span data-ttu-id="2c3f0-109">Polecenie cmdlet **Remove-AzDiskAccess** usuwa zasób dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="2c3f0-109">The **Remove-AzDiskAccess** cmdlet removes a disk access resource.</span></span>

## <span data-ttu-id="2c3f0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c3f0-110">EXAMPLES</span></span>

### <span data-ttu-id="2c3f0-111">Przykład 1: Usuwanie dostępu do dysku przy użyciu domyślnego zestawu parametrów</span><span class="sxs-lookup"><span data-stu-id="2c3f0-111">Example 1: Remove Disk Access using Default Parameter Set</span></span>
```
PS C:\> Remove-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
```

<span data-ttu-id="2c3f0-112">To polecenie usuwa dostęp do dysku o nazwie "DiskAccess01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="2c3f0-112">This command removes the disk access named "DiskAccess01" in resource group "ResourceGroup01"</span></span>

### <span data-ttu-id="2c3f0-113">Przykład 2: Usuwanie dostępu do dysku przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="2c3f0-113">Example 2: Remove Disk Access using Resource ID</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -ResourceId $myDiskAccess.id
```

<span data-ttu-id="2c3f0-114">To polecenie usuwa dostęp do dysku według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="2c3f0-114">This command removes the disk access by Resource ID</span></span>

### <span data-ttu-id="2c3f0-115">Przykład 3: Usuwanie dostępu do dysku przy użyciu obiektu wejściowego</span><span class="sxs-lookup"><span data-stu-id="2c3f0-115">Example 3: Remove Disk Access using Input Object</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -InputObject $myDiskAccess
```

<span data-ttu-id="2c3f0-116">To polecenie usuwa dostęp do dysku przez program Inputobject</span><span class="sxs-lookup"><span data-stu-id="2c3f0-116">This command removes the disk access by InputObject</span></span>

### <span data-ttu-id="2c3f0-117">Przykład 4: Usuwanie dostępu do dysku przez obiekt wejściowy instalacji rurowej</span><span class="sxs-lookup"><span data-stu-id="2c3f0-117">Example 4: Remove Disk Access by piping Input Object</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" | Remove-AzDiskAccess 
```

<span data-ttu-id="2c3f0-118">To polecenie usuwa dostęp do dysku przez przewody wejściowe</span><span class="sxs-lookup"><span data-stu-id="2c3f0-118">This command removes the disk access by piping the InputObject</span></span>

## <span data-ttu-id="2c3f0-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c3f0-119">PARAMETERS</span></span>

### <span data-ttu-id="2c3f0-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c3f0-120">-AsJob</span></span>
<span data-ttu-id="2c3f0-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2c3f0-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2c3f0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c3f0-122">-DefaultProfile</span></span>
<span data-ttu-id="2c3f0-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c3f0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c3f0-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2c3f0-124">-InputObject</span></span>
<span data-ttu-id="2c3f0-125">Obiekt programu Access z dysku</span><span class="sxs-lookup"><span data-stu-id="2c3f0-125">PowerShell Disk Access Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess
Parameter Sets: InputObjectParameterSet
Aliases: DiskAccess

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c3f0-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2c3f0-126">-Name</span></span>
<span data-ttu-id="2c3f0-127">Określa nazwę dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="2c3f0-127">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c3f0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c3f0-128">-ResourceGroupName</span></span>
<span data-ttu-id="2c3f0-129">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2c3f0-129">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c3f0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c3f0-130">-ResourceId</span></span>
<span data-ttu-id="2c3f0-131">Identyfikator zasobu w celu uzyskania dostępu do dysku.</span><span class="sxs-lookup"><span data-stu-id="2c3f0-131">Resource ID for your disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c3f0-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2c3f0-132">-Confirm</span></span>
<span data-ttu-id="2c3f0-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c3f0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c3f0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c3f0-134">-WhatIf</span></span>
<span data-ttu-id="2c3f0-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c3f0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c3f0-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2c3f0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c3f0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c3f0-137">CommonParameters</span></span>
<span data-ttu-id="2c3f0-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c3f0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c3f0-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c3f0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c3f0-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c3f0-140">INPUTS</span></span>

### <span data-ttu-id="2c3f0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2c3f0-141">System.String</span></span>

### <span data-ttu-id="2c3f0-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="2c3f0-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="2c3f0-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c3f0-143">OUTPUTS</span></span>

### <span data-ttu-id="2c3f0-144">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="2c3f0-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="2c3f0-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c3f0-145">NOTES</span></span>

## <span data-ttu-id="2c3f0-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c3f0-146">RELATED LINKS</span></span>

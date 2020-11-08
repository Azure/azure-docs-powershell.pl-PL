---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 0fbf44e9a68a5cfaaea4138ec17caa2960a41e67
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063265"
---
# <span data-ttu-id="f5023-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="f5023-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="f5023-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5023-102">SYNOPSIS</span></span>
<span data-ttu-id="f5023-103">Usuwa nowy prefiks usługi peer-and.</span><span class="sxs-lookup"><span data-stu-id="f5023-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="f5023-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5023-104">SYNTAX</span></span>

### <span data-ttu-id="f5023-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f5023-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PrefixName] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5023-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="f5023-106">InputObject</span></span>
```
Remove-AzPeeringServicePrefix [-InputObject] <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5023-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f5023-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5023-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f5023-108">DESCRIPTION</span></span>
<span data-ttu-id="f5023-109">Usuwa prefiks usługi peer-in z usługi peer.</span><span class="sxs-lookup"><span data-stu-id="f5023-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="f5023-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5023-110">EXAMPLES</span></span>

### <span data-ttu-id="f5023-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f5023-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="f5023-112">Usuwanie prefiksu z obiektu usługi komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="f5023-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="f5023-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f5023-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="f5023-114">Usuwanie prefiksu z identyfikatora zasobu usługi peer.</span><span class="sxs-lookup"><span data-stu-id="f5023-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="f5023-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f5023-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="f5023-116">Usuwanie prefiksu z nazwy i nazwy grupy zasobów usługi peer Relationships</span><span class="sxs-lookup"><span data-stu-id="f5023-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="f5023-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5023-117">PARAMETERS</span></span>

### <span data-ttu-id="f5023-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5023-118">-AsJob</span></span>
<span data-ttu-id="f5023-119">Działa w tle.</span><span class="sxs-lookup"><span data-stu-id="f5023-119">Run in the background.</span></span>

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

### <span data-ttu-id="f5023-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5023-120">-DefaultProfile</span></span>
<span data-ttu-id="f5023-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5023-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5023-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f5023-122">-Force</span></span>
<span data-ttu-id="f5023-123">Wymuszanie ukończenia operacji</span><span class="sxs-lookup"><span data-stu-id="f5023-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="f5023-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f5023-124">-InputObject</span></span>
<span data-ttu-id="f5023-125">Używanie Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="f5023-125">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5023-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f5023-126">-Name</span></span>
<span data-ttu-id="f5023-127">Unikatowa nazwa PSPeering.</span><span class="sxs-lookup"><span data-stu-id="f5023-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="f5023-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5023-128">-PassThru</span></span>
<span data-ttu-id="f5023-129">Zwraca wartość PRAWDA dla powodzenia lub fałszu w przypadku niepowodzenia.</span><span class="sxs-lookup"><span data-stu-id="f5023-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="f5023-130">-Prefixname</span><span class="sxs-lookup"><span data-stu-id="f5023-130">-PrefixName</span></span>
<span data-ttu-id="f5023-131">Nazwa prefiksu.</span><span class="sxs-lookup"><span data-stu-id="f5023-131">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5023-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5023-132">-ResourceGroupName</span></span>
<span data-ttu-id="f5023-133">Tworzenie lub używanie istniejącej nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f5023-133">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="f5023-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5023-134">-ResourceId</span></span>
<span data-ttu-id="f5023-135">Nazwa ciągu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="f5023-135">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5023-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f5023-136">-Confirm</span></span>
<span data-ttu-id="f5023-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5023-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5023-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5023-138">-WhatIf</span></span>
<span data-ttu-id="f5023-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5023-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5023-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f5023-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5023-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5023-141">CommonParameters</span></span>
<span data-ttu-id="f5023-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5023-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5023-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5023-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5023-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5023-144">INPUTS</span></span>

### <span data-ttu-id="f5023-145">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="f5023-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="f5023-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f5023-146">System.String</span></span>

## <span data-ttu-id="f5023-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5023-147">OUTPUTS</span></span>

### <span data-ttu-id="f5023-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5023-148">System.Boolean</span></span>

## <span data-ttu-id="f5023-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5023-149">NOTES</span></span>

## <span data-ttu-id="f5023-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5023-150">RELATED LINKS</span></span>

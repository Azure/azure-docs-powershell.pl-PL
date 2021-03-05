---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: 02a8fef51ca0689fb92d3990bf5bcc182f902549
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996241"
---
# <span data-ttu-id="40ec3-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="40ec3-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="40ec3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40ec3-102">SYNOPSIS</span></span>
<span data-ttu-id="40ec3-103">Usuwa profil sieciowy.</span><span class="sxs-lookup"><span data-stu-id="40ec3-103">Removes a network profile.</span></span>

## <span data-ttu-id="40ec3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="40ec3-104">SYNTAX</span></span>

### <span data-ttu-id="40ec3-105">RemoveByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="40ec3-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40ec3-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40ec3-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40ec3-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40ec3-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40ec3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="40ec3-108">DESCRIPTION</span></span>
<span data-ttu-id="40ec3-109">Polecenie **cmdlet Remove-AzNetworkProfile** usuwa profil sieciowy, jeśli nie utworzono interfejsów sieciowych kontenerów (w odróżnieniu od konfiguracji kontenera interfejsu sieciowego).</span><span class="sxs-lookup"><span data-stu-id="40ec3-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration**) have been created.</span></span>

## <span data-ttu-id="40ec3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="40ec3-110">EXAMPLES</span></span>

### <span data-ttu-id="40ec3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="40ec3-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="40ec3-112">Spowoduje to usunięcie profilu sieciowego o nazwie np1 z grupy zasobów rg1.</span><span class="sxs-lookup"><span data-stu-id="40ec3-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="40ec3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40ec3-113">PARAMETERS</span></span>

### <span data-ttu-id="40ec3-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="40ec3-114">-AsJob</span></span>
<span data-ttu-id="40ec3-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="40ec3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40ec3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40ec3-116">-DefaultProfile</span></span>
<span data-ttu-id="40ec3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="40ec3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40ec3-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="40ec3-118">-Force</span></span>
<span data-ttu-id="40ec3-119">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="40ec3-119">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="40ec3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40ec3-120">-InputObject</span></span>
<span data-ttu-id="40ec3-121">Obiekt profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="40ec3-121">Network profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40ec3-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="40ec3-122">-Name</span></span>
<span data-ttu-id="40ec3-123">Nazwa profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="40ec3-123">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40ec3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40ec3-124">-PassThru</span></span>
<span data-ttu-id="40ec3-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="40ec3-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="40ec3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40ec3-126">-ResourceGroupName</span></span>
<span data-ttu-id="40ec3-127">Nazwa grupy zasobów profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="40ec3-127">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40ec3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40ec3-128">-ResourceId</span></span>
<span data-ttu-id="40ec3-129">Identyfikator zasobu menedżera zasobów platformy Azure profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="40ec3-129">The Azure resource manager resource ID of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40ec3-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="40ec3-130">-Confirm</span></span>
<span data-ttu-id="40ec3-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="40ec3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40ec3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40ec3-132">-WhatIf</span></span>
<span data-ttu-id="40ec3-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40ec3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40ec3-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="40ec3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40ec3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40ec3-135">CommonParameters</span></span>
<span data-ttu-id="40ec3-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40ec3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40ec3-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40ec3-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40ec3-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40ec3-138">INPUTS</span></span>

### <span data-ttu-id="40ec3-139">System.String</span><span class="sxs-lookup"><span data-stu-id="40ec3-139">System.String</span></span>

### <span data-ttu-id="40ec3-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="40ec3-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="40ec3-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40ec3-141">OUTPUTS</span></span>

### <span data-ttu-id="40ec3-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="40ec3-142">System.Boolean</span></span>

## <span data-ttu-id="40ec3-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="40ec3-143">NOTES</span></span>

## <span data-ttu-id="40ec3-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40ec3-144">RELATED LINKS</span></span>

[<span data-ttu-id="40ec3-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="40ec3-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="40ec3-146">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="40ec3-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="40ec3-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="40ec3-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
